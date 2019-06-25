# Ethernet OAM / Ethernet CFM

## URL

```
frinx-oam:oam
```

## OPENCONFIG YANG

[YANG models](https://github.com/FRINXio/openconfig/tree/master/oam/src/main/yang)

```javascript
{
    "frinx-oam:oam": {
        "cfm": {
            "domains" {
                "domain": [
                    {
                        "domain-name": "{{domain_name}}",
                        "config": {
                            "domain-name": "{{domain_name}}",
                            "level": {{level}}
                        },
                        "mas": {
                            "ma": [
                                {
                                    "ma-name": "{{ma_name}}",
                                    "config": {
                                        "ma-name": "{{ma_name}}"
                                    }
                                }
                            ]
                        }
                    }
                ]
            }
        }
    }
}
```

## OS Configuration Commands

### Cisco IOS XR 6.6.2

#### CLI

<pre>
ethernet cfm
 domain {{domain_name}} level {{level}}
  service {{ma_name}} down-meps
</pre>

#### Unit

Link to github : [xr-unit](https://github.com/FRINXio/cli-units/tree/master/ios-xr/oam)
