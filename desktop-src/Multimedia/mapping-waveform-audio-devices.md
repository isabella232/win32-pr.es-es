---
title: Asignación de dispositivos Waveform-Audio
description: Asignación de dispositivos Waveform-Audio
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- audio multimedia, asignación de los dispositivos de audio de onda
- audio, asignación de los dispositivos de audio de onda
- Administrador de compresión de audio (ACM), asignar dispositivos de audio de onda
- ACM (Administrador de compresión de audio), asignar dispositivos de audio de onda
- asignación de dispositivos de audio de onda
- audio multimedia, asignador
- audio, asignador
- Administrador de compresión de audio (ACM), asignador
- ACM (Administrador de compresión de audio), asignador
- mapper
- audio de onda, dispositivos de asignación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903333"
---
# <a name="mapping-waveform-audio-devices"></a>Asignación de dispositivos Waveform-Audio

Windows proporciona un conjunto de funciones estándar para dispositivos de audio. Estas funciones emiten llamadas a controladores de dispositivos que administran los dispositivos de hardware. El sistema utiliza un módulo denominado "asignador" para administrar los dispositivos instalados. El asignador usa enlaces especiales en la interfaz del controlador para interceptar las llamadas y actuar como intermediario entre el sistema y los controladores instalados en el sistema. El asignador es responsable de hacer coincidir las solicitudes de una aplicación para el acceso a un dispositivo con los dispositivos disponibles y para buscar un dispositivo que cumpla los requisitos de audio de la aplicación actual. El sistema proporciona asignadores para tipos de controlador estándar: audio de onda de onda, MIDI (interfaz digital de instrumentos musicales) y dispositivos auxiliares.

ACM es una extensión del sistema multimedia básico y se instala como un asignador. Esto significa que ACM usa los enlaces del asignador de interfaz de controlador para dispositivos de audio de forma de onda. El uso de estos enlaces permite a ACM descodificar o codificar los datos de audio de forma de onda antes de pasarlos a o desde un controlador de dispositivo de audio de forma de onda. La diferencia entre el sistema ACM y el asignador estándar es que ACM puede buscar un dispositivo de audio de forma de onda que admita un formato especificado o buscar una combinación de un dispositivo de audio de forma de onda y un compresor o descompresor de ACM que admita un formato especificado.

Cuando una aplicación solicita que el sistema abra un dispositivo de audio de forma de onda para entrada o salida, la solicitud especifica el formato y el dispositivo. Cuando el dispositivo especificado es el asignador, el asignador debe encontrar un dispositivo que admita el formato especificado. El asignador implementado en ACM busca un dispositivo de audio de forma de onda instalado que admita el formato especificado. Si ACM no puede encontrar este dispositivo, busca un dispositivo de audio de forma de onda y un compresor o descompresor que admitan el formato. En concreto, ACM busca un compresor o descompresor que convierte el formato especificado en un formato compatible con un dispositivo de audio de forma de onda instalado. Una vez que ACM encuentra un dispositivo que admite el formato convertido, puede aceptar solicitudes para reproducir o grabar el formato solicitado originalmente, aunque ningún dispositivo de audio de forma de onda instalado admita directamente ese formato.

Además de la conversión de formato, el ACM también ofrece servicios para admitir la compresión, la descompresión, el filtrado, la selección de formato y la selección de filtro. Proporciona una API estándar que admite mediante la llamada a sus propios controladores.

 

 




