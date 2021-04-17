---
title: Delegados
description: La API de streaming de multimedia proporciona las siguientes funciones de controlador de eventos.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533129"
---
# <a name="delegates"></a>Delegados

La [API de streaming de multimedia](media-streaming-api-portal.md) proporciona las siguientes funciones de controlador de eventos.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))<br/>                   | Representa la función que controlará el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) , que notifica al cliente los cambios en el estado de conexión de red del dispositivo.<br/>               |
| [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))<br/>       | Representa la función que controlará los eventos [**DeviceArrival**](devicearrival.md) y [**DeviceDeparture**](devicedeparture.md) , que notifican al cliente los cambios en la lista de dispositivos almacenados en caché.<br/> |
| [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))<br/> | Representa la función que controlará el evento [**RenderingParametersUpdate**](renderingparametersupdate.md) , que notifica al cliente una actualización a cualquiera de los parámetros de control de representación de DMR.<br/>  |
| [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))<br/> | Representa la función que controlará el evento [**TransportParametersUpdate**](transportparametersupdate.md) , que notifica al cliente una actualización a cualquiera de los parámetros de transporte DMR.<br/>          |



 

 

