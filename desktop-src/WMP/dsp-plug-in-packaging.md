---
title: Empaquetado del complemento DE DSP
description: Empaquetado del complemento DE DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Reproductor de Windows Media complementos, canalización Media Foundation datos
- complementos, canalización de Media Foundation
- complementos de procesamiento de señal digital, canalización Media Foundation digital
- Complementos de DSP, canalización de Media Foundation
- Media Foundation canalización
- Reproductor de Windows Media complementos,DirectShow canalización
- complementos, canalización de DirectShow
- complementos de procesamiento de señal digital, canalización DirectShow digital
- Complementos de DSP, canalización de DirectShow
- DirectShow canalización
- complementos de procesamiento de señales digitales, básico
- Complementos de DSP, básico
- Reproductor de Windows Media complementos, DSP básico
- complementos, DSP básico
- complementos de DSP básicos
- Reproductor de Windows Media complementos, DSP de modo dual
- complementos, DSP de modo dual
- complementos de procesamiento de señales digitales, modo dual
- Complementos de DSP, modo dual
- complementos DSP de modo dual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bd87e1729b4d8759f3b9f1d7d4d7993660512d49c34ea9bf9aa34802b69cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749510"
---
# <a name="dsp-plug-in-packaging"></a>Empaquetado del complemento DE DSP

Reproductor de Windows Media representa audio y vídeo mediante una de las siguientes canalizaciones.

-   DirectShow
-   Media Foundation

En Microsoft Windows XP y versiones anteriores, el reproductor usa DirectShow. En Windows Vista, el reproductor a veces usa DirectShow y, a veces, usa Media Foundation.

Un complemento DSP diseñado para ejecutarse en la canalización DirectShow se denomina complemento *DSP básico.* Los complementos de DSP básicos actúan como un objeto multimedia DirectX (DMO). Un complemento DSP básico se puede ejecutar de forma nativa en la canalización de DirectShow y también se puede ejecutar en la canalización Media Foundation dentro de un contenedor proporcionado por Media Foundation.

Un complemento DSP diseñado para ejecutarse de forma nativa (no se requiere ningún contenedor) en las canalizaciones DirectShow y Media Foundation se denomina complemento DSP de modo *dual.* Un complemento DSP de modo dual puede actuar como DMO o como una transformación Media Foundation (MFT).

Un complemento DSP es un objeto COM que se empaqueta como un archivo de registro .dll registro. Las interfaces que implementa el complemento dependen de si el complemento está diseñado como un complemento DSP básico o como un complemento DSP de modo dual. Para obtener información detallada sobre las interfaces que deben implementar los complementos de DSP, vea [Interfaces necesarias.](required-interfaces.md)

Un complemento DSP que se ejecuta en la canalización Media Foundation (ya sea de forma nativa o encapsulada) debe registrar su modelo de subprocesos como "Ambos". Para obtener información detallada sobre las subclaves del Registro y las entradas asociadas a los complementos de DSP, consulte Registro de complementos [DE DSP.](registering-dsp-plug-ins.md)

Un complemento DSP que implementa interfaces personalizadas y se ejecuta en la canalización de Media Foundation (ya sea de forma nativa o encapsulada) debe emparejarse con un archivo de código auxiliar de proxy .dll que pueda serializar las interfaces personalizadas a través de los límites del proceso. Para obtener información sobre el componente de código auxiliar de proxy, vea Actualización de complementos y actualizaciones [de DSP existentes](updating-existing-dsp-plug-ins.md) al Asistente para complementos [DE DSP para Reproductor de Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

Los objetos de complemento de DSP no deben crearse como singletons. Reproductor de Windows Media ser capaz de crear varias instancias independientes de un complemento DE DSP determinado.

Los complementos DE DSP que se ejecutan en Windows la ruta de acceso multimedia protegida (PMP) de Vista deben estar firmados. Para obtener más información, vea [Firma de código para componentes multimedia protegidos en Windows Vista](/windows-hardware/test/hlk/).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador del complemento DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 