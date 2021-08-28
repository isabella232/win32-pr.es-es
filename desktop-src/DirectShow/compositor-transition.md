---
description: Transición de compositor
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Transición de compositor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 763194308ea01a31e132aebccdfca84f06dae56e9c01b47c689b03215cdb2698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084304"
---
# <a name="compositor-transition"></a>Transición de compositor

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La transición compositora compone una subrectangle desde el primer plano a un rectángulo designado en el fondo, sin modificar el resto del fondo. Use esta transición para crear efectos de pantalla dividida o de imagen en imagen.

En la imagen siguiente se muestra la transición del compositor:

![compositor transition](images/trans-compositor.png)

Id. de clase (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}

Nombre de la variable CLSID: CLSID \_ DxtCompositor

Nombre descriptivo: "DxtCompositor"

Propiedades



| Propiedad   | Tipo | Valor predeterminado | Descripción                                                    |
|------------|------|---------|----------------------------------------------------------------|
| Alto     | long | 0       | Alto del rectángulo de destino, en píxeles.                     |
| OffsetX    | long | 0       | Desplazamiento horizontal del rectángulo de destino, en píxeles.          |
| OffsetY    | long | 0       | Desplazamiento vertical del rectángulo de destino, en píxeles.            |
| SrcHeight  | long | 0       | Alto de la subrectangle en el origen, en píxeles.       |
| SrcOffsetX | long | 0       | Coordenada x de la subrectangle en el origen, en píxeles. |
| SrcOffsetY | long | 0       | Coordenada y de la subrectangle en el origen, en píxeles. |
| SrcWidth   | long | 0       | Ancho de la subrectangle en el origen, en píxeles.        |
| Ancho      | long | 0       | Ancho del rectángulo de destino, en píxeles.                      |



 

En el diagrama siguiente se muestran estas propiedades:

![propiedades de compositor](images/compmeasure.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transiciones y efectos](transitions-and-effects.md)
</dt> </dl>

 

 



