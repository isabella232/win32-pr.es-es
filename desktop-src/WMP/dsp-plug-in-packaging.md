---
title: Empaquetado de complementos de DSP
description: Empaquetado de complementos de DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Complementos de Windows Media Player, Media Foundation canalización
- complementos, canalización Media Foundation
- Complementos de procesamiento de señal digital, Media Foundation canalización
- Complementos DSP, canalización de Media Foundation
- Canalización de Media Foundation
- Complementos de Windows Media Player, canalización de DirectShow
- complementos, canalización de DirectShow
- Complementos de procesamiento de señal digital, canalización de DirectShow
- Complementos DSP, canalización de DirectShow
- Canalización de DirectShow
- Complementos de procesamiento de señal digital, básico
- Complementos DSP, básico
- Complementos de Windows Media Player, DSP básico
- complementos, DSP básico
- Complementos DSP básicos
- Complementos de Windows Media Player, DSP de modo dual
- complementos, DSP de modo dual
- Complementos de procesamiento de señal digital, modo dual
- Complementos DSP, modo dual
- Complementos DSP de modo dual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695662"
---
# <a name="dsp-plug-in-packaging"></a>Empaquetado de complementos de DSP

Windows Media Player representa audio y vídeo mediante una de las siguientes canalizaciones.

-   DirectShow
-   Media Foundation

En Microsoft Windows XP y versiones anteriores, el reproductor utiliza DirectShow. En Windows Vista, el reproductor a veces usa DirectShow y a veces usa Media Foundation.

Un complemento DSP diseñado para ejecutarse en la canalización de DirectShow se denomina *complemento DSP básico*. Los complementos de DSP básicos actúan como un objeto multimedia de DirectX (DMO). Un complemento DSP básico se puede ejecutar de forma nativa en la canalización de DirectShow y también puede ejecutarse en la canalización de Media Foundation dentro de un contenedor proporcionado por Media Foundation.

Un complemento DSP diseñado para ejecutarse de forma nativa (no se requiere ningún contenedor) en las canalizaciones de DirectShow y Media Foundation se denomina *complemento DSP de modo dual*. Un complemento DSP de modo dual puede actuar como un DMO o como una transformación de Media Foundation (MFT).

Un complemento DSP es un objeto COM que se empaqueta como un archivo. dll de registro automático. Las interfaces que implementa el complemento dependen de si el complemento está diseñado como un complemento de DSP básico o como un complemento de DSP de modo dual. Para obtener información detallada sobre las interfaces que deben implementar los complementos DSP, consulte [interfaces necesarias](required-interfaces.md).

Un complemento DSP que se ejecuta en la canalización de Media Foundation (ya sea de forma nativa o ajustada) debe registrar su modelo de subprocesos como "both". Para obtener información detallada acerca de las subclaves del registro y las entradas asociadas a los complementos de DSP, consulte [registrar complementos de DSP](registering-dsp-plug-ins.md).

Un complemento DSP que implementa interfaces personalizadas y que se ejecuta en la canalización Media Foundation (ya sea de forma nativa o ajustada) debe estar emparejado con un archivo. dll de código auxiliar de proxy que pueda serializar las interfaces personalizadas a través de los límites del proceso. Para obtener información acerca del componente proxy-stub, vea [actualizar complementos de DSP existentes](updating-existing-dsp-plug-ins.md) y [actualizaciones del Asistente para complementos de dsp para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

Los objetos de complemento de DSP no deben crearse como singletons. Windows Media Player debe ser capaz de crear varias instancias independientes de un complemento DSP determinado.

Los complementos DSP que se ejecutan en la ruta de acceso multimedia protegida (PMP) de Windows Vista deben estar firmados. Para obtener más información, vea [firma de código para componentes multimedia protegidos en Windows Vista](/windows-hardware/test/hlk/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador de complementos de DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 