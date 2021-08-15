---
description: La propiedad OutParameters del objeto SWbemMethod es un objeto SWbemObject cuyas propiedades definen los parámetros out y el tipo de valor devuelto de este método. Esta propiedad es de solo lectura.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: Propiedad SWbemMethod.OutParameters (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5dec1b2fe18dae65443b45ee6c1d2efcd1d924a72eb2817869c35406ebbc7808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314426"
---
# <a name="swbemmethodoutparameters-property"></a>Propiedad SWbemMethod.OutParameters

La **propiedad OutParameters** del objeto [**SWbemMethod**](swbemmethod.md) es un objeto [**SWbemObject**](swbemobject.md) cuyas propiedades definen los parámetros out y el tipo de valor devuelto de este método. Esta propiedad es de solo lectura.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

Para obtener más información sobre cómo usar esta propiedad para obtener parámetros de salida de métodos de proveedor, vea Construir objetos [InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Tenga en cuenta que los cambios realizados en este objeto no se reflejan en la definición del método subyacente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemMethod<br/>                                                            |



## <a name="see-also"></a>Consulte también

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

 

 




