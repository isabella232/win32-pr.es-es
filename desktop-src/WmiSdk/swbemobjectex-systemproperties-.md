---
description: Devuelve un objeto SWbemPropertySet que contiene la colección de propiedades del sistema WMI que se aplican al objeto .
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: SWbemObjectEx.SystemProperties_ propiedad (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 23de364e4616b7b7c2ac6b7de6daaf42edfd73e2e7b3920f7ac3b84b7a59bde5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857335"
---
# <a name="swbemobjectexsystemproperties_-property"></a>SWbemObjectEx.Syspropiedad temProperties \_

La **propiedad \_ SystemProperties** del objeto [**SWbemObjectEx**](swbemobjectex.md) devuelve un objeto [**SWbemPropertySet**](swbempropertyset.md) que contiene la colección de propiedades del sistema [WMI](wmi-system-properties.md) que se aplican al objeto .

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se recuperan los valores de propiedad de la clase \_ Process de Win32.


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

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
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> </dl>

 

 




