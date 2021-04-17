---
description: La \_ propiedad Properties del objeto SWbemObject devuelve un objeto SWbemPropertySet que es una colección de las propiedades de la clase o la instancia actual. Esta propiedad es de solo lectura.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Properties_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b215abb7a0ca466c8a93fe20f20518f8d7b2ec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706051"
---
# <a name="swbemobjectproperties_-property"></a>Propiedad SWbemObject. Properties \_

La **propiedad \_ Properties** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemPropertySet**](swbempropertyset.md) que es una colección de las propiedades de la clase o la instancia actual. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

El ejemplo de código de PowerShell [generar scripts de clase WMI de PowerShell](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) en la galería de TechNet usa la \_ propiedad Properties para generar un script para cada una de las clases WMI que mostrarán el nombre de la clase WMI y las propiedades.

En el código siguiente, tomado de la [lista todas las propiedades de un ejemplo de código de VBScript de clase WMI](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) en la galería de TechNet, se enumeran las propiedades de una clase WMI especificada.


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
Next 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



 

 




