---
title: Obtenga información sobre DirectShow en Windows Media Format SDK 11, una arquitectura de streaming de datos de alto nivel, modular, extensible y para la plataforma Windows.
description: Acerca de DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK,DirectShow
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- DirectShow, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a76d7c8971c452f01176be7472e313181eb2831
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011298"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Acerca de DirectShow (Windows Media Format SDK 11)

DirectShow es una arquitectura de streaming de datos modular, extensible y de alto nivel para la plataforma Windows. Proporciona los componentes de software subyacentes y las interfaces de programación de aplicaciones (API) para una amplia variedad de aplicaciones de audio y vídeo digitales en el mercado actualmente. DirectShow está disponible como parte del Kit de desarrollo de software de Microsoft DirectX. Para más información sobre DirectShow, consulte el SDK de la plataforma de Microsoft.

En DirectShow, todos los componentes de streaming de datos se *denominan filtros*. Un filtro puede representar un dispositivo de hardware, un codificador o descodificador de software, un representador de audio o vídeo, o cualquier funcionalidad de procesamiento de audio y vídeo. Para permitir que las aplicaciones basadas en DirectShow lean y escriban contenido Windows Media Format, incluido el contenido protegido por Digital Rights Management (DRM), Microsoft proporciona dos filtros que encapsulan partes del SDK de Windows Media Format. Estos son el [lector de ASF de WM](wm-asf-reader-filter.md) y el escritor de [ASF de WM.](wm-asf-writer-filter.md) Estos filtros y las interfaces que exponen se conocen colectivamente como componentes de QASF, después del archivo DLL en el que se empaquetan. (La Q es el nombre de código inicial de DirectShow).

> [!Note]  
> El uso de los códecs de las series Windows Media Audio y Video 9 a través de los componentes de DirectShow QASF requiere Microsoft Windows Millennium Edition o posterior, o DirectX 8.0 o posterior.

 

En el diagrama siguiente se muestra un gráfico de filtros de DirectShow para reproducir Windows Media Video archivos.

![Gráfico de reproducción de vídeo de Windows Media](images/wmv-wmasfreader.png)

El [lector DE ASF](wm-asf-reader-filter.md) wm es un componente QASF, los descodificadores son componentes del SDK de Windows Media Format hospedados en el filtro contenedor de DMO (un componente QASF) y los representadores son componentes de DirectShow.

 

 




