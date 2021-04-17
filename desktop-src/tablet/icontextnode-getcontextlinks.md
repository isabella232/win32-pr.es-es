---
description: Recupera una colección de objetos IContextLink que representa relaciones con otros objetos IContextNode.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: 'IContextNode:: GetContextLinks (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de62550a09d0a538ddc680f6d57c35a1016fe255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652435"
---
# <a name="icontextnodegetcontextlinks-method"></a>IContextNode:: GetContextLinks (método)

Recupera una colección de objetos [**IContextLink**](icontextlink.md) que representa relaciones con otros objetos [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppContextLinks* \[ enuncia\]
</dt> <dd>

Puntero a una colección de objetos [**IContextLink**](icontextlink.md) que representa relaciones con otros objetos [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextLinks* cuando ya no necesite usar la colección de vínculos de contexto.

 

Para obtener información sobre las relaciones entre los nodos primarios y secundarios, use [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) o [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md).

Para obtener más información sobre los tipos de relaciones que se describen en los vínculos, vea [**IContextLink**](icontextlink.md) y [**ContextLinkDirection**](contextlinkdirection.md).

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

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

