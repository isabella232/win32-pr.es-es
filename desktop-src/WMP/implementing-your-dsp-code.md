---
title: Implementación del código DSP
description: Implementación del código DSP
ms.assetid: e1feaaee-1127-4a3a-9a4c-a30584a7e8ff
keywords:
- Reproductor de Windows Media complementos, procesamiento de señal digital (DSP)
- complementos, procesamiento de señales digitales (DSP)
- complementos de procesamiento de señales digitales, implementar código
- Complementos de DSP, implementar código
- complementos de procesamiento de señales digitales, modificación del código de ejemplo
- Complementos de DSP, modificar código de ejemplo
- complementos de DSP de audio, implementar código
- complementos DE DSP de vídeo, implementar código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8504a44b9f3e980be612569e9b7cbe06081d0bfe704a5932e44eef789127687f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135568"
---
# <a name="implementing-your-dsp-code"></a>Implementación del código DSP

Una vez que haya creado el complemento DSP de ejemplo, puede modificar el código para crear su propio complemento de REPRODUCTOR DE WINDOWS MEDIA DSP. Los métodos que cambie y los que puede dejar como están dependen de los siguientes factores:

-   Número de propiedades que desea permitir que el usuario cambie. Sin duda, querrá cambiar la implementación predeterminada de la página de propiedades para que se adapte a sus necesidades y es posible que tenga que agregar propiedades adicionales.
-   Si el complemento DSP necesita asignar recursos de streaming. El complemento puede requerir búferes adicionales.
-   Si el complemento DSP de audio debe seguir generando datos después de que Reproductor de Windows Media haya dejado de proporcionar datos en el búfer de entrada.

En las secciones siguientes se usa el código de ejemplo del complemento DSP generado por el Asistente para complementos de Reproductor de Windows Media para ilustrar conceptos importantes. Es posible que le sea útil abrir Microsoft Visual Studio generar primero el código de ejemplo para que pueda hacer referencia a él mientras lee esta sección. Para obtener más información sobre cómo usar el Asistente para Reproductor de Windows Media complemento, consulte [Building a DSP Plug-in](building-a-dsp-plug-in.md).



| Sección                                                                    | Descripción                                                                                                       |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Implementación de un complemento dsp de audio](implementing-an-audio-dsp-plug-in.md) | Describe lo que necesita saber para crear su propio complemento DSP de audio basado en el ejemplo generado por el asistente. |
| [Implementación de un complemento DSP de vídeo](implementing-a-video-dsp-plug-in.md)   | Describe lo que necesita saber para crear su propio complemento DSP de vídeo basado en el ejemplo generado por el asistente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de los complementos de DSP**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




