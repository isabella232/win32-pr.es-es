---
title: Errores del secuenciador
description: Errores del secuenciador
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- Valores devueltos de MCIERR, errores del secuenciador
- referencia multimedia, errores del secuenciador
- referencia de los elementos multimedia, errores del secuenciador
- Media control Interface (MCI), errores del secuenciador
- MCI (interfaz de control de medios), errores del secuenciador
- referencia de MCI, errores del secuenciador
- Referencia de MCI, errores del secuenciador
- Media control Interface (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- errores del secuenciador
- Errores del secuenciador de MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775978"
---
# <a name="sequencer-errors"></a>Errores del secuenciador

Se definen los siguientes valores devueltos adicionales para los secuenciadores MCI:



| Value                          | Significado                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ Seq \_ div \_ incompatible | Los formatos de hora del "puntero de canción" y SMPTE son singulares. No se pueden usar juntos.                                                              |
| MCIERR \_ Seq \_ NOMIDIPRESENT     | Este sistema no tiene dispositivos MIDI instalados. Use la opción controladores del panel de control para instalar un controlador MIDI.                                       |
| MCIERR \_ Seq \_ Puerto \_ inuse       | El puerto MIDI especificado ya está en uso. Espere hasta que sea gratuito; a continuación, vuelva a intentarlo.                                                                       |
| MCIERR \_ Seq \_ Puerto \_ MAPNODEVICE | La configuración actual del asignador de MIDI hace referencia a un dispositivo MIDI que no está instalado en el sistema. Use el asignador MIDI del panel de control para editar la configuración. |
| MCIERR \_ Seq \_ Puerto \_ MISCERROR   | Se produjo un error con el puerto especificado.                                                                                                                   |
| Puerto de MCIERR \_ Seq \_ \_ inexistente | El dispositivo MIDI especificado no está instalado en el sistema. Use la opción controladores del panel de control para instalar un dispositivo MIDI.                        |
| MCIERR \_ Seq \_ PORTUNSPECIFIED   | El sistema no tiene especificado un puerto MIDI actual.                                                                                                  |
| temporizador de MCIERR \_ Seq \_             | Todos los temporizadores multimedia están siendo utilizados por otras aplicaciones. Salga de una de estas aplicaciones; a continuación, vuelva a intentarlo.                                             |



 

 

 




