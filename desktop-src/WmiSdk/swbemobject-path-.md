---
description: La propiedad Path del objeto SWbemObject devuelve un objeto SWbemObjectPath que representa la ruta de acceso del objeto \_ de la clase o instancia actual. Esta propiedad se puede pasar como un parámetro a los métodos que requieren una ruta de acceso de objeto.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: SWbemObject.Path_ propiedad (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b87d2ad73fcaea2be2214a962940f154bb6df2b428f98d4646e0cb935ab2859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991995"
---
# <a name="swbemobjectpath_-property"></a>SWbemObject.Path, propiedad \_

La **\_ propiedad Path** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa la ruta de acceso del objeto de la clase o instancia actual. Esta propiedad se puede pasar como un parámetro a los métodos que requieren una ruta de acceso de objeto.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Solo se puede modificar la propiedad [**Class**](swbemobjectpath-class.md) de la [**instancia de SWbemObjectPath**](swbemobjectpath.md) devuelta. Si intenta modificar cualquier otra propiedad o intenta llamar a los métodos [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton,**](swbemobjectpath-setassingleton.md)recibirá un error **wbemErrReadOnly.**

Por este problema, no se puede modificar el objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que es el valor de la propiedad [**Keys**](swbemobjectpath-keys.md) de la instancia [**de SWbemObjectPath devuelta.**](swbemobjectpath.md) Si intenta llamar a los métodos [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) en este valor, recibirá un error wbemErrReadOnly. Además, no puede modificar ningún [**valor SWbemNamedValue**](swbemnamedvalue.md) obtenido de esta colección. Los intentos de modificar **la propiedad Value** devuelven el mismo código de error.

Sin embargo, si llama a [**\_ SWbemObject.Clone**](swbemobject-clone-.md) para crear una copia, la propiedad [**SWbemObjectPath.Path**](swbemobjectpath-path.md) de la copia es totalmente modificable.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente, tomado de Enumerar todas las clases [cimV2](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) de WMI en la Galería de TechNet, se usa la propiedad Path para enumerar todas las \_ clases cimV2 de WMI.


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
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



 

 




