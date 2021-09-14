---
description: Desarrollo de codificadores y descodificadores
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Desarrollo de codificadores y descodificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160174"
---
# <a name="encoder-and-decoder-development"></a>Desarrollo de codificadores y descodificadores

Esta sección contiene artículos sobre el desarrollo de codificadores y descodificadores para DirectShow. Estos temas no son pertinentes para los desarrolladores de aplicaciones.

Se debe implementar un descodificador de software que admita la aceleración de vídeo (VA) de DirectX como filtro DirectShow transformación de copia. Si el descodificador no admite DirectX VA, también se puede implementar como un objeto multimedia directX (DMO). Un descodificador que se conecta a un representador de vídeo no debe implementarse como filtro trans-in-place, ya que esto provocará una degradación significativa del rendimiento. Para obtener información sobre cómo escribir un filtro de transformación de copia, vea [Escribir filtros de transformación](writing-transform-filters.md).

Los codificadores de software se pueden implementar como filtros de transformación o DDO. Los codificadores no usan DirectX VA, ya que DirectX VA actualmente solo se usa para la descompresión. La especificación de Encoder API descrita en esta sección es relevante para los codificadores de hardware y software.

Esta sección contiene los siguientes temas:

-   [Encoder API](encoder-api.md)
-   [Interfaces y especificaciones del descodificador](decoder-interfaces-and-specifications.md)
-   [Descodificador Configuración para Windows Media Center Edition](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de VMR para DirectShow de filtros](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



