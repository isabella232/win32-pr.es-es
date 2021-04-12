---
description: Vista previa de efectos y transiciones
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Vista previa de efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152522"
---
# <a name="previewing-effects-and-transitions"></a>Vista previa de efectos y transiciones

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Algunos efectos y transiciones tardan mucho tiempo en representarse. Durante la versión preliminar, esto puede hacer que el vídeo sea entrecortado o no sincronizado con el audio. Puede aumentar la velocidad de la versión preliminar deshabilitando los efectos o las transiciones:

-   Para deshabilitar todos los efectos, llame a [**IAMTimeline:: EnableEffects**](iamtimeline-enableeffects.md).
-   Para deshabilitar todas las transiciones, llame a [**IAMTimeline:: EnableTransitions**](iamtimeline-enabletransitions.md).
-   Para deshabilitar una transición determinada, llame a [**IAMTimelineTrans:: SetCutsOnly**](iamtimelinetrans-setcutsonly.md).

Cuando se deshabilitan los efectos, no se representan durante la vista previa. Cuando se deshabilita una transición, se representa como un corte de salto. Todavía se produce el segue entre pistas, pero el efecto visual no se representa.

Si no se puede representar un efecto o una transición, el motor de representación sustituye a un efecto o transición predeterminados. Llame al método [**IAMTimeline:: SetDefaultEffect**](iamtimeline-setdefaulteffect.md) para establecer el efecto predeterminado y el método [**IAMTimeline:: SetDefaultTransition**](iamtimeline-setdefaulttransition.md) para establecer la transición predeterminada. Si no especifica un valor predeterminado, o si el que especifica también produce un error, DES utiliza su propio valor predeterminado.

> [!Note]  
> También puede mejorar la calidad de la vista previa aumentando la cantidad de almacenamiento en búfer de fotogramas. Vea [**IAMTimelineGroup:: SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



