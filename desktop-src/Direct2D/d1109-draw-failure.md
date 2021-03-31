---
title: Error de D1109 Draw
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Error en una llamada a Draw por un destino de representación
keywords:
- Error de D1109 Draw Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793708"
---
# <a name="d1109-draw-failure"></a>D1109: error de dibujo

Una llamada a Draw de un recurso de destino de representación produjo un error \[  \] . Tags \[ *TAG1*, *etiqueta2* \] .

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*recurso*
</dt> <dd>

Dirección del destino de representación.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

El primer valor de etiqueta (vea [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obtener más información).

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*etiqueta2*
</dt> <dd>

El segundo valor de etiqueta (consulte [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obtener más información).

</dd> </dl> 

|             |         |
|-------------|---------|
| Nivel de error | Advertencia |



 

## <a name="possible-causes"></a>Causas posibles

Hay muchas razones por las que se puede producir un error en una llamada a Draw. Para obtener más información, consulte la documentación del SDK de Direct2D para el método en el que se produjo el error.

 

 