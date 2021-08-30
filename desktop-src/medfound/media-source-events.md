---
description: Eventos de origen multimedia
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Eventos de origen multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee97d0d13aa96b4b0c480535836e827e9cdea47a551c371082d71a65c1c8021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941645"
---
# <a name="media-source-events"></a>Eventos de origen multimedia

En este tema se enumeran los eventos enviados por orígenes multimedia y secuencias multimedia. Los orígenes multimedia también pueden enviar eventos personalizados que no aparecen aquí.

## <a name="media-source-events"></a>Eventos de origen multimedia



| Evento                                                                      | Descripción                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Evento MEEndOfPresentation](meendofpresentation.md)                       | Finalizó la presentación. Todas las secuencias de la presentación han llegado al final de la secuencia.      |
| [Evento MENewStream](menewstream.md)                                       | Se ha creado una nueva secuencia. El evento contiene un puntero a la secuencia.                            |
| [Evento MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) | Las características del origen han cambiado. (Opcional).                                      |
| [Evento MESourceMetadataChanged](mesourcemetadatachanged.md)               | Los metadatos del origen han cambiado. (Opcional).                                                   |
| [Evento MESourcePaused](mesourcepaused.md)                                 | El origen se ha pausado. No todos los orígenes admiten pausas.                                          |
| [Evento MESourceRateChanged](mesourceratechanged.md)                       | La velocidad de reproducción del origen ha cambiado. (Opcional; se aplica si el origen admite el control de velocidad). |
| [Evento MESourceRateChangeRequested](mesourceratechangerequested.md)       | El origen solicita una nueva velocidad de reproducción. (Opcional).                                        |
| [Evento MESourceSeeked](mesourceseeked.md)                                 | Se ha buscando el origen. No todos los orígenes admiten la búsqueda.                                          |
| [Evento MESourceStarted](mesourcestarted.md)                               | Se inició el origen.                                                                          |
| [Evento MESourceStopped](mesourcestopped.md)                               | Se detuvo el origen.                                                                          |
| [Evento MEUpdatedStream](meupdatedstream.md)                               | Se ha buscan o se vuelve a iniciar una secuencia existente. El evento contiene un puntero a la secuencia.         |



 

## <a name="media-stream-events"></a>Eventos de secuencias multimedia



| Evento                                                    | Descripción                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Evento MEEndOfStream](meendofstream.md)                 | La secuencia finalizó.                                                                                                              |
| [Evento MEError](meerror.md)                             | Se ha producido un error durante el streaming. Use este evento para los errores que no están relacionados con ninguno de los demás eventos enumerados aquí. |
| [Evento MEMediaSample](memediasample.md)                 | La secuencia ha generado un nuevo ejemplo.                                                                                         |
| [Evento MEStreamFormatChanged](mestreamformatchanged.md) | El tipo de medio ha cambiado. (Opcional).                                                                                        |
| [Evento MEStreamPaused](mestreampaused.md)               | La secuencia se ha pausado.                                                                                                         |
| [Evento MEStreamSeeked](mestreamseeked.md)               | Se ha buscando la secuencia.                                                                                                         |
| [Evento MEStreamStarted](mestreamstarted.md)             | Se inició la secuencia.                                                                                                        |
| [Evento MEStreamStopped](mestreamstopped.md)             | La secuencia se detuvo.                                                                                                        |
| [Evento MEStreamThinMode](mestreamthinmode.md)           | El modo de ajuste se ha iniciado o detenido. (Opcional).                                                                              |
| [Evento MEStreamTick](mestreamtick.md)                   | Hay una brecha en la secuencia. (Opcional).                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia](media-sources.md)
</dt> </dl>

 

 



