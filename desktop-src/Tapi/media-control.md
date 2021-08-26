---
description: El medio de una sesión de comunicaciones es el formulario en el que se transmiten los datos. Los controles multimedia permiten a una aplicación reconocer diversos tipos de medios y ajustar aspectos de la secuencia multimedia, como el volumen de transmisión de voz.
ms.assetid: b32503fe-d494-44ea-b144-e38b8ab9b3d4
title: Control multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17e3ad30107a98cc5d1a312880fa29422c42dce2b2bc59cadfbf894cb032d74a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034535"
---
# <a name="media-control"></a>Control multimedia

El medio de una sesión de comunicaciones es el formulario en el que se transmiten los datos. Los controles multimedia permiten a una aplicación reconocer diversos tipos de medios y ajustar aspectos de la secuencia multimedia, como el volumen de transmisión de voz.

La disponibilidad del control multimedia y la información varía ampliamente con el tipo de aplicación TAPI, la compatibilidad con el proveedor de servicios y el entorno de comunicaciones local. El siguiente material proporciona una descripción general del control multimedia. TAPI proporciona un marco flexible para la implementación de controles, por lo que las funcionalidades más interesantes a menudo serán específicas de un proveedor de servicios determinado.

En la telefonía clásica, una aplicación tenía muy poco control sobre el flujo multimedia una vez que se había configurado una ruta de comunicación. Las aplicaciones TAPI 2 tienen acceso a algunas funciones que les permiten reconocer y reaccionar a dígitos o tonos durante una llamada, y pueden usar Wave API para ejercer un control adicional sobre los medios durante una sesión de comunicaciones, pero de lo contrario no tienen acceso al flujo multimedia. Consulte la introducción a TAPI 2.2 [Media Access](./media-access.md) o la información general de TSPI [Media Access](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) para ver una revisión de estas funciones.

TAPI 3 presenta los proveedores de [servicios](about-the-media-service-provider-msp-.md)multimedia , lo que aumenta considerablemente tanto la información sobre los medios como el control sobre ellos o una sesión de comunicación. Una aplicación TAPI 3 puede acceder directamente al flujo [multimedia](stream-objects.md) de una sesión. Se crea una secuencia independiente para cada tipo de medio implicado en la sesión, como voz o vídeo. Algunos MSP pueden implementar controles de subdifusión, que pueden dividir aún más las secuencias, como por participante en el caso del MSP de IPConf.



| Funciones TAPI 2.x                                          | Descripción                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**lineGatherDigits**](/windows/win32/api/tapi/nf-tapi-linegatherdigits)       | Inicia la recopilación en búfer de dígitos en la llamada especificada.                                                          |
| [**lineGenerateDigits**](/windows/win32/api/tapi/nf-tapi-linegeneratedigits)   | Inicia la generación de los dígitos especificados en la llamada especificada como tonos de inband mediante el modo de señalización especificado. |
| [**lineGenerateTone**](/windows/win32/api/tapi/nf-tapi-linegeneratetone)       | Genera el tono de inband especificado sobre la llamada especificada.                                                               |
| [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)     | Habilita y deshabilita la detección sin búfer de dígitos recibidos en la llamada.                                              |
| [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia)       | Habilita y deshabilita la detección de tipos de medios en la llamada especificada.                                                   |
| [**lineMonitorMonitorMonitor**](/windows/win32/api/tapi/nf-tapi-linemonitortones)       | Habilita y deshabilita la detección de los tonos de inband en la llamada.                                                            |
| [**lineSetMediaControl**](/windows/win32/api/tapi/nf-tapi-linesetmediacontrol) | Habilita y deshabilita las acciones de control en el flujo multimedia asociado a la línea, dirección o llamada especificadas.             |



 



| Interfaces o métodos tapi 3.x                               | Descripción                                                                                                                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) | Admite aplicaciones heredadas que deben comunicarse directamente con un dispositivo.                                                                                                                             |
| [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport)           | Permite que una aplicación detecte si un terminal creado por un TSP heredado (anterior a TAPI 3) se puede controlar mediante Wave API.                                                                        |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                 | Permite que una aplicación recupere información en una secuencia; para iniciar, pausar o detener la secuencia; para seleccionar o anular la selección de terminales en una secuencia; y para obtener una lista de terminales seleccionados en la secuencia. |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)                   | Permite que una aplicación enumere, cree o quite secuencias multimedia.                                                                                                                                   |



 

 

 
