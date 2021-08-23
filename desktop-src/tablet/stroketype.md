---
description: Indica si un trazo se debe analizar como parte de un dibujo o como parte de la escritura.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Enumeración StrokeType (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 4b02a05582d675f04ad4458b1cb21c6d4a1797bacf15baf5d0851804d1a95d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589585"
---
# <a name="stroketype-enumeration"></a>StrokeType (enumeración)

Indica si un trazo se debe analizar como parte de un dibujo o como parte de la escritura.

## <a name="syntax"></a>Syntax


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType \_ Sin clasificar**
</dt> <dd>

El trazo puede ser parte de un dibujo o parte de la escritura.

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Escritura \_ de StrokeType**
</dt> <dd>

El trazo forma parte de la escritura.

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**Dibujo \_ de StrokeType**
</dt> <dd>

El trazo forma parte de un dibujo.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra parte de un controlador de eventos de trazo, implementado de forma similar al ejemplo de [receptores de eventos de C++.](c---event-sinks-sample.md) El trazo agregado se comprueba para ver si la parte superior de su rectángulo delimitador se ha dibujado debajo de un margen, `drawingMargin` . Si es así, el [**objeto IInkAnalyzer,**](iinkanalyzer.md) , se establece para analizar el trazo como un trazo de dibujo, en lugar de como `m_spInkAnalyzer` un trazo de escritura a mano. `CheckHResult` es una función que toma y una cadena, y produce una excepción creada con la `HRESULT` cadena si no es `HRESULT` **SUCCESS**.


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer::SetStrokeType (Método)**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




