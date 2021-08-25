---
description: La propiedad Properties del objeto SWbemObject devuelve un objeto SWbemPropertySet que es una colección de las propiedades de la clase o instancia \_ actual. Esta propiedad es de solo lectura.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: SWbemObject.Properties_ propiedad (Wbemdisp.h)
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
ms.openlocfilehash: 413e13b725fce117b9358a254a860c631fc5fbe3158bf7f6d277ebca22647168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857315"
---
# <a name="swbemobjectproperties_-property"></a>Propiedad SWbemObject.Properties \_

La **\_ propiedad Properties** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemPropertySet**](swbempropertyset.md) que es una colección de las propiedades de la clase o instancia actual. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

El ejemplo de código generar scripts de clase WMI de [PowerShell](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) en la Galería de TechNet usa la propiedad Propiedades para generar un script para cada una de las clases WMI que enumerarán el nombre de clase WMI y las \_ propiedades.

En el código siguiente, tomado del ejemplo de código [VBScript](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) Enumera todas las propiedades de una clase WMI en la Galería de TechNet, se enumeran las propiedades de una clase WMI especificada.


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



 

 




