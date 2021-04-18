---
description: La propiedad Methods \_ del objeto SWbemObject devuelve un objeto SWbemMethodSet que es una colección de los métodos de la clase o la instancia actual. Esta propiedad es de solo lectura.
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Methods_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6a702f0acf0736810de4d3176f8695fa8008d3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707087"
---
# <a name="swbemobjectmethods_-property"></a>Propiedad SWbemObject. Methods \_

La **propiedad \_ Methods** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemMethodSet**](swbemmethodset.md) que es una colección de los métodos de la clase o la instancia actual. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="examples"></a>Ejemplos

En el siguiente [ejemplo de código](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), tomado de la galería de TechNet, se describe cómo enumerar todos los métodos de una clase.


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
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



 

 




