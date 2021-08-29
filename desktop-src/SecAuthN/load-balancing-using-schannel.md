---
description: Cada servidor puede establecer un valor de clave del Registro MachineID en el Registro que se establece como una parte fija del identificador de sesión.
ms.assetid: 1B373496-1C1B-4D4B-8CAC-B572C58E43A2
title: Equilibrio de carga mediante Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b4b65802a1d354e085cab31ecf3cc6c0a99e2c36cb2cb5e5ba2c56b786e952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922350"
---
# <a name="load-balancing-using-schannel"></a>Equilibrio de carga mediante Schannel

Cada servidor puede establecer un valor de clave del Registro MachineID en el Registro que se establece como una parte fija del identificador de sesión. La clave del Registro MachineID es un **tipo de valor REG \_ DWORD.** El equilibrador de carga puede usar esta parte del identificador de sesión para determinar qué servidor ha generado la sesión SSL y puede mantener la asignación a ese servidor. El identificador de sesión forma parte del protocolo de enlace SSL/TLS que se envía a través de la conexión. El código del equilibrador de carga debe usar el segundo **DWORD** en el identificador de sesión al reanudar o volver a conectarse al cliente. El segundo **DWORD** del identificador de sesión aleatorio generado por un servidor Schannel se reemplaza por el **DWORD** almacenado en el registro. El valor del Registro para **DWORD** no se puede 0xffffffff.

El valor de la clave del Registro es el siguiente.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            SecurityProviders
               SCHANNEL
                  MachineID<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

 

 



