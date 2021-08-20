---
title: Asignación Waveform-Audio dispositivos
description: Asignación Waveform-Audio dispositivos
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- audio multimedia, asignación de dispositivos de audio de forma de onda
- audio, asignación de dispositivos de audio de forma de onda
- administrador de compresión de audio (ACM), asignación de dispositivos de audio de forma de onda
- ACM (administrador de compresión de audio), asignación de dispositivos de audio de forma de onda
- asignación de dispositivos de audio de forma de onda
- audio multimedia, asignador
- audio,mapper
- administrador de compresión de audio (ACM), asignador
- ACM (administrador de compresión de audio), asignador
- mapper
- audio de forma de onda, dispositivos de asignación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4204a79eebd5fed3c8f96712aa3cd83c50056b1c194bafe2ce485a5b4b68f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138776"
---
# <a name="mapping-waveform-audio-devices"></a>Asignación Waveform-Audio dispositivos

Windows proporciona un conjunto de funciones estándar para dispositivos de audio. Estas funciones emiten llamadas a controladores de dispositivo que administran dispositivos de hardware. El sistema usa un módulo denominado "asignador" para administrar los dispositivos instalados. El asignador usa enlaces especiales en la interfaz del controlador para interceptar llamadas y actuar como intermediario entre el sistema y los controladores instalados en el sistema. El asignador es responsable de hacer coincidir las solicitudes de acceso de una aplicación a un dispositivo con los dispositivos disponibles y de buscar un dispositivo que cumpla los requisitos de audio de la aplicación actual. El sistema proporciona asignadores para tipos de controladores estándar: audio de forma de onda, MIDI (interfaz digital de instrumentar música) y dispositivos auxiliares.

El ACM es una extensión del sistema multimedia básico y se instala como asignador. Esto significa que el ACM usa los enlaces del asignador de interfaz de controlador para dispositivos de audio de forma de onda. El uso de estos enlaces permite al ACM descodificar o codificar datos de audio de forma de onda antes de pasarlo a o desde un controlador de dispositivo de audio de forma de onda. La diferencia entre el ACM y el asignador del sistema estándar es que el ACM puede buscar un dispositivo de audio de forma de onda que admita un formato especificado o encontrar una combinación de un dispositivo de audio de forma de onda y un descomprimidor o un descomprimidor de ACM que admita un formato especificado.

Cuando una aplicación solicita que el sistema abra un dispositivo de audio de forma de onda para la entrada o salida, la solicitud especifica el formato y el dispositivo. Cuando el dispositivo especificado es el asignador, el asignador debe encontrar un dispositivo que admita el formato especificado. El asignador implementado en el ACM busca un dispositivo de audio de forma de onda instalado que admita el formato especificado. Si el ACM no encuentra este tipo de dispositivo, busca un dispositivo de audio de forma de onda y un descomprimidor o descomprimido que juntos admitan el formato. En concreto, el ACM busca un descomprimido o un descomprimidor que convierte el formato especificado en un formato compatible con un dispositivo de audio de forma de onda instalado. Después de que el ACM encuentre un dispositivo que admita el formato convertido, puede respetar las solicitudes para reproducir o grabar el formato solicitado originalmente, aunque ningún dispositivo de audio de forma de onda instalado admita directamente ese formato.

Además de la conversión de formato, el ACM también ofrece servicios para admitir la compresión, la descompresión, el filtrado, la selección de formato y la selección de filtros. Proporciona una API estándar que admite llamando a sus propios controladores.

 

 




