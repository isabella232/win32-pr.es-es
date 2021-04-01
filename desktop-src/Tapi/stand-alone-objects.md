---
description: TAPI 3 implica una serie de objetos que son independientes de los cinco objetos TAPI principales (TAPI, dirección, llamada, CallHub y terminal).
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Objetos Stand-Alone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909621"
---
# <a name="stand-alone-objects"></a>Objetos Stand-Alone

TAPI 3 implica una serie de objetos que son independientes de los cinco objetos TAPI principales (TAPI, dirección, llamada, CallHub y terminal). Las interfaces de [eventos](./event-interfaces.md) y los [enumeradores](enumerator-interfaces.md) son objetos independientes y se resumen por separado. A continuación se resumen las interfaces independientes sin eventos y sin enumerador.



| Interfaz                                             | Descripción                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | Proporciona métodos para permitir que las aplicaciones cliente de automatización como Visual Basic recuperen información de la colección.                                                                                             |
| [**ITCollection2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | Extiende [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) proporcionando métodos adicionales para modificar colecciones.                                                                                                       |
| [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | Interfaz COM estándar para implementar la automatización.                                                                                                                                                           |
| [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | Interfaz COM estándar para obtener punteros a interfaces de objeto.                                                                                                                                             |
| [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | Permite que una aplicación recupere el puntero de envío de otra interfaz en un objeto, dado un puntero [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) actual. Útil para algunos lenguajes de scripting. |
| [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | Proporciona métodos que permiten a una aplicación TAPI 3 usar [telefonía asistida](assisted-telephony-overview.md).                                                                                                |



 



| Interfaz                                  | Descripción                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | Inicia, detiene y pausa las acciones actuales, como una reproducción.                                                                                                             |
| [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | Proporciona métodos específicos de reproducción que permiten que una aplicación realice operaciones como establecer la lista de archivos que se van a reproducir y cambiar la velocidad de reproducción.              |
| [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | Proporciona métodos específicos del registro que permiten que una aplicación realice operaciones como establecer los nombres de los archivos que se van a registrar y cambiar la duración de una grabación. |



 



| Interfaz                                                  | Descripción                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITScriptableAudioFormat**](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | Recupera el formato de audio de, o establece el formato de audio de una pista.                                                                                             |
| [**ITStaticAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | Proporciona métodos de objetos de terminal de audio estáticos que son necesarios para admitir dispositivos telefónicos. TAPI 3,1 MSP debe exponer esta interfaz en todos los terminales de audio estáticos. |



 

 

 
