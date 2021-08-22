---
description: La propiedad Namespace del objeto SWbemObjectPath contiene el nombre del espacio de nombres que forma parte de la ruta de acceso del objeto.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath.Namespace (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9daa9b74918c16d58546f6830bb474e40e449a8c596f61f7e27f03342c47b4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503765"
---
# <a name="swbemobjectpathnamespace-property"></a>SWbemObjectPath.Namespace, propiedad

La **propiedad Namespace** del objeto [**SWbemObjectPath**](swbemobjectpath.md) contiene el nombre del espacio de nombres que forma parte de la ruta de acceso del objeto. Por ejemplo, la ruta de acceso siguiente muestra la propiedad namespace que devuelve la \\ raíz cimv2:

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

Para obtener la explicación de la sintaxis, [consulte Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo obtener el nombre del espacio de nombres de las instancias de [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que son discos duros. El script se conecta al espacio de nombres predeterminado.


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
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



 

