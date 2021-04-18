---
description: Transición de compositor
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Transición de compositor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104556999"
---
# <a name="compositor-transition"></a>Transición de compositor

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La transición de compositor compone un subrectángulo desde el primer plano en un rectángulo designado en el fondo, sin alterar el resto del fondo. Use esta transición para crear efectos de pantalla dividida o imagen en imagen.

La siguiente imagen muestra la transición de compositor:

![transición de compositor](images/trans-compositor.png)

IDENTIFICADOR de clase (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}

Nombre de la variable CLSID: CLSID \_ DxtCompositor

Nombre descriptivo: "DxtCompositor"

Propiedades



| Propiedad   | Tipo | Valor predeterminado | Descripción                                                    |
|------------|------|---------|----------------------------------------------------------------|
| Alto     | long | 0       | Alto del rectángulo de destino, en píxeles.                     |
| OffsetX    | long | 0       | Desplazamiento horizontal del rectángulo de destino, en píxeles.          |
| OffsetY    | long | 0       | Desplazamiento vertical del rectángulo de destino, en píxeles.            |
| SrcHeight  | long | 0       | Alto del subrectángulo en el origen, en píxeles.       |
| SrcOffsetX | long | 0       | Coordenada x del subrectángulo en el origen, en píxeles. |
| SrcOffsetY | long | 0       | Coordenada y del subrectángulo en el origen, en píxeles. |
| SrcWidth   | long | 0       | Ancho del subrectángulo en el origen, en píxeles.        |
| Ancho      | long | 0       | Ancho del rectángulo de destino, en píxeles.                      |



 

En el diagrama siguiente se muestran estas propiedades:

![propiedades de compositor](images/compmeasure.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transiciones y efectos](transitions-and-effects.md)
</dt> </dl>

 

 



