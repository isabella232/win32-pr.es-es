---
description: Orígenes de información de la región de DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Orígenes de información de la región de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac426f995323bfd30d3430dccb4044c5f71a119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002383"
---
# <a name="sources-of-dvd-region-information"></a>Orígenes de información de la región de DVD

Hay tres orígenes de información de la región de DVD que funcionan conjuntamente para determinar la región de reproducción de DVD en un equipo Windows.

-   Título del DVD. La mayoría de los títulos de DVD se marcan para una región específica. Algunos títulos se pueden reproducir en una sola región, algunos se pueden reproducir en varias regiones y otros pueden reproducirse en todas las regiones. Las regiones 1 a 6 se definieron en la especificación de DVD-Video original. La región 7 no está definida actualmente. La región 8 se agregó en 1999 para lugares especiales, como aviones. Los discos DVD-ROM (los que no tienen ninguna zona de vídeo) no deben contener ninguna codificación de región.
-   Unidad de DVD-ROM. Hay dos tipos de unidades de DVD-ROM: las unidades RPC Phase 1 (RPC1) y las unidades RPC Phase 2 (RPC2). Las unidades RPC1 no tienen compatibilidad integrada con hardware para la administración de regiones. Para estas unidades, Windows mantiene la información del recuento de cambios de la región y la región se puede cambiar una sola vez. Las unidades RPC2 mantienen la información de recuento de cambios de la región en hardware y, en general, la región de dichas unidades puede cambiarse hasta cinco veces.
-   Descodificador de DVD. Algunos descodificadores de DVD, hardware o software, se establecen para una región específica. En general, el usuario no puede cambiar la región del descodificador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad de cambio de región de DVD en Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



