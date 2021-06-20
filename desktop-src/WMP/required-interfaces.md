---
title: Interfaces necesarias (Reproductor de Windows Media SDK)
description: Obtenga información sobre las interfaces necesarias que Reproductor de Windows Media implementa en DirectShow o Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Reproductor de Windows Media complementos, interfaces
- complementos, interfaces
- complementos de procesamiento de señales digitales, interfaces
- Complementos de DSP, interfaces
- interfaces, complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406098"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Interfaces necesarias (Reproductor de Windows Media SDK)

Reproductor de Windows Media representa audio y vídeo mediante una de las siguientes canalizaciones.

-   DirectShow
-   Media Foundation

En Microsoft Windows XP y versiones anteriores, el reproductor usa DirectShow. En Windows Vista, el Reproductor a veces usa DirectShow y, a veces, usa Media Foundation.

Un complemento DSP implementa algunas o todas las interfaces siguientes:

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

Un complemento que implementa **IMediaObject** e **IWMPPluginEnable** se puede ejecutar en la canalización de DirectShow. También se puede ejecutar en la canalización Media Foundation dentro de un contenedor proporcionado por Media Foundation. Un complemento de este tipo se denomina objeto multimedia (DMO) de Microsoft DirectX. Es habitual pensar que un DMO es análogo a un objeto de filtro en DirectShow. La documentación de DMO se encuentra en la sección DirectShow de la Windows SDK.

Un complemento que implementa **IMFTransform** y **IMFGetService** se puede ejecutar de forma nativa (no se requiere ningún contenedor) en la Media Foundation ejecución. Un complemento de este tipo se denomina Media Foundation Transform (MFT). La documentación de MFT se encuentra en Media Foundation sección de la Windows SDK.

Un complemento que implementa **IMediaObject**, **IWMPPluginEnable,** **IMFTransform** y **IMFGetService** se puede ejecutar en la canalización DirectShow y también se puede ejecutar de forma nativa en la canalización Media Foundation. Este tipo de complemento, que se denomina complemento DSP de modo *dual,* puede desempeñar el rol de DMO o MFT.

Cuando Reproductor de Windows Media un complemento DSP de modo dual en la canalización de Media Foundation, primero consulta la interfaz **DETRANSFORM.** Si se produce un error en esa consulta, Reproductor de Windows Media consultas para la **interfaz IMediaObject.** Si la **consulta IMediaObject** se realiza correctamente, el complemento se encapsula y se agrega a la Media Foundation ejecución.

Independientemente de la canalización, cualquier complemento de DSP que permita al usuario establecer propiedades debe implementar **ISpecifyPropertyPages**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador del complemento DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Interfaces de complemento DE DSP**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Empaquetado del complemento DE DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




