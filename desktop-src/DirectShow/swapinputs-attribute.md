---
description: El atributo swapinputs especifica si se deben intercambiar las entradas de la transición. Si el valor es TRUE, se intercambian las entradas. El valor predeterminado es FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Atributo swapinputs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361412"
---
# <a name="swapinputs-attribute"></a>Atributo swapinputs

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `swapinputs` atributo especifica si se deben intercambiar las entradas de la transición. Si el valor es **true**, se intercambian las entradas. El valor predeterminado es **FALSE**.

## <a name="possible-values"></a>Valores posibles

Los siguientes valores se definen como TRUE: y, Y, t, T, 1. Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).

## <a name="applies-to"></a>Se aplica a

[**transitorio**](transition-element.md)

## <a name="remarks"></a>Observaciones

De forma predeterminada, una transición continúa desde el compuesto de todas las capas de prioridad más baja hasta la capa en la que reside la transición. Si el `swapinputs` atributo es 1, esta dirección se invierte. Para obtener más información sobre el modelo de capas que usa DES, vea [el modelo Timeline](the-timeline-model.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



