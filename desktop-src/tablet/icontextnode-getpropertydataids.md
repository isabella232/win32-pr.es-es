---
description: Recupera los identificadores para los que hay datos de propiedad.
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: Método IContextNode::GetPropertyDataIds (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94aab2b91a5da9588de65f5a48bf496bdceae71bf4aa90f82f3969cbe6a9e76e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935375"
---
# <a name="icontextnodegetpropertydataids-method"></a>IContextNode::GetPropertyDataIds (método)

Recupera los identificadores para los que hay datos de propiedad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulGuidCount* \[ out\]
</dt> <dd>

Número de propiedades.

</dd> <dt>

*ppGuids* \[ out\]
</dt> <dd>

Identificadores para los que hay datos de propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppGuids* cuando ya no necesite la información.

 

Este método devuelve los identificadores específicos de la aplicación para los datos de propiedad que se han agregado. También devuelve los identificadores de los datos de propiedad internos, que se describen mediante las constantes [Propiedades del nodo](context-node-properties.md) de contexto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

