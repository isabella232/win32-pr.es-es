---
title: Consultas de dispositivos de mezclador
description: Consultas de dispositivos de mezclador
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- audio multimedia, consultas de dispositivo de mezclador
- consultas de audio y de dispositivo de mezclador
- Mezcladores de audio, consultas de dispositivos
- mezcladores, consultas de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077691"
---
# <a name="mixer-device-queries"></a>Consultas de dispositivos de mezclador

Los servicios de mezclador proporcionan funciones para determinar el número de dispositivos de mezclador presentes en el sistema y las capacidades de los dispositivos. También puede usar una función de servicios de mezclador para determinar el identificador de dispositivo para un dispositivo de mezclador.

Puede usar la función [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) para determinar el número de dispositivos de mezclador presentes en el sistema. Los dispositivos de mezclador se identifican mediante un identificador de dispositivo. Los identificadores de dispositivo se determinan implícitamente a partir del número de dispositivos presentes en un sistema determinado. Van desde cero hasta uno menos que el número de dispositivos presentes.

Antes de usar un dispositivo de mezclador, debe determinar sus capacidades. Las capacidades de audio pueden variar de un equipo multimedia a otro, por lo que las aplicaciones deben trabajar con una variedad de hardware de audio.

Puede usar la función [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) para determinar las capacidades de los dispositivos de mezclador. Esta función rellena una estructura [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) con información sobre las capacidades de un dispositivo especificado.

La función [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) recupera el identificador de dispositivo del mezclador de audio asociado a un identificador de dispositivo especificado. Por ejemplo, puede usar esta función para recuperar el identificador de dispositivo de un mezclador de audio y, a continuación, usar el identificador de dispositivo para ajustar el volumen o para mostrar otro control.

 

 