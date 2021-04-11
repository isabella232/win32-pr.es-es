---
description: Devuelve un objeto SWbemPropertySet que contiene la colección de propiedades del sistema WMI que se aplican al objeto.
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: SWbemObjectEx.Syspropiedad temProperties_ (Wbemdisp. h)
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
ms.openlocfilehash: cf8b7e15536c0d4e3116f0583662b3cd0b7d0887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278974"
---
# <a name="swbemobjectexsystemproperties_-property"></a>SWbemObjectEx.Sys\_ propiedad temProperties

La **propiedad \_ SystemProperties** del objeto [**SWbemObjectEx**](swbemobjectex.md) devuelve un objeto [**SWbemPropertySet**](swbempropertyset.md) que contiene la colección de [propiedades del sistema WMI](wmi-system-properties.md) que se aplican al objeto.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se recuperan los valores de propiedad para la clase de proceso de Win32 \_ .


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
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | \_ISWBEMOBJECTEX IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> </dl>

 

 




