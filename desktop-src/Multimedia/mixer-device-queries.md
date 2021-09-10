---
title: Mixer Consultas de dispositivos
description: Mixer Consultas de dispositivos
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- audio multimedia, consultas de dispositivo mezclador
- audio, consultas de dispositivo mezclador
- mezcladores de audio, consultas de dispositivos
- mezcladores, consultas de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372398"
---
# <a name="mixer-device-queries"></a>Mixer Consultas de dispositivos

Los servicios mezcladores proporcionan funciones para determinar el número de dispositivos mezcladores presentes en el sistema y las funcionalidades de los dispositivos. También puede usar una función de servicios de mezclador para determinar el identificador de dispositivo de un dispositivo mezclador.

Puede usar la [**función mixerGetNumDevs para**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) determinar cuántos dispositivos mezclador están presentes en el sistema. Mixer dispositivos se identifican mediante un identificador de dispositivo. Los identificadores de dispositivo se determinan implícitamente a partir del número de dispositivos presentes en un sistema determinado. Oscilan entre cero y uno menos que el número de dispositivos presentes.

Antes de usar un dispositivo mezclador, debe determinar sus funcionalidades. Las funcionalidades de audio pueden variar de un equipo multimedia a otro, por lo que las aplicaciones deben trabajar con una variedad de hardware de audio.

Puede usar la función [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) para determinar las funcionalidades de los dispositivos mezcladores. Esta función rellena una estructura [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) con información sobre las funcionalidades de un dispositivo especificado.

La [**función mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) recupera el identificador del dispositivo mezclador de audio asociado a un identificador de dispositivo especificado. Por ejemplo, podría usar esta función para recuperar el identificador de dispositivo de un mezclador de audio y, a continuación, usar el identificador del dispositivo para ajustar el volumen o para mostrar otro control.

 

 