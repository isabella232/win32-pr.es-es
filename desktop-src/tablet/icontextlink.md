---
description: Representa una relación entre dos objetos IContextNode.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Interfaz IContextLink (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7dc9244fed59604a56817f15801de94b64c476762e186cc6f7c36186e8d0b26d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719919"
---
# <a name="icontextlink-interface"></a>Interfaz IContextLink

Representa una relación entre dos [**objetos IContextNode.**](icontextnode.md)

## <a name="members"></a>Miembros

La **interfaz IContextLink** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextLink también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IContextLink** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetContextLinkDirection**](icontextlink-getcontextlinkdirection.md) | Recupera el tipo de relación que **representa este IContextLink.**<br/>                                         |
| [**GetDestinationNode**](icontextlink-getdestinationnode.md)           | Recupera el [**objeto IContextNode**](icontextnode.md) que es el destino de **este objeto IContextLink.**<br/> |
| [**GetSourceNode**](icontextlink-getsourcenode.md)                     | Recupera el [**objeto IContextNode**](icontextnode.md) que es el origen de **este objeto IContextLink.**<br/>      |



 

## <a name="remarks"></a>Observaciones

A continuación se muestra un ejemplo de una relación representada por un **objeto IContextLink:**

-   Cuando se usa un nodo AnalysisHint en el análisis de entrada de lápiz, la operación de análisis de entrada de lápiz crea un objeto **IContextLink** de tipo AnalysisHint entre el nodo de sugerencia de análisis y el nodo que contiene escritura dentro del área de la sugerencia. El nodo de origen es el nodo de sugerencia de análisis y el nodo de destino es el nodo que contiene escritura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> </dl>

 

