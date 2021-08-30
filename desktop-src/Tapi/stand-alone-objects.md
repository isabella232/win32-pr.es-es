---
description: TAPI 3 implica una serie de objetos que son independientes de sus cinco objetos TAPI principales (TAPI, Address, Call, CallHub y Terminal).
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Stand-Alone objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0094f4409fc6f2ec52d505e29a2f09a2bcff872b159fbd3fafdf7c4ec56f8861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991775"
---
# <a name="stand-alone-objects"></a>Stand-Alone objetos

TAPI 3 implica una serie de objetos que son independientes de sus cinco objetos TAPI principales (TAPI, Address, Call, CallHub y Terminal). [Las interfaces de eventos](./event-interfaces.md) [y las interfaces de enumerador](enumerator-interfaces.md) son objetos independientes y se resumen por separado. A continuación se resumen las interfaces independientes que no son de evento y que no son de enumerador.



| Interfaz                                             | Descripción                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | Proporciona métodos para permitir que las aplicaciones cliente de Automation, como Visual Basic recuperar información de recopilación.                                                                                             |
| [**ITCollection2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | Extiende [**ITCollection proporcionando**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) métodos adicionales para modificar colecciones.                                                                                                       |
| [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | Interfaz COM estándar para implementar Automation.                                                                                                                                                           |
| [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | Interfaz COM estándar para obtener punteros a interfaces de objeto.                                                                                                                                             |
| [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | Permite que una aplicación recupere el puntero de envío de otra interfaz en un objeto , dado un puntero [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) actual. Útil para algunos lenguajes de scripting. |
| [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | Proporciona métodos que permiten que una aplicación TAPI 3 use [la telefonía asistida](assisted-telephony-overview.md).                                                                                                |



 



| Interfaz                                  | Descripción                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | Inicia, detiene y pausa las acciones actuales, como una reproducción.                                                                                                             |
| [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | Proporciona métodos específicos de reproducción que permiten a una aplicación realizar operaciones como establecer la lista de archivos para reproducir y cambiar la velocidad de reproducción.              |
| [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | Proporciona métodos específicos de grabación que permiten a una aplicación realizar operaciones como establecer los nombres de los archivos para grabar y cambiar la duración de una grabación. |



 



| Interfaz                                                  | Descripción                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITScriptableAudioFormat**](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | Recupera el formato de audio de una pista o establece el formato de audio de una pista.                                                                                             |
| [**ITStaticAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | Proporciona métodos en objetos de terminal de audio estáticos que son necesarios para admitir dispositivos de teléfono. Los MSP de TAPI 3.1 deben exponer esta interfaz en todos los terminales de audio estático. |



 

 

 
