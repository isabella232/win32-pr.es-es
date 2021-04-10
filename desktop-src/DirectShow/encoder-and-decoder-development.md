---
description: Desarrollo del codificador y descodificador
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Desarrollo del codificador y descodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152347"
---
# <a name="encoder-and-decoder-development"></a>Desarrollo del codificador y descodificador

Esta sección contiene artículos sobre el desarrollo de codificadores y descodificadores para DirectShow. Estos temas no son relevantes para los desarrolladores de aplicaciones.

Un descodificador de software que admita DirectX video Acceleration (VA) debe implementarse como un filtro de transformación de copia de DirectShow. Si el descodificador no admite DirectX VA, también puede implementarse como un objeto multimedia de DirectX (DMO). Un descodificador que se conecta a un representador de vídeo no debe implementarse como un filtro de transbordo en contexto, ya que esto dará lugar a una degradación significativa del rendimiento. Para obtener información sobre cómo escribir un filtro de transformación de copia, consulte [escribir filtros de transformación](writing-transform-filters.md).

Los codificadores de software se pueden implementar como filtros de transformación o DMOs. Los codificadores no usan DirectX VA, ya que actualmente DirectX se usa solo para la descompresión. La especificación de la API del codificador que se describe en esta sección es relevante para los codificadores de hardware y software.

Esta sección contiene los siguientes temas:

-   [API del codificador](encoder-api.md)
-   [Interfaces y especificaciones del descodificador](decoder-interfaces-and-specifications.md)
-   [Configuración del descodificador para Windows Media Center Edition](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar la VMR para desarrolladores de filtros de DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



