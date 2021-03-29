---
description: La \_ propiedad path del objeto SWbemObject devuelve un objeto SWbemObjectPath que representa la ruta de acceso del objeto de la clase o la instancia actual. Esta propiedad se puede pasar como un parámetro a los métodos que requieren una ruta de acceso de objeto.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Path_ (Wbemdisp. h)
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
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277508"
---
# <a name="swbemobjectpath_-property"></a>SWbemObject. Path \_ (propiedad)

La **propiedad \_ path** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa la ruta de acceso del objeto de la clase o la instancia actual. Esta propiedad se puede pasar como un parámetro a los métodos que requieren una ruta de acceso de objeto.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Solo se puede modificar la propiedad de [**clase**](swbemobjectpath-class.md) de la instancia de [**SWbemObjectPath**](swbemobjectpath.md) devuelta. Si intenta modificar cualquier otra propiedad o intenta llamar a los métodos [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton**](swbemobjectpath-setassingleton.md), obtendrá un error **wbemErrReadOnly** .

Por este motivo, no se puede modificar el objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que es el valor de la propiedad [**Keys**](swbemobjectpath-keys.md) de la instancia de [**SWbemObjectPath**](swbemobjectpath.md) devuelta. Si intenta llamar a los métodos [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) en este valor, recibirá un error wbemErrReadOnly. Además, no se puede modificar ningún [**SWbemNamedValue**](swbemnamedvalue.md) Obtenido de esta colección. Los intentos de modificar la propiedad **Value** devuelven el mismo código de error.

Sin embargo, si llama a [**SWbemObject. \_ Clone**](swbemobject-clone-.md) para crear una copia, la propiedad [**SWbemObjectPath. Path**](swbemobjectpath-path.md) de la copia es totalmente modificable.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código, tomado de la [lista de todas las clases de WMI cimv2](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) en la galería de TechNet, usa la \_ propiedad path para enumerar todas las clases de WMI cimv2.


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
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



 

 




