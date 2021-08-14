---
description: La propiedad Relpath del objeto SWbemObjectPath contiene la ruta de acceso relativa de la ruta de acceso completa.
ms.assetid: 9a4363ae-b6b3-4e8c-a7ca-a9e48c28e19b
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath.Relpath (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Relpath
- ISWbemObjectPath.Relpath
- ISWbemObjectPath.get_Relpath
- ISWbemObjectPath.put_Relpath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4cb3cae6a6c5de5c955bb719880cd8b4be49208a8dc0c1fa3f85c0da5ff74a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313708"
---
# <a name="swbemobjectpathrelpath-property"></a>Propiedad SWbemObjectPath.Relpath

La **propiedad Relpath** del objeto [**SWbemObjectPath**](swbemobjectpath.md) contiene la ruta de acceso relativa de la ruta de acceso completa.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Relpath As String
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se muestra la diferencia entre los datos obtenidos de [**\_ SWbemObject.Path**](swbemobject-path-.md) y **SWbemObjectPath.Relpath**.


```VB
set objWMIService = GetObject ("winmgmts:root/cimv2")

set Processes = objWMIService.ExecQuery( _
    "Select * from win32_process")

For Each Process in Processes
 WScript.Echo Process.Path_ 
 WScript.Echo Process.Path_.Relpath
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

 




