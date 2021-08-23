---
description: El atributo swapinputs especifica si se intercambian las entradas de transición. Si el valor es TRUE, se intercambian las entradas. El valor predeterminado es FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: atributo swapinputs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b74d16d9b195f504188f4684cf234a5b0c7627274c6e74d57e6824df20a0c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951714"
---
# <a name="swapinputs-attribute"></a>atributo swapinputs

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `swapinputs` atributo especifica si se intercambian las entradas de transición. Si el valor es **TRUE**, se intercambian las entradas. El valor predeterminado es **FALSE**.

## <a name="possible-values"></a>Valores posibles

Los valores siguientes se definen como TRUE: y, Y, t, T, 1. Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).

## <a name="applies-to"></a>Se aplica a

[**Transición**](transition-element.md)

## <a name="remarks"></a>Comentarios

De forma predeterminada, una transición pasa de la composición de todas las capas de prioridad inferior a la capa en la que reside la transición. Si el `swapinputs` atributo es 1, se invierte esta dirección. Para obtener más información sobre el modelo de capas usado por DES, vea [El modelo de escala de tiempo](the-timeline-model.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



