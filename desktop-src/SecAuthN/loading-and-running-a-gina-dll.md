---
description: Windows carga y ejecuta el archivo DLL estándar de Microsoft GINA (MSGina.dll). Para cargar una GINA diferente, debe modificar un valor de clave del Registro.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Carga y ejecución de un archivo DLL de GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a4e8d68a1e1846a28e1db9402d730834768a132a7c502021fd101f20926f54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140958"
---
# <a name="loading-and-running-a-gina-dll"></a>Carga y ejecución de un archivo DLL de GINA

Windows carga y ejecuta el archivo DLL estándar de Microsoft GINA (MSGina.dll). Para cargar una [*GINA diferente,*](../secgloss/g-gly.md)debe modificar el siguiente valor de clave del Registro:

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

Si el valor de clave GinaDLL está presente, debe contener el nombre de un archivo DLL de GINA que [*Winlogon*](../secgloss/w-gly.md) cargará y usará.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar y probar un archivo DLL de GINA](building-and-testing-a-gina-dll.md)
</dt> <dt>

[Funciones de exportación de GINA](authentication-functions.md)
</dt> <dt>

[Estructuras de GINA](authentication-structures.md)
</dt> <dt>

[Funciones GINA de Terminal Services](terminal-services-gina-functions.md)
</dt> </dl>

 

 
