---
description: Agrega un archivo MOF a la lista de archivos compilados durante la recuperación del repositorio.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma autorecover
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
ms.openlocfilehash: cc36191482731e77d0f82c4e3734350da2f6ed2fbd3faad7b2972dca4e0e6bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992705"
---
# <a name="pragma-autorecover"></a>pragma autorecover

El **comando pragma autorecover** preprocessor agrega un archivo MOF a la lista de archivos compilados durante la recuperación del repositorio. La lista de archivos MOF **de recuperación** automática se almacena en esta clave del Registro:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **autorecover mofs**

WMI comprueba la integridad del repositorio WMI cuando el sistema operativo inicia WMI. Si el repositorio está dañado, WMI recompila automáticamente el repositorio y vuelve a compilar los archivos MOF enumerados en esta clave en el Registro.

A continuación se describe la sintaxis del comando pragma autorecover:


```mof
#pragma autorecover
```



Sin embargo, debe observar las restricciones siguientes al usar este comando:

-   WMI no puede recuperar archivos MOF ubicados en un equipo remoto.

    Por lo tanto, los archivos MOF enumerados en esta clave del Registro deben residir en el equipo local.

-   No se pueden especificar los modificadores de línea de comandos que usa el compilador MOF cuando WMI recupera un archivo MOF.

    Por lo tanto, debe incluir [comandos pragma](-pragma.md) en el archivo MOF que hacen que los modificadores de línea de comandos sean innecesarios. En el ejemplo siguiente se describe un modificador de línea de comandos común que WMI no usa al recuperar un archivo MOF desde esta clave del Registro: **mofcomp -N:Root \\ Test mymof.mof**

    Sin embargo, puede especificar el espacio de nombres mediante un [comando pragma](-pragma.md) en el archivo MOF.

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 




