---
description: Orígenes de información de región de DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Orígenes de información de región de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729dc02d07b927dd2bb7938ba87c6435df04459ad3ebd1976ede808bd292552e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904105"
---
# <a name="sources-of-dvd-region-information"></a>Orígenes de información de región de DVD

Hay tres orígenes de información de la región de DVD que funcionan conjuntamente para determinar la región para la reproducción de DVD en un Windows PC.

-   Título del DVD. La mayoría de los títulos de DVD se marcan para una región específica. Algunos títulos solo se pueden reproducir en una región, otros se pueden reproducir en varias regiones y otros se pueden reproducir en todas las regiones. Las regiones del 1 al 6 se definieron en la especificación DVD-Video original. La región 7 no está definida actualmente. La región 8 se agregó en 1999 para lugares especiales, como aviones. Los discos DVD-ROM (aquellos que no tienen ninguna zona de vídeo) no deben contener ninguna codificación de región.
-   Unidad DE DVD-ROM. Hay dos tipos de unidades de DVD-ROM: unidades rpc fase 1 (RPC1) y rpc fase 2 (RPC2). Las unidades RPC1 no tienen compatibilidad integrada con hardware para la administración de regiones. Para estas unidades, Windows la información de recuento de cambios de región y la región solo se puede cambiar una vez. Las unidades RPC2 mantienen la información de recuento de cambios de región en el hardware y, en general, la región de dichas unidades se puede cambiar hasta cinco veces.
-   Descodificador de DVD. Algunos descodificadores de DVD, hardware o software, se establecen para una región específica. En general, el usuario no puede cambiar la región del descodificador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con el cambio de región de DVD en Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



