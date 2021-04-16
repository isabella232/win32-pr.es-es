---
description: La propiedad parameters del objeto SWbemMethod es un objeto SWbemObject cuyas propiedades definen los parámetros de entrada para este método.
ms.assetid: fba1bb97-29f9-41d3-8ecc-f283989118c1
ms.tgt_platform: multiple
title: Propiedad SWbemMethod. Parameters (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.InParameters
- ISWbemMethod.InParameters
- ISWbemMethod.get_InParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c8df897f876673f6b4afe875e718401ae4c217e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696797"
---
# <a name="swbemmethodinparameters-property"></a>SWbemMethod. Parameters (propiedad)

La propiedad **Parameters** del objeto [**SWbemMethod**](swbemmethod.md) es un objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros de entrada para este método. Esta propiedad es de solo lectura. Tenga en cuenta que los cambios que se realicen en este objeto no se reflejarán en la definición del método subyacente.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemMethod.InParameters As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | \_ISWBEMMETHOD IID<br/>                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




