---
title: Interfaces necesarias (SDK de Windows Media Player)
description: Interfaces necesarias
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Complementos de Windows Media Player, interfaces
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos DSP, interfaces
- interfaces, Complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9c6923af513f2d241955b508f0872f85a4b020
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904952"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Interfaces necesarias (SDK de Windows Media Player)

Windows Media Player representa audio y vídeo mediante una de las siguientes canalizaciones.

-   DirectShow
-   Media Foundation

En Microsoft Windows XP y versiones anteriores, el reproductor utiliza DirectShow. En Windows Vista, el reproductor a veces usa DirectShow y a veces usa Media Foundation.

Un complemento DSP implementa algunas o todas las interfaces siguientes:

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

Un complemento que implementa **IMediaObject** y **IWMPPluginEnable** puede ejecutarse en la canalización de DirectShow. También puede ejecutarse en la canalización de Media Foundation dentro de un contenedor proporcionado por Media Foundation. Un complemento de este tipo se denomina Microsoft DirectX media Object (DMO). Es habitual considerar que un DMO es análogo a un objeto de filtro en DirectShow. La documentación de DMO está en la sección de DirectShow del Windows SDK.

Un complemento que implementa **IMFTransform** y **IMFGetService** se puede ejecutar de forma nativa (no se requiere ningún contenedor) en la canalización de Media Foundation. Un complemento de este tipo se denomina Media Foundation Transform (MFT). La documentación de MFT está en la sección Media Foundation del Windows SDK de.

Los complementos que implementan **IMediaObject**, **IWMPPluginEnable**, **IMFTransform** y **IMFGetService** se pueden ejecutar en la canalización de DirectShow y también se pueden ejecutar de forma nativa en la canalización de Media Foundation. Este tipo de complemento, que se denomina un *complemento DSP de modo dual*, puede desempeñar el rol de un DMO o una MFT.

Cuando Windows Media Player usa un complemento DSP de modo dual en la canalización de Media Foundation, primero consulta la interfaz **IMFTransform** . Si se produce un error en la consulta, Windows Media Player consultas para la interfaz **IMediaObject** . Si la consulta **IMediaObject** se realiza correctamente, el complemento se ajusta y se agrega a la canalización Media Foundation.

Independientemente de la canalización, cualquier complemento de DSP que permita al usuario establecer propiedades debe implementar **ISpecifyPropertyPages**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador de complementos de DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Interfaces de complemento de DSP**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Empaquetado de complementos de DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




