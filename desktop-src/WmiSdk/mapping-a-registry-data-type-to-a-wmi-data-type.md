---
description: La aplicación debe crear las propiedades con un tipo de datos que se asigna al tipo de datos del Registro.
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: Asignar un tipo de datos del Registro a un tipo de datos WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e620d51eee52592df946e822165d8ed1833214c6f75519d4274b0d7fe3f5550c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050693"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>Asignar un tipo de datos del Registro a un tipo de datos WMI

La aplicación debe crear las propiedades con un tipo de datos que se asigna al tipo de datos del Registro. No es necesario especificar el tipo de datos del Registro en los métodos que crean, obtienen o establecen valores del Registro. Sin embargo, el parámetro de entrada que contiene el valor debe estar en el tipo de datos WMI correcto. Por ejemplo, si una aplicación recibe datos **\_ REG DWORD** del Registro, la clase que recibe los datos debe incluir una **propiedad Uint32.**

En la tabla siguiente se muestra la asignación entre los tipos de datos del Registro y WMI usados en [**los métodos StdRegProv.**](/previous-versions/windows/desktop/regprov/stdregprov)



| Tipo de datos del Registro      | Tipo de datos WMI                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **REG \_ BINARY**         | **Matriz uint8**<br/> Matriz de valores que no superan los 255 o hexadecimales ff. Por ejemplo, el siguiente código Visual Basic script crea una matriz que se ajusta a este tipo de datos.<br/> `BinArray = Array(&H01, &Ha2)`<br/> El [**método de clase StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) requiere el **tipo de datos REG \_ BINARY.**<br/>                                                                                          |
| **REG \_ DWORD**          | **uint32,** **sint32** o Visual Basic **entero**<br/> Un único valor de 32 bits. Los [**métodos de clase StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov) y [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) requieren el **tipo de datos REG \_ DWORD.**<br/>                                                                                                                                                                  |
| **REG \_ SZ**             | **string**<br/> El [**método de clase StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) requiere el **tipo de datos REG \_ SZ.**<br/>                                                                                                                                                                                                                                                                                                            |
| **REG \_ QWORD**          | **uint64**.<br/> Un único valor de 64 bits. Los métodos de clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetQWORDValue**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov) y [**SetQWORDValue**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov) requieren el **tipo de datos REG \_ QWORD.**<br/>                                                                                                                                                                                                         |
| **REG \_ EXPAND \_ SZ**     | **string**<br/> Las cadenas expandida son cadenas especiales que representan variables de entorno del sistema. Por ejemplo, el siguiente código VBScript crea una cadena que representa la variable de entorno **HKEY \_ LOCAL \_ USER** TEMP.<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> El [**método de clase StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) requiere el **tipo de datos REG EXPAND \_ \_ SZ.**<br/> |
| **REG \_ MULTI \_ SZ**      | **Matriz de** cadenas<br/> El tipo de datos Multistring contiene varias cadenas. Por ejemplo, el siguiente código VBScript crea una matriz que se ajusta a este tipo de datos.<br/> `MultiValue = Array("first", "second", "third")`<br/> El [**método de clase StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) requiere el tipo de **datos REG MULTI \_ \_ SZ.**<br/>                                                                     |
| **REG \_ RESOURCE \_ LIST** | Según el caso. Para obtener más información, [vea Describing a Resource for the Registry](describing-a-resource-for-the-registry.md).<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Definir clases para el proveedor del Registro del sistema](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

