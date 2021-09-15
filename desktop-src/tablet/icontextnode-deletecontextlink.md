---
description: Elimina un objeto IContextLink de la colección de vínculos del objeto IContextNode.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: Método IContextNode::D eleteContextLink (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.DeleteContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac5676635bec961129078ed8689169d1a81cd87d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574489"
---
# <a name="icontextnodedeletecontextlink-method"></a>IContextNode::D eleteContextLink (método)

Elimina un objeto [**IContextLink**](icontextlink.md) de la colección de vínculos del objeto [**IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContextLinkToDelete* \[ En\]
</dt> <dd>

Objeto [**IContextLink que**](icontextlink.md) se eliminará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Un vínculo de contexto tiene un nodo de origen y un nodo de destino (vea [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) e [**IContextLink::GetDestinationNode).**](icontextlink-getdestinationnode.md) Este método quita [**IContextLink**](icontextlink.md) de la colección de vínculos de contexto de los nodos de origen y destino (vea [**IContextNode::GetContextLinks).**](icontextnode-getcontextlinks.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




