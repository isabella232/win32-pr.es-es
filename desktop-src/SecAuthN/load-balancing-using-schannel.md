---
description: Cada servidor puede establecer un valor de clave del registro MachineID en el registro que se establece como una parte fija del identificador de sesión.
ms.assetid: 1B373496-1C1B-4D4B-8CAC-B572C58E43A2
title: Equilibrio de carga mediante Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce190d665f4cc41eb0615a2ddc83e0ee54798d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910346"
---
# <a name="load-balancing-using-schannel"></a>Equilibrio de carga mediante Schannel

Cada servidor puede establecer un valor de clave del registro MachineID en el registro que se establece como una parte fija del identificador de sesión. La clave del registro MachineID es un tipo de valor de **reg \_ DWORD** . El equilibrador de carga puede utilizar esta parte del ID. de sesión para determinar qué servidor ha generado la sesión SSL y puede mantener la asignación a ese servidor. El ID. de sesión forma parte del Protocolo de enlace SSL/TLS que se envía a través de la conexión. El código del equilibrador de carga debe usar el segundo **valor DWORD** en el identificador de sesión al reanudar o volver a conectar al cliente. El segundo **valor DWORD** del ID. de sesión aleatorio generado por un servidor Schannel se reemplaza por el **valor DWORD** almacenado en el registro. El valor del registro para **DWORD** no puede ser 0xFFFFFFFF.

El valor de la clave del registro es el siguiente.

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

 

 



