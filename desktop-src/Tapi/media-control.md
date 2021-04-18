---
description: El medio de una sesión de comunicaciones es el formulario en el que se transmiten los datos. Los controles multimedia permiten a una aplicación reconocer una variedad de tipos de medios y ajustar aspectos del flujo multimedia, como el volumen de la transmisión de voz.
ms.assetid: b32503fe-d494-44ea-b144-e38b8ab9b3d4
title: Control multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50dad56e3feef8493a70cf93152b225be2777848
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678639"
---
# <a name="media-control"></a>Control multimedia

El medio de una sesión de comunicaciones es el formulario en el que se transmiten los datos. Los controles multimedia permiten a una aplicación reconocer una variedad de tipos de medios y ajustar aspectos del flujo multimedia, como el volumen de la transmisión de voz.

La disponibilidad de la información y el control multimedia varía considerablemente con el tipo de aplicación TAPI, la compatibilidad con el proveedor de servicios y el entorno de comunicaciones local. En el material siguiente se proporciona una descripción general del control de medios. TAPI proporciona un marco de trabajo flexible para la implementación de controles, por lo que las funcionalidades más interesantes serán a menudo específicas para un determinado proveedor de servicios.

En la telefonía clásica, una aplicación tenía muy poco control sobre el flujo multimedia una vez configurada una ruta de comunicación. Las aplicaciones TAPI 2 tienen acceso a algunas funciones que les permiten reconocer y reaccionar por dígitos o tonos durante una llamada, y pueden usar la API Wave para ejercer un mayor control sobre los medios durante una sesión de comunicaciones, pero de lo contrario no tienen acceso a la transmisión por secuencias multimedia. Consulte información general sobre el [acceso a medios](./media-access.md) de TAPI 2,2 o información general sobre el [acceso a los medios](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) de TSPI para una revisión de estas funciones.

TAPI 3 presenta los [proveedores de servicios multimedia](about-the-media-service-provider-msp-.md), que aumentan a la vez la información y el control sobre el medio o una sesión de comunicación. Una aplicación TAPI 3 puede tener acceso directamente al [flujo](stream-objects.md) multimedia de una sesión. Se crea una secuencia independiente para cada tipo de medio implicado en la sesión, como voz o vídeo. Algunos MSP pueden implementar controles de subflujo, que pueden dividir aún más las secuencias, como por participante en el caso de IPConf MSP.



| Funciones de TAPI 2. x                                          | Descripción                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**lineGatherDigits**](/windows/win32/api/tapi/nf-tapi-linegatherdigits)       | Inicia la recopilación de dígitos almacenada en búfer en la llamada especificada.                                                          |
| [**lineGenerateDigits**](/windows/win32/api/tapi/nf-tapi-linegeneratedigits)   | Inicia la generación de los dígitos especificados en la llamada especificada como tonos de banda ancha mediante el modo de señalización especificado. |
| [**lineGenerateTone**](/windows/win32/api/tapi/nf-tapi-linegeneratetone)       | Genera el tono de inband especificado en la llamada especificada.                                                               |
| [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)     | Habilita y deshabilita la detección no almacenada en búfer de dígitos recibidos en la llamada.                                              |
| [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia)       | Habilita y deshabilita la detección de tipos de medios en la llamada especificada.                                                   |
| [**lineMonitorTones**](/windows/win32/api/tapi/nf-tapi-linemonitortones)       | Habilita y deshabilita la detección de tonos en banda en la llamada.                                                            |
| [**lineSetMediaControl**](/windows/win32/api/tapi/nf-tapi-linesetmediacontrol) | Habilita y deshabilita las acciones de control en el flujo multimedia asociado a la línea, dirección o llamada especificadas.             |



 



| Interfaces o métodos TAPI 3. x                               | Descripción                                                                                                                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) | Es compatible con aplicaciones heredadas que se deben comunicar directamente con un dispositivo.                                                                                                                             |
| [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport)           | Permite a una aplicación detectar si un terminal creado por un TSP heredado (anterior a la TAPI 3) se puede controlar mediante Wave API.                                                                        |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                 | Permite que una aplicación recupere información en un flujo; para iniciar, pausar o detener la secuencia; para seleccionar o anular la selección de terminales en una secuencia; y para obtener una lista de los terminales seleccionados en la secuencia. |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)                   | Permite que una aplicación Enumere, cree o quite secuencias de multimedia.                                                                                                                                   |



 

 

 
