---
description: Especifica el tipo de confirmación que puede producirse en un objeto IContextNode.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Enumeración ConfirmationType (IACom.h)
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
ms.openlocfilehash: 9f89d5457e3d75bcf781a100449e4da9f8b45624af38760ca0cdda358fbf47ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936955"
---
# <a name="confirmationtype-enumeration"></a>ConfirmationType (enumeración)

Especifica el tipo de confirmación que puede producirse en un [**objeto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ None**
</dt> <dd>

No se aplica ninguna confirmación. [**IInkAnalyzer es libre**](iinkanalyzer.md) de cambiar un nodo de contexto o cualquiera de sus descendientes según sea necesario.

</dd> <dt>

<span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**
</dt> <dd>

[**IInkAnalyzer no**](iinkanalyzer.md) puede cambiar el tipo ni ninguna propiedad del nodo de contexto especificado.

</dd> <dt>

<span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType \_ TopBoundary**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) no realizará operaciones, incluida la adición de entrada de lápiz o la combinación con otros [**ContextNodes,**](icontextnodes.md)que hacen que TopBoundary se mueva más allá del límite superior actual. Por ejemplo:

-   Una aplicación analiza un conjunto de ink y se identifica paragraphnode.
-   La aplicación confirma el TopBoundary de este párrafo.
-   El usuario de la aplicación escribe nueva entrada de lápiz sobre el párrafo actual. Cuando se llama de nuevo a analyze, la nueva entrada manuscrita no se incorporará al nodo Párrafo confirmado.
-   Puesto que solo se confirma el límite superior, ContextNode puede seguir creciendo en otras direcciones. La eliminación de trazos puede hacer que el límite superior se mueva hacia abajo. La traducción de ContextNode puede hacer que la ubicación cambie, pero no permitirá que se combine más lápiz en la nueva ubicación.

ConfirmationType solo es aplicable a los nodos de párrafo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Solo puede usar el valor **NodeTypeAndProperties para** los nodos de dibujo de lápiz y de palabras manuscrita (vea [**IContextNode::GetType).**](icontextnode-gettype.md) De lo contrario, se devuelve **un \_ E INVALIDARG** desde [**IContextNode::Confirm**](icontextnode-confirm.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode::Confirm**](icontextnode-confirm.md)
</dt> <dt>

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




