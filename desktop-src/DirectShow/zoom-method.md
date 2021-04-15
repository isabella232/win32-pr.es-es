---
description: El método de zoom amplía el vídeo mostrado hacia arriba o hacia afuera, centrado en un conjunto determinado de coordenadas de pantalla.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoom (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497981"
---
# <a name="zoom-method"></a>Zoom (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `Zoom` método amplía el vídeo mostrado hacia arriba o hacia afuera, centrado en un conjunto determinado de coordenadas de pantalla.

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*
</dt> <dd>

Especifica la coordenada x en el centro del área de zoom rectangular como un entero.

</dd> <dt>

<span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*
</dt> <dd>

Especifica la coordenada y en el centro del rectángulo que se va a ampliar como un entero.

</dd> <dt>

<span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*
</dt> <dd>

Especifica el factor de ampliación que se aplica al valor de zoom actual como un entero. El valor máximo total depende de lo que admita la superposición de hardware; suele ser un factor de 32 a 64 veces el tamaño original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La nueva relación de zoom permanece en vigor hasta que se restaura al tamaño original o se cambia de nuevo. En otras palabras, dos llamadas a este método que especifican un *iZoomRatio* de dos darán lugar a una relación de zoom cuatro veces mayor que el tamaño del vídeo original. Si el usuario intenta hacer zoom más allá de lo que el hardware puede admitir, este método se realizará correctamente, pero no hará nada.

El método [**SetClipVideoRect**](setclipvideorect-method.md) es otra manera de hacer zoom; la única diferencia entre los dos métodos es la forma en que se especifica el rectángulo de zoom.

 

 



