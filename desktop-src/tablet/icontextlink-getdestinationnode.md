---
description: Recupera el objeto IContextNode que es el destino de este IContextLink.
ms.assetid: 7e185e69-821b-409b-bc58-d89a4aefeb23
title: 'IContextLink:: GetDestinationNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetDestinationNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 86d34bfcca39f7df9d9010e8dae32747ca8f1d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360344"
---
# <a name="icontextlinkgetdestinationnode-method"></a>IContextLink:: GetDestinationNode (método)

Recupera el objeto [**IContextNode**](icontextnode.md) que es el destino de este [**IContextLink**](icontextlink.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDestinationNode(
  [out] IContextNode **ppDstContextNodeId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDstContextNodeId* \[ enuncia\]
</dt> <dd>

Un puntero al objeto [**IContextNode**](icontextnode.md) que es el destino de este [**IContextLink**](icontextlink.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppDstContextNodeId* cuando ya no necesite usar el nodo de destino.

 

Si el objeto [**IContextLink**](icontextlink.md) se vincula entre un nodo que contiene escritura y un nodo que contiene dibujos, el nodo de destino es generalmente el nodo que contiene la escritura.

Si el objeto [**IContextLink**](icontextlink.md) tiene un tipo de vínculo de encloses (vea [**IContextLink:: GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md)), el nodo de destino es el objeto [**IContextNode**](icontextnode.md) que se incluye.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

