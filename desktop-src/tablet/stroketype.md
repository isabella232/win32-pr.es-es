---
description: Indica si se debe analizar un trazo como parte de un dibujo o como parte de la escritura.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Enumeración StrokeType (IACom. h)
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
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278006"
---
# <a name="stroketype-enumeration"></a>Enumeración StrokeType

Indica si se debe analizar un trazo como parte de un dibujo o como parte de la escritura.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType sin \_ clasificar**
</dt> <dd>

El trazo puede formar parte de un dibujo o de una parte de la escritura.

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Escritura de StrokeType \_**
</dt> <dd>

El trazo forma parte de la escritura.

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**Dibujo de StrokeType \_**
</dt> <dd>

El trazo forma parte de un dibujo.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra parte de un controlador de eventos de trazo, implementado de manera similar al [ejemplo de receptores de eventos de C++](c---event-sinks-sample.md). El trazo agregado se comprueba para ver si la parte superior de su cuadro de límite se ha dibujado debajo de un margen `drawingMargin` . Si es así, el objeto [**IInkAnalyzer**](iinkanalyzer.md) , `m_spInkAnalyzer` , se establece para analizar el trazo como un trazo de dibujo, en lugar de como un trazo de escritura a mano. `CheckHResult` es una función que toma un `HRESULT` y una cadena, y produce una excepción creada con la cadena si el `HRESULT` no es **correcto**.


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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalyzer:: SetStrokeType (método)**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




