---
description: Vista previa de efectos y transiciones
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Vista previa de efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254199"
---
# <a name="previewing-effects-and-transitions"></a>Vista previa de efectos y transiciones

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Algunos efectos y transiciones llevan un tiempo relativamente largo de representación. Durante la versión preliminar, esto puede provocar que el vídeo se vuelva desa sincronizar con el audio. Puede aumentar la velocidad de vista previa deshabilitando efectos o transiciones:

-   Para deshabilitar todos los efectos, llame [**a IAMTimeline::EnableEffects**](iamtimeline-enableeffects.md).
-   Para deshabilitar todas las transiciones, llame [**a IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md).
-   Para deshabilitar una transición determinada, llame a [**IAMTimelineTrans::SetCutsOnly.**](iamtimelinetrans-setcutsonly.md)

Cuando los efectos están deshabilitados, no se representan durante la versión preliminar. Cuando se deshabilita una transición, se representa como un salto. El segue entre pistas todavía se produce, pero el efecto visual no se representa.

Si no se puede representar un efecto o una transición, el motor de representación sustituye un efecto o transición predeterminados. Llame al [**método IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md) para establecer el efecto predeterminado y al método [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md) para establecer la transición predeterminada. Si no especifica un valor predeterminado o si el especificado también produce un error, DES usa su propio valor predeterminado.

> [!Note]  
> También puede mejorar la calidad de la vista previa si aumenta la cantidad de almacenamiento en búfer de fotogramas. Vea [**IAMTimelineGroup::SetOutputBuffering.**](iamtimelinegroup-setoutputbuffering.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



