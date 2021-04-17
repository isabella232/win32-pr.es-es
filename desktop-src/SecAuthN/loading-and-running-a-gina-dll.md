---
description: Windows carga y ejecuta el archivo DLL estándar de Microsoft GINA (MSGina.dll). Para cargar un GINA diferente, debe modificar un valor de clave del registro.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Cargar y ejecutar un archivo DLL de GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652725"
---
# <a name="loading-and-running-a-gina-dll"></a>Cargar y ejecutar un archivo DLL de GINA

Windows carga y ejecuta el archivo DLL estándar de Microsoft GINA (MSGina.dll). Para cargar un [*Gina*](../secgloss/g-gly.md)diferente, debe modificar el siguiente valor de clave del registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

Si el valor de la clave GinaDLL está presente, debe contener el nombre de un archivo DLL de GINA, que [*Winlogon*](../secgloss/w-gly.md) cargará y usará.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar y probar un archivo DLL de GINA](building-and-testing-a-gina-dll.md)
</dt> <dt>

[Funciones de exportación de GINA](authentication-functions.md)
</dt> <dt>

[Estructuras GINA](authentication-structures.md)
</dt> <dt>

[Terminal Services funciones GINA](terminal-services-gina-functions.md)
</dt> </dl>

 

 
