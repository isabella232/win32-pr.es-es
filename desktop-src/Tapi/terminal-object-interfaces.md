---
description: Las interfaces de objeto de terminal proporcionan a una aplicación acceso para manipular los dispositivos usados para crear o recibir transmisiones multimedia.
ms.assetid: 08320d1c-1400-4746-b526-74b0789c5fc0
title: Interfaces de objetos de terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3286d9a2bf3c247f813d3a1f942b0490de0154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819411"
---
# <a name="terminal-object-interfaces"></a>Interfaces de objetos de terminal

Las interfaces de [objeto de terminal](terminal-object.md) proporcionan a una aplicación acceso para manipular los dispositivos usados para crear o recibir transmisiones multimedia.

Estas interfaces se implementan mediante un MSP y no estarán disponibles si la dirección no es compatible con un proveedor de servicios multimedia. Si existe un MSP asociado, la interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) se expone en el [objeto Address](address-object.md).

Las interfaces [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal) y [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) no se exponen directamente en el objeto terminal, sino que están estrechamente relacionadas con ella y se enumeran aquí para facilitar la referencia.



| Interfaz                                                                  | Descripción                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                           | Interfaz base para el objeto terminal. Proporciona métodos para obtener información como la clase de terminal y los medios admitidos. |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                                 | Establece y obtiene el formato multimedia de DirectShow.                                                                                            |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)                       | Proporciona métodos para establecer y obtener características estándar del terminal de audio, como el volumen.                                          |
| [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal)                                     | Enumera [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal).                                                                                      |
| [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)                           | Enumera la [**clase de terminal**](terminal-class.md).                                                                              |
| [**IEnumPluggableSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo)       | Enumera [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo).                                        |
| [**IEnumPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo) | Enumera [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo).                                                  |
| [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack)                                         | Recupera y establece información sobre las pistas de terminal de archivo.                                                                   |
| [**ITASRTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent)                           | Recupera la descripción de los eventos de terminal de reconocimiento de voz automáticos.                                                        |
| [**ITFileTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent)                         | Recupera la descripción de los eventos de terminal de archivo.                                                                                |
| [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal)                       | Enumera, crea o quita pistas en terminales multipista.                                                                   |



 



| Interfaz                                                                                      | Descripción                                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)                           | Recupera información relativa a un terminal acoplable.                                                                       |
| [**ITPluggableTerminalClassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalclassregistration)           | Crea, modifica o elimina la entrada del registro para un terminal acoplable.                                                   |
| [**ITPluggableTerminalInitialization**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalinitialization)                 | Realiza la creación de objetos de Terminal Server principales para los terminales conectables, lo que permite al administrador de Terminal Server inicializar el terminal. |
| [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)                 | Recupera el nombre y el CLSID de una clase de terminal conectable.                                                                  |
| [**ITPluggableTerminalSuperclassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalsuperclassregistration) | Recupera y establece información acerca de una superclase de terminal (nombre y CLSID).                                                 |
| [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink)                           | Notifica a las aplicaciones cliente los cambios en un terminal acoplable.                                                          |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)   | Registra y anula el registro de una aplicación cliente para recibir notificaciones sobre los eventos de terminal conectables.                             |



 



| Interfaz                                            | Descripción                                                        |
|------------------------------------------------------|--------------------------------------------------------------------|
| [**ITTTSTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent)     | Recupera la descripción de los eventos de terminal de texto a voz (TTS). |
| [**ITToneDetectionEvent**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittonedetectionevent) | Recupera información sobre un evento de detección de tono.                |
| [**ITToneTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent)   | Recupera la descripción de los eventos de terminal de tono.                 |



 

 

 
