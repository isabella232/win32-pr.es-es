---
description: El modo de dirección de textura de abrazadera, identificado por el \_ miembro D3DTADDRESS clamp del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D Sujete las coordenadas de textura al \[ intervalo 0,0, 1,0 \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Modo de dirección de textura de abrazadera (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153ed1f044bacaec6b87420eb7df22a2557349a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714878"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a>Modo de dirección de textura de abrazadera (Direct3D 9)

El modo de dirección de textura de abrazadera, identificado por el \_ miembro D3DTADDRESS clamp del tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , hace que Direct3D Sujete las coordenadas de textura al \[ intervalo 0,0, 1,0 \] . Es decir, aplica la textura una vez y después difumina el color de los píxeles del borde. Por ejemplo, supongamos que la aplicación crea un primitivo cuadrado y asigna coordenadas de textura de (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) y (3,0, 0,0) a los vértices del primitivo. Al establecer el modo de direccionamiento de textura en D3DTADDRESS \_ Clamp, la textura se aplica una vez. Los colores de píxeles en la parte superior de las columnas y el final de las filas se extienden a la parte superior y derecha de la primitiva, respectivamente.

En la ilustración siguiente se muestra una textura fija.

![Ilustración de una textura y una textura fija](images/clamp.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos de direccionamiento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
