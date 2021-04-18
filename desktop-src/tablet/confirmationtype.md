---
description: Especifica el tipo de confirmación que se puede producir en un objeto IContextNode.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Enumeración ConfirmationType (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714960"
---
# <a name="confirmationtype-enumeration"></a>Enumeración ConfirmationType

Especifica el tipo de confirmación que se puede producir en un objeto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ ninguno**
</dt> <dd>

No se aplica ninguna confirmación. [**IInkAnalyzer**](iinkanalyzer.md) es libre de cambiar un nodo de contexto o cualquiera de sus descendientes según sea necesario.

</dd> <dt>

<span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) no puede cambiar el tipo ni ninguna propiedad del nodo de contexto especificado.

</dd> <dt>

<span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**Límite de ConfirmationType \_**
</dt> <dd>

El [**IInkAnalyzer**](iinkanalyzer.md) no realizará operaciones, incluida la adición de tinta o combinación con otros [**ContextNodes**](icontextnodes.md), lo que hace que el límite se mueva más allá del límite superior actual. Por ejemplo:

-   Una aplicación analiza un conjunto de entradas de lápiz y se identifica un ParagraphNode.
-   La aplicación confirma el límite de este párrafo.
-   El usuario de la aplicación escribe una nueva entrada de lápiz sobre el párrafo actual. Cuando se llama de nuevo a Analyze, la nueva entrada de lápiz no se incorporará en el nodo de párrafo confirmado.
-   Dado que solo se confirma el límite superior, el ContextNode puede seguir creciendo en otras direcciones. La eliminación de trazos puede hacer que el límite superior se desplace hacia abajo. La traducción de ContextNode puede hacer que la ubicación cambie, pero no permite la combinación de tinta adicional en la nueva ubicación.

Este ConfirmationType solo es aplicable a los nodos de párrafo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede usar el valor **NodeTypeAndProperties** solo para los nodos de dibujo de tinta y de lápiz (vea [**IContextNode:: GetType**](icontextnode-gettype.md)). De lo contrario, se devuelve un **E \_ INVALIDARG** de [**IContextNode:: CONFIRM**](icontextnode-confirm.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode:: CONFIRM**](icontextnode-confirm.md)
</dt> <dt>

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




