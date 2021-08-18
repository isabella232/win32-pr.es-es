---
title: Interfaces necesarias (Reproductor de Windows Media SDK)
description: Obtenga información sobre las interfaces necesarias que Reproductor de Windows Media implementa en DirectShow o Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Reproductor de Windows Media complementos,interfaces
- complementos, interfaces
- complementos de procesamiento de señales digitales, interfaces
- Complementos de DSP, interfaces
- interfaces, complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a3552cbe741b3b527c899e5bb7d68fe4d7c4e0bdc61203f822c57111e94a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646835"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Interfaces necesarias (Reproductor de Windows Media SDK)

Reproductor de Windows Media representa audio y vídeo mediante una de las siguientes canalizaciones.

-   DirectShow
-   Media Foundation

En Microsoft Windows XP y versiones anteriores, el reproductor usa DirectShow. En Windows Vista, el reproductor a veces usa DirectShow y, a veces, usa Media Foundation.

Un complemento DSP implementa algunas o todas las interfaces siguientes:

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

Un complemento que implementa **IMediaObject** e **IWMPPluginEnable** se puede ejecutar en la DirectShow ejecución. También se puede ejecutar en la canalización Media Foundation dentro de un contenedor proporcionado por Media Foundation. Un complemento de este tipo se denomina objeto multimedia De Microsoft DirectX (DMO). Es habitual pensar en un DMO como análogo a un objeto de filtro en DirectShow. La DMO documentación está en la DirectShow del SDK Windows.

Un complemento que implementa **IMFTransform** y **IMFGetService** se puede ejecutar de forma nativa (no se requiere ningún contenedor) en la canalización Media Foundation datos. Un complemento de este tipo se denomina Media Foundation Transform (MFT). La documentación de MFT se encuentra en Media Foundation sección del SDK de Windows.

Un complemento que implementa **IMediaObject,** **IWMPPluginEnable,** **IMFTransform** y **IMFGetService** se puede ejecutar en la canalización de DirectShow y también se puede ejecutar de forma nativa en la canalización Media Foundation. Este tipo de complemento, que se denomina complemento DSP de modo *dual,* puede desempeñar el rol de un DMO o MFT.

Cuando Reproductor de Windows Media un complemento DSP de modo dual en la canalización Media Foundation, primero consulta la interfaz **DETRANSFORMTransform.** Si se produce un error en esa consulta, Reproductor de Windows Media consultas para la **interfaz IMediaObject.** Si la **consulta IMediaObject** se realiza correctamente, el complemento se encapsula y se agrega a la Media Foundation ejecución.

Independientemente de la canalización, cualquier complemento DSP que permita al usuario establecer propiedades debe implementar **ISpecifyPropertyPages**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador del complemento DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Interfaces de complemento DE DSP**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Empaquetado del complemento DE DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




