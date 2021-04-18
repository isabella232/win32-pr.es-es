---
description: La aplicación debe crear las propiedades con un tipo de datos que se asigna al tipo de datos del registro.
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: Asignar un tipo de datos del registro a un tipo de datos WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b96a3bcda0060e376427375059f006e3241118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546374"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>Asignar un tipo de datos del registro a un tipo de datos WMI

La aplicación debe crear las propiedades con un tipo de datos que se asigna al tipo de datos del registro. No es necesario especificar el tipo de datos del registro en los métodos que crean, obtienen o establecen valores del registro. Sin embargo, el parámetro de entrada que contiene el valor debe estar en el tipo de datos WMI correcto. Por ejemplo, si una aplicación recibe datos de **reg \_ DWORD** del registro, la clase que recibe los datos debe incluir una propiedad **Uint32** .

En la tabla siguiente se muestra la asignación entre los tipos de datos del registro y WMI utilizados en los métodos [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) .



| Tipo de datos del registro      | Tipo de datos WMI                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_binario de reg**         | **Uint8** (matriz)<br/> Una matriz de valores que no superan 255 o Hex FF. Por ejemplo, el siguiente código de script de Visual Basic crea una matriz que se ajusta a este tipo de datos.<br/> `BinArray = Array(&H01, &Ha2)`<br/> El método [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) de la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) requiere el tipo de datos **reg \_ binario** .<br/>                                                                                          |
| **\_valor DWORD reg**          | **UInt32**, **sint32** o Visual Basic **entero**<br/> Un único valor de 32 bits. Los métodos de la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov) y [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) requieren el tipo de datos **reg \_ DWORD** .<br/>                                                                                                                                                                  |
| **Registro \_ SZ**             | **string**<br/> El método de clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) requiere el tipo de datos **reg \_ SZ** .<br/>                                                                                                                                                                                                                                                                                                            |
| **QWord de REG \_**          | **UInt64**.<br/> Un único valor de 64 bits. Los métodos de la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetQWORDValue**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov) y [**SetQWORDValue**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov) requieren el tipo de datos **reg \_ QWord** .<br/>                                                                                                                                                                                                         |
| **REG \_ expandir \_ SZ**     | **string**<br/> Las cadenas expandidas son cadenas especiales que representan variables de entorno del sistema. Por ejemplo, el siguiente código de VBScript crea una cadena que representa la variable de entorno del **\_ \_ usuario local HKEY** Temp.<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> El método de clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) requiere el tipo de datos **reg \_ Expand \_** .<br/> |
| **REG \_ multi \_ SZ**      | matriz de **cadenas**<br/> El tipo de datos multistring contiene varias cadenas. Por ejemplo, el siguiente código de VBScript crea una matriz que se ajusta a este tipo de datos.<br/> `MultiValue = Array("first", "second", "third")`<br/> El método de clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) requiere el tipo de datos **reg \_ multi \_ SZ** .<br/>                                                                     |
| **\_lista de recursos del registro \_** | Según el caso. Para obtener más información, vea [Descripción de un recurso para el registro](describing-a-resource-for-the-registry.md).<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Definir clases para el proveedor del registro del sistema](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

