---
description: Use la propiedad Count del objeto SWbemObjectSet para determinar cuántos elementos hay en una colección SWbemObjectSet. Esta propiedad es de solo lectura.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Propiedad SWbemObjectSet.Count (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1305cc0119f002f8ac3229664227d5c21bea9d865eedb0a31fcb7eb77250424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857235"
---
# <a name="swbemobjectsetcount-property"></a>SWbemObjectSet.Count, propiedad

Use la **propiedad Count** del [**objeto SWbemObjectSet**](swbemobjectset.md) para determinar cuántos elementos hay en una **colección SWbemObjectSet.** Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Una cuestión que debe tener cuidado al usar Count es que WMI no mantiene un recuento en ejecución del número de elementos de una colección. Si solicita Count para una colección, WMI no puede responder al instante con un número; en su lugar, debe contar literalmente los elementos, enumerando toda la colección. Para una colección que tiene relativamente pocos elementos, como servicios, esta enumeración probablemente tarda menos de un segundo. Sin embargo, contar el número de eventos de una colección de registros de eventos puede tardar bastante más tiempo.

Y, a continuación, supongamos que desea mostrar los valores de propiedad para cada evento de la colección. Si es así, WMI tendrá que enumerar toda la colección una segunda vez.

> [!Note]  
> Si intenta obtener esta propiedad de un objeto [**SWbemObjectSet**](swbemobjectset.md) que se devuelve de un método donde las marcas especificadas se incluyen en la marca wbemFlagForwardOnly, recibirá un error wbemErrFailed.

 

## <a name="examples"></a>Ejemplos

En su mayor parte, lo único que hará con un SWbemObjectSet es enumerar todos los objetos contenidos dentro de la propia colección. Sin embargo, el recuento puede ser útil en el scripting de administración del sistema. Como su nombre indica, Count indica el número de elementos de la colección. Por ejemplo, este script recupera una colección de todos los servicios instalados en un equipo y, a continuación, refleja el número total de servicios encontrados:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



Lo que hace que Count sea útil es que puede saber si una instancia específica está disponible en un equipo. Por ejemplo, este script recupera una colección de todos los servicios de un equipo que tienen el nombre W3SVC. Si count es 0 (y es válido para que las colecciones no tengan instancias), significa que el servicio W3SVC no está instalado en el equipo.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




