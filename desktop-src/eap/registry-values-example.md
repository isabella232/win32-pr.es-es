---
title: Ejemplo de valores del registro
description: En el ejemplo siguiente se muestran los datos posibles para algunos de los valores del registro del Protocolo de autenticación.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104077160"
---
# <a name="registry-values-example"></a>Ejemplo de valores del registro

En el ejemplo siguiente se muestran los datos posibles para algunos de los valores del registro del Protocolo de autenticación.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| Nombre de clave            | Datatype        | Value                                  |
|---------------------|-----------------|----------------------------------------|
| Ruta                | REG \_ expandir \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| FriendlyName        | Registro \_ SZ         | Protocolo EAP de ejemplo                    |
| ConfigUIPath        | REG \_ expandir \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| IdentityPath        | REG \_ expandir \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| InteractiveUIPath   | REG \_ expandir \_ SZ | % SystemRoot% \\ system32 \\sample.dll     |
| RequireConfigUI     | \_valor DWORD reg      | 1                                      |
| ConfigCLSID         | Registro \_ SZ         | {0000031A-0000-0000-C000-000000000046} |
| StandaloneSupported | \_valor DWORD reg      | 1                                      |



 

 

 




