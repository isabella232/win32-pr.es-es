---
description: La \_ propiedad path del objeto SWbemLastError devuelve un objeto SWbemObjectPath que representa la ruta de acceso del objeto de la clase o la instancia actual. Esta propiedad se puede pasar como un parámetro a los métodos que requieren una ruta de acceso de objeto.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: Propiedad SWbemLastError.Path_ (Wbemdisp. h)
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
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082864"
---
# <a name="swbemlasterrorpath_-property"></a>SWbemLastError. Path \_ (propiedad)

La **propiedad \_ path** del objeto [**SWbemLastError**](swbemlasterror.md) devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa la ruta de acceso del objeto de la clase o la instancia actual. Esta propiedad se puede pasar como un parámetro a los métodos que requieren una ruta de acceso de objeto.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Solo se puede modificar la propiedad de [**clase**](swbemobjectpath-class.md) de la instancia de [**SWbemObjectPath**](swbemobjectpath.md) devuelta. Si intenta modificar cualquier otra propiedad o intenta llamar a los métodos [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton**](swbemobjectpath-setassingleton.md) , obtendrá un error de **wbemErrReadOnly**.

Por este motivo, no se puede modificar el objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que es el valor de la propiedad [**Keys**](swbemobjectpath-keys.md) de la instancia de [**SWbemObjectPath**](swbemobjectpath.md) devuelta. Si intenta llamar a los métodos [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) en este valor, obtendrá un error **wbemErrReadOnly** . Además, no se puede modificar ningún [**SWbemNamedValue**](swbemnamedvalue.md) Obtenido de esta colección. Los intentos de modificar la propiedad [**Value**](swbemnamedvalue-value.md) devuelven el mismo código de error.

Sin embargo, si llama a [**SWbemObject. \_ Clone**](swbemobject-clone-.md) para crear una copia, la propiedad [**\_ path**](swbemobject-path-.md) de la copia es totalmente modificable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | \_ISWBEMLASTERROR IID<br/>                                                         |



 

 




