---
description: La propiedad Path del objeto SWbemLastError devuelve un objeto SWbemObjectPath que representa la ruta de acceso del objeto de \_ la clase o instancia actual. Esta propiedad se puede pasar como parámetro a métodos que requieren una ruta de acceso de objeto.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: SWbemLastError.Path_ propiedad (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5503d11d5c73f2bf955b25da9b5dbccbc18d41b9bc9b84bc3235993562938b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612205"
---
# <a name="swbemlasterrorpath_-property"></a>Propiedad SWbemLastError.Path \_

La **\_ propiedad Path** del objeto [**SWbemLastError**](swbemlasterror.md) devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa la ruta de acceso del objeto de la clase o instancia actual. Esta propiedad se puede pasar como parámetro a métodos que requieren una ruta de acceso de objeto.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Solo se puede modificar la propiedad [**Class**](swbemobjectpath-class.md) de [**la instancia de SWbemObjectPath**](swbemobjectpath.md) devuelta. Si intenta modificar cualquier otra propiedad o intenta llamar a los métodos [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton,**](swbemobjectpath-setassingleton.md) se produce un error de **wbemErrReadOnly**.

Por este problema, no se puede modificar el objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que es el valor de la propiedad [**Keys**](swbemobjectpath-keys.md) de la instancia [**de SWbemObjectPath devuelta.**](swbemobjectpath.md) Si intenta llamar a los [**métodos Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) en este valor, se produce un error **wbemErrReadOnly.** Además, no puede modificar ningún [**valor SWbemNamedValue**](swbemnamedvalue.md) obtenido de esta colección. Los intentos de modificar la [**propiedad Value**](swbemnamedvalue-value.md) devuelven el mismo código de error.

Sin embargo, si llama a [**SWbemObject.Clone \_**](swbemobject-clone-.md) para crear una copia, la propiedad [**Path \_**](swbemobject-path-.md) de la copia es totalmente modificable.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




