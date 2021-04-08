---
title: Acerca de DirectShow (Windows Media Format 11 SDK)
description: Acerca de DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078753"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Acerca de DirectShow (Windows Media Format 11 SDK)

DirectShow es una arquitectura de streaming de datos de alto nivel, modular y extensible para la plataforma Windows. Proporciona los componentes de software subyacentes y las interfaces de programación de aplicaciones (API) para una amplia variedad de aplicaciones de audio y vídeo digitales en el mercado de hoy en día. DirectShow está disponible como parte del kit de desarrollo de software de Microsoft DirectX. Para obtener más información sobre DirectShow, vea el SDK de la plataforma de Microsoft.

En DirectShow, todos los componentes de streaming de datos se denominan *filtros*. Un filtro puede representar un dispositivo de hardware, un codificador o descodificador de software, un representador de audio o vídeo o cualquier capacidad de procesamiento de audio y vídeo. Para permitir que las aplicaciones basadas en DirectShow lean y escriban contenido de formato de Windows Media, incluido el contenido protegido por Rights Management digitales (DRM), Microsoft proporciona dos filtros que encapsulan partes del SDK de Windows Media Format. Estos son el [lector ASF de WM](wm-asf-reader-filter.md) y el [escritor ASF de WM](wm-asf-writer-filter.md). Estos filtros y las interfaces que exponen se conocen colectivamente como componentes de QASF, después de la DLL en la que se empaquetan. (La letra Q significa Quartz, un nombre de código temprano para DirectShow).

> [!Note]  
> El uso de los códecs de la serie de Windows Media Audio y vídeo 9 a través de los componentes de QASF de DirectShow requiere Microsoft Windows Millennium Edition o posterior, o bien DirectX 8,0 o posterior.

 

En el diagrama siguiente se muestra un gráfico de filtros de DirectShow para reproducir archivos Windows Media Video.

![gráfico de reproducción de vídeo de Windows Media](images/wmv-wmasfreader.png)

El [lector ASF de WM](wm-asf-reader-filter.md) es un componente de qasf, los descodificadores son componentes del SDK de Windows Media Format hospedados en el filtro de contenedor de DMO (un componente qasf) y los representadores son componentes de DirectShow.

 

 




