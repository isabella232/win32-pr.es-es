---
title: Error de dibujo D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Error al llamar a Draw de un destino de representación
keywords:
- Error de dibujo D1109 Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 09d84f549b2361d2753ac40650ce057de9e4f84c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549970"
---
# <a name="d1109-draw-failure"></a>D1109: Error de dibujo

Error al llamar a Draw de un recurso de destino de \[ *representación.* \] Etiquetas \[ *tag1,* *tag2* \] .

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Recursos*
</dt> <dd>

Dirección del destino de representación.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

Primer valor de etiqueta (vea [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) más para obtener información).

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

Segundo valor de etiqueta (vea [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) más para obtener información).

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nivel de error | Advertencia |



 

## <a name="possible-causes"></a>Causas posibles

Hay muchas razones por las que una llamada a Draw podría producir un error. Para obtener más información, consulte la documentación del SDK de Direct2D para el método que ha producido un error.

 

 