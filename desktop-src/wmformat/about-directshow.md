---
title: Obtenga información DirectShow en Windows SDK de Formato multimedia 11, una arquitectura de streaming de datos de alto nivel, modular, extensible y para la plataforma Windows.
description: Acerca de DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows SDK de formato multimedia, DirectShow
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- DirectShow,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aeb5dc9ebc613f7820a8ba4c4f5877ce9ac27068f1c4e873f9e8b00ec2f3b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840420"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Acerca DirectShow (Windows SDK de Formato multimedia 11)

DirectShow es una arquitectura de streaming de datos modular, extensible y de alto nivel para la plataforma Windows datos. Proporciona los componentes de software subyacentes y las interfaces de programación de aplicaciones (API) para una amplia variedad de aplicaciones de audio y vídeo digitales en el mercado actualmente. DirectShow está disponible como parte del Kit de desarrollo de software de Microsoft DirectX. Para obtener más información sobre DirectShow, consulte el SDK de la plataforma de Microsoft.

En DirectShow, todos los componentes de streaming de datos se *denominan filtros*. Un filtro puede representar un dispositivo de hardware, un codificador o descodificador de software, un representador de audio o vídeo, o cualquier funcionalidad de procesamiento de audio y vídeo. Para permitir que las aplicaciones basadas en DirectShow lean y escriban contenido de formato multimedia de Windows, incluido el contenido protegido por Digital Rights Management (DRM), Microsoft proporciona dos filtros que encapsulan partes del SDK de formato multimedia de Windows. Estos son el [lector de ASF de WM](wm-asf-reader-filter.md) y el escritor de [ASF de WM.](wm-asf-writer-filter.md) Estos filtros y las interfaces que exponen se conocen colectivamente como componentes de QASF, después del archivo DLL en el que se empaquetan. (La Q es el nombre de código inicial de La Q, un nombre de código DirectShow).

> [!Note]  
> El uso de los códecs de la serie Windows Media Audio y Video 9 a través de los componentes qasF de DirectShow requiere Microsoft Windows Millennium Edition o posterior, o DirectX 8.0 o posterior.

 

En el diagrama siguiente se muestra DirectShow gráfico de filtros para reproducir Windows archivos de vídeo multimedia.

![Gráfico de reproducción de vídeo de Windows Media](images/wmv-wmasfreader.png)

El lector [DE ASF](wm-asf-reader-filter.md) wm es un componente QASF, los descodificadores son componentes del SDK de formato multimedia Windows hospedados en el filtro contenedor de DMO (un componente QASF) y los representadores son componentes DirectShow.

 

 




