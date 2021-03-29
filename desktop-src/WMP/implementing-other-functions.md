---
title: Implementar otras funciones
description: Implementar otras funciones
ms.assetid: 274ba948-b954-4e9e-a384-dee5b3befbcb
keywords:
- visualizaciones, interfaz IWMPEffects
- visualizaciones personalizadas, interfaz IWMPEffects
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función render, funciones adicionales
- Interfaz IWMPEffects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed6efa5cc9a0697653e558f27165b66d5f230fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420285"
---
# <a name="implementing-other-functions"></a>Implementar otras funciones

Sin duda, querrá escribir su propia implementación de la función **Render** . Se proporcionan otras funciones que también son funciones miembro de la interfaz **IWMPEffects** . Algunos le proporcionarán información adicional que puede elegir usar y otros proporcionarán de forma automática Windows Media Player con información generada por el asistente, como el nombre de la visualización.

La interfaz **IWMPEffects** admite las siguientes funciones además de **presentar**:



| Función                                                   | Descripción                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DisplayPropertyPage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage) | Implementación predeterminada no proporcionada por el asistente.                                                                                                                                                                                                                                                           |
| [GetCapabilities](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities)         | Obtiene las capacidades de la visualización y las pasa a Windows Media Player.                                                                                                                                                                                                                     |
| [GetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset)       | El asistente creó dos valores preestablecidos cuando generó el código para la visualización. Se llama a esta función cuando el desarrollador de máscaras desea obtener el índice del valor preestablecido actual. No querrá cambiar la implementación de esta función porque solo usa la información establecida por otras funciones. |
| [GetPresetCount](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount)           | El asistente creó dos valores preestablecidos cuando generó el código para la visualización. Puede cambiar el recuento cambiando la implementación de **GetPresetCount**. Consulte [valores preestablecidos](presets.md) para obtener más información sobre cómo cambiar los valores preestablecidos.                                                             |
| [GetPresetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle)           | El asistente creó dos valores preestablecidos cuando generó el código para la visualización. Puede cambiar los títulos utilizados cambiando la implementación de **GetPresetTitle**. Consulte [valores preestablecidos](presets.md) para obtener más información sobre cómo cambiar los valores preestablecidos.                                                       |
| [GetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle)                       | Obtiene el título de la visualización y lo pasa a Windows Media Player. El asistente usó el nombre del proyecto para generar el nombre que se ha devuelto.                                                                                                                                           |
| [GoFullscreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen)               | Implementación predeterminada no proporcionada por el asistente.                                                                                                                                                                                                                                                           |
| [MediaInfo](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo)                     | Recupera el número de canales de audio y la velocidad de muestra del audio que se reproduce actualmente.                                                                                                                                                                                                               |
| [RenderFullScreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen)       | Implementación predeterminada no proporcionada por el asistente.                                                                                                                                                                                                                                                           |
| [SetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset)       | El asistente creó dos valores preestablecidos cuando generó el código para la visualización. Se llama a esta función cuando Windows Media Player desea cambiar a un valor preestablecido con nombre.                                                                                                                                   |



 

La interfaz **IWMPEffects2** admite las siguientes funciones adicionales:



| Función                                            | Descripción                                                                                                                                      |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creación](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)                   | Al representar en una ventana, Windows Media Player llama a esta función para que pueda crear una nueva ventana para la representación.                          |
| [Borrar](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy)                 | Cuando se representa en una ventana, Windows Media Player llama a esta función para permitirle destruir la ventana que creó cuando se llamó a **Create** . |
| [NotifyNewMedia](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia)   | Esta función permite que la visualización responda cuando el reproductor haya cargado un nuevo elemento multimedia.                                          |
| [OnWindowMessage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage) | Esta función recibe mensajes de Windows del reproductor cuando se representa en modo sin ventanas.                                                       |
| [RenderWindowed](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed)   | El reproductor llama a esta función en lugar de **IWMPEffects:: Render** cuando el reproductor se representa en modo de ventana.                          |
| [SetCore](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore)                 | Esta función recibe un puntero a la interfaz **IWMPCore** .                                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementar el código**](implementing-your-code.md)
</dt> </dl>

 

 




