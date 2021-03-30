---
description: Agrega un archivo MOF a la lista de archivos compilados durante la recuperación del repositorio.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: Autorrecuperación de pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002650"
---
# <a name="pragma-autorecover"></a>Autorrecuperación de pragma

El comando **pragma autocover** del preprocesador agrega un archivo MOF a la lista de archivos compilados durante la recuperación del repositorio. La lista de archivos MOF de **Autorrecuperación** se almacena en esta clave del registro:

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **autocover MOF**

WMI comprueba la integridad del repositorio WMI cuando el sistema operativo inicia WMI. Si el repositorio está dañado, WMI vuelve a generar automáticamente el repositorio y vuelve a compilar los archivos MOF enumerados en esta clave en el registro.

A continuación se describe la sintaxis del comando pragma autocover:


```mof
#pragma autorecover
```



Sin embargo, debe observar las restricciones siguientes al usar este comando:

-   WMI no puede recuperar archivos MOF ubicados en un equipo remoto.

    Por lo tanto, los archivos MOF que se enumeran en esta clave del registro deben residir en el equipo local.

-   No se pueden especificar los modificadores de línea de comandos que utiliza el compilador MOF cuando WMI recupera un archivo MOF.

    Por lo tanto, debe incluir comandos [pragma](-pragma.md) en el archivo MOF que hacen que los modificadores de línea de comandos no sean necesarios. En el siguiente ejemplo se describe un modificador de la línea de comandos común que WMI no utiliza al recuperar un archivo MOF de esta clave del registro: **MOFCOMP-N:root \\ Test mymof. mof**

    Sin embargo, puede especificar el espacio de nombres mediante un comando [pragma](-pragma.md) en el archivo MOF.

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 




