---
title: Implementar otras funciones
description: Implementar otras funciones
ms.assetid: 274ba948-b954-4e9e-a384-dee5b3befbcb
keywords:
- visualizaciones, interfaz IWMPEffects
- visualizaciones personalizadas, interfaz IWMPEffects
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función de representación, funciones adicionales
- Interfaz IWMPEffects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73392204357ec856c5c04f2a0f24028ea29e5f09c3aa203d95ed8e2cc7e4ded3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508935"
---
# <a name="implementing-other-functions"></a>Implementar otras funciones

Sin duda, querrá escribir su propia implementación de la **función Render.** Se proporcionan otras funciones que también son funciones miembro de **la interfaz IWMPEffects.** Algunos le proporcionarán información adicional que puede usar y otras proporcionarán automáticamente Reproductor de Windows Media información generada por el asistente, como el nombre de la visualización.

La **interfaz IWMPEffects** admite las siguientes funciones además de **Representar**:



| Función                                                   | Descripción                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DisplayPropertyPage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage) | Implementación predeterminada no proporcionada por el asistente.                                                                                                                                                                                                                                                           |
| [GetCapabilities](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities)         | Obtiene las funcionalidades de la visualización y las pasa a Reproductor de Windows Media.                                                                                                                                                                                                                     |
| [GetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset)       | El asistente creó dos valores preestablecidos cuando generó el código para la visualización. Se llama a esta función cuando el desarrollador de máscaras quiere obtener el índice del valor preestablecido actual. No querrá cambiar la implementación de esta función porque simplemente usa información establecida por otras funciones. |
| [GetPresetCount](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount)           | El asistente creó dos valores preestablecidos cuando generó el código para la visualización. Puede cambiar el recuento cambiando la implementación de **GetPresetCount**. Consulte [Valores preestablecidos](presets.md) para obtener más información sobre cómo cambiar los valores preestablecidos.                                                             |
| [GetPresetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle)           | El asistente creó dos valores preestablecidos cuando generó el código para la visualización. Puede cambiar los títulos usados cambiando la implementación de **GetPresetTitle**. Consulte [Valores preestablecidos](presets.md) para obtener más información sobre cómo cambiar los valores preestablecidos.                                                       |
| [GetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle)                       | Obtiene el título de la visualización y lo pasa a Reproductor de Windows Media. El asistente usó el nombre del proyecto para generar el nombre que se pasa.                                                                                                                                           |
| [GoFullscreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen)               | Implementación predeterminada no proporcionada por el asistente.                                                                                                                                                                                                                                                           |
| [Mediainfo](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo)                     | Recupera el número de canales de audio y la velocidad de muestreo del audio que se reproduce actualmente.                                                                                                                                                                                                               |
| [RenderFullScreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen)       | Implementación predeterminada no proporcionada por el asistente.                                                                                                                                                                                                                                                           |
| [SetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset)       | El asistente creó dos valores preestablecidos cuando generó el código para la visualización. Se llama a esta función Reproductor de Windows Media desea cambiar a un valor preestablecido con nombre.                                                                                                                                   |



 

La **interfaz IWMPEffects2** admite las siguientes funciones adicionales:



| Función                                            | Descripción                                                                                                                                      |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creación](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)                   | Al representar en una ventana, Reproductor de Windows Media llama a esta función para permitirle crear una nueva ventana para la representación.                          |
| [Destruir](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy)                 | Al representar en una ventana, Reproductor de Windows Media llama a esta función para que le permita destruir la ventana que creó cuando **se llamó** a Create. |
| [NotifyNewMedia](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia)   | Esta función permite que la visualización responda cuando el reproductor haya cargado un nuevo elemento multimedia.                                          |
| [OnWindowMessage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage) | Esta función recibe mensajes de Windows del reproductor cuando se representa en modo sin ventanas.                                                       |
| [RenderWindowed](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed)   | Player llama a esta función en lugar de **IWMPEffects::Render** cuando el reproductor se representa en modo de ventana.                          |
| [SetCore](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore)                 | Esta función recibe un puntero a la **interfaz IWMPCore.**                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementar el código**](implementing-your-code.md)
</dt> </dl>

 

 




