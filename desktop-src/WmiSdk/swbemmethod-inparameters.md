---
description: La propiedad InParameters del objeto SWbemMethod es un objeto SWbemObject cuyas propiedades definen los parámetros de entrada para este método.
ms.assetid: fba1bb97-29f9-41d3-8ecc-f283989118c1
ms.tgt_platform: multiple
title: Propiedad SWbemMethod.InParameters (Wbemdisp.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359397"
---
# <a name="swbemmethodinparameters-property"></a>SWbemMethod.InParameters, propiedad

La **propiedad InParameters** del objeto [**SWbemMethod**](swbemmethod.md) es un objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros de entrada para este método. Esta propiedad es de solo lectura. Tenga en cuenta que los cambios realizados en este objeto no se reflejan en la definición del método subyacente.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemMethod.InParameters As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Para obtener más información, vea [Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemMethod<br/>                                                            |



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

 

 




