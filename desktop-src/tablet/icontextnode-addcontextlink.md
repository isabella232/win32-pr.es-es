---
description: Agrega un nuevo IContextLink a la colección del objeto IContextNode de vínculos de contexto.
ms.assetid: b7b9da10-3015-4976-bc4e-1a7f69b7c85b
title: 'IContextNode:: AddContextLink (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eccfcc8be51ff951c1bcd6de55bd3a0f89cdc201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652438"
---
# <a name="icontextnodeaddcontextlink-method"></a>IContextNode:: AddContextLink (método)

Agrega un nuevo [**IContextLink**](icontextlink.md) a la colección del objeto [**IContextNode**](icontextnode.md) de vínculos de contexto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddContextLink(
  [in]  IContextNode         *pDestinationNode,
  [in]  ContextLinkDirection linkDirection,
  [out] IContextLink         **ppContextLinkToAdd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestinationNode* \[ de\]
</dt> <dd>

[**IContextNode**](icontextnode.md) de destino para el nuevo [**IContextLink**](icontextlink.md).

</dd> <dt>

*linkDirection* \[ de\]
</dt> <dd>

Dirección del objeto [**IContextLink**](icontextlink.md) que se va a crear.

</dd> <dt>

*ppContextLinkToAdd* \[ enuncia\]
</dt> <dd>

Puntero al nuevo objeto [**IContextLink**](icontextlink.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextLinkToAdd* cuando ya no necesite usar el nodo de contexto.

 

Este objeto [**IContextNode**](icontextnode.md) es el nodo de origen (vea [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md)) para el nuevo objeto [**IContextLink**](icontextlink.md) .

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

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::D eleteContextLink**](icontextnode-deletecontextlink.md)
</dt> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

