---
description: Recupera una colección de objetos IContextLink que representa las relaciones con otros objetos IContextNode.
ms.assetid: 0fe56e6d-c779-4916-9c80-6f18cf6f1b09
title: Método IContextNode::GetContextLinks (IACom.h)
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
ms.openlocfilehash: 2c3b63e50cf43f06f6065a61dacfbbbd8a00fe7959bb5133407a6c2a980a1a20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057845"
---
# <a name="icontextnodegetcontextlinks-method"></a>IContextNode::GetContextLinks (método)

Recupera una colección de objetos [**IContextLink**](icontextlink.md) que representa las relaciones con otros [**objetos IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetContextLinks(
  [out] IContextLinks **ppContextLinks
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppContextLinks* \[ out\]
</dt> <dd>

Puntero a una colección de [**objetos IContextLink**](icontextlink.md) que representa las relaciones con otros [**objetos IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppContextLinks* cuando ya no necesite usar la colección de vínculos de contexto.

 

Para obtener información sobre las relaciones de nodo primario o secundario, use [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) o [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md).

Para obtener más información sobre los tipos de relaciones que se describen mediante vínculos, vea [**IContextLink**](icontextlink.md) y [**ContextLinkDirection**](contextlinkdirection.md).

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[**IContextNode::AddContextLink**](icontextnode-addcontextlink.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

