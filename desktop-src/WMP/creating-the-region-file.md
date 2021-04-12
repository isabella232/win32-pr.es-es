---
title: Crear el archivo de región
description: Crear el archivo de región
ms.assetid: e901dfa1-1e06-4136-b877-64be03107f6f
keywords:
- Aspectos móviles de Windows Media Player, archivos de regiones
- máscaras, archivos de regiones
- crear máscaras, archivos de regiones
- Archivos de regiones en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf3268b101255191bef4b3e4c4880e2bb846414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356781"
---
# <a name="creating-the-region-file"></a>Crear el archivo de región

Querrá crear un archivo de región que muestre qué áreas responden a los grifos. Simplemente puede copiar los niveles base de cada elemento en una nueva capa y colorearlos para que se correspondan con los números de color que utilizará en el archivo de definición de máscara. Asegúrese de que las imágenes que crea en esta capa son sólidas y que no se aplica ningún efecto. Probablemente querrá anotar los números de color de cada imagen. Puede obtener los números de color del selector de colores de Photoshop. Desea los números RGB, que son tres números decimales. Cada número oscila entre 0 y 255. Por ejemplo, un rojo sólido sería 255, 0,0.

> [!Note]  
> Los archivos de región no se usan en las máscaras móviles de Windows Media Player 10 porque los tipos de botón no se admiten en Windows Media Player 10 Mobile o posterior.

 

La siguiente imagen es el archivo de región.

![archivo de región](images/ceswmreg.png)

Solo hay cuatro imágenes en este archivo porque solo los botones PlayPause, detener, siguiente y anterior son botones de tipo de posicionamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear el arte**](creating-the-art.md)
</dt> </dl>

 

 




