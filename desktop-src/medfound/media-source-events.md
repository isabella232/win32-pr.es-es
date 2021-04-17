---
description: Eventos de origen de medios
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Eventos de origen de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717393"
---
# <a name="media-source-events"></a>Eventos de origen de medios

En este tema se enumeran los eventos enviados por los orígenes multimedia y los flujos multimedia. Los orígenes multimedia también pueden enviar eventos personalizados que no se enumeran aquí.

## <a name="media-source-events"></a>Eventos de origen de medios



| Evento                                                                      | Descripción                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Evento MEEndOfPresentation](meendofpresentation.md)                       | Finalizó la presentación. Todas las secuencias de la presentación han alcanzado el final de la secuencia.      |
| [Evento MENewStream](menewstream.md)                                       | Se creó una nueva secuencia. El evento contiene un puntero a la secuencia.                            |
| [Evento MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) | Las características del origen han cambiado. (Opcional).                                      |
| [Evento MESourceMetadataChanged](mesourcemetadatachanged.md)               | Los metadatos del origen han cambiado. (Opcional).                                                   |
| [Evento MESourcePaused](mesourcepaused.md)                                 | El origen está en pausa. No todos los orígenes admiten la pausa.                                          |
| [Evento MESourceRateChanged](mesourceratechanged.md)                       | La velocidad de reproducción del origen ha cambiado. (Opcional; se aplica si el origen admite el control de tasas). |
| [Evento MESourceRateChangeRequested](mesourceratechangerequested.md)       | El origen está solicitando una nueva velocidad de reproducción. (Opcional).                                        |
| [Evento MESourceSeeked](mesourceseeked.md)                                 | Se ha buscado el origen. No todos los orígenes admiten búsquedas.                                          |
| [Evento MESourceStarted](mesourcestarted.md)                               | Se inició el origen.                                                                          |
| [Evento MESourceStopped](mesourcestopped.md)                               | El origen se detuvo.                                                                          |
| [Evento MEUpdatedStream](meupdatedstream.md)                               | Se ha buscado o se ha vuelto a iniciar una secuencia existente. El evento contiene un puntero a la secuencia.         |



 

## <a name="media-stream-events"></a>Eventos de flujo de medios



| Evento                                                    | Descripción                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Evento MEEndOfStream](meendofstream.md)                 | La secuencia finalizó.                                                                                                              |
| [Evento MEError](meerror.md)                             | Se ha producido un error durante el streaming. Utilice este evento para los errores que no están relacionados con ninguno de los otros eventos que se enumeran aquí. |
| [Evento MEMediaSample](memediasample.md)                 | La secuencia ha generado un nuevo ejemplo.                                                                                         |
| [Evento MEStreamFormatChanged](mestreamformatchanged.md) | El tipo de medio ha cambiado. (Opcional).                                                                                        |
| [Evento MEStreamPaused](mestreampaused.md)               | La secuencia está en pausa.                                                                                                         |
| [Evento MEStreamSeeked](mestreamseeked.md)               | Se ha buscado en la secuencia.                                                                                                         |
| [Evento MEStreamStarted](mestreamstarted.md)             | Se inició el flujo.                                                                                                        |
| [Evento MEStreamStopped](mestreamstopped.md)             | La secuencia se detuvo.                                                                                                        |
| [Evento MEStreamThinMode](mestreamthinmode.md)           | El modo delgado se ha iniciado o detenido. (Opcional).                                                                              |
| [Evento MEStreamTick](mestreamtick.md)                   | Hay una brecha en la secuencia. (Opcional).                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia](media-sources.md)
</dt> </dl>

 

 



