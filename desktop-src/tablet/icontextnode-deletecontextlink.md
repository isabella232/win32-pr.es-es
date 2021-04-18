---
description: Elimina un objeto IContextLink de la colección de vínculos del objeto IContextNode.
ms.assetid: c4a69a74-30d6-4099-a02a-13c8a2e52bc7
title: IContextNode::D método eleteContextLink (IACom. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715231"
---
# <a name="icontextnodedeletecontextlink-method"></a>IContextNode::D método eleteContextLink

Elimina un objeto [**IContextLink**](icontextlink.md) de la colección de vínculos del objeto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeleteContextLink(
  [in] IContextLink *pContextLinkToDelete
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContextLinkToDelete* \[ de\]
</dt> <dd>

Objeto [**IContextLink**](icontextlink.md) que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Un vínculo de contexto tiene un nodo de origen y un nodo de destino (vea [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md) y [**IContextLink:: GetDestinationNode**](icontextlink-getdestinationnode.md)). Este método quita el [**IContextLink**](icontextlink.md) de la colección de los nodos de origen y de destino de los vínculos de contexto (vea [**IContextNode:: GetContextLinks**](icontextnode-getcontextlinks.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




