---
title: Errores del secuenciador
description: Errores del secuenciador
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- MCIERR devuelve valores, errores de secuenciador
- referencia multimedia, errores de secuenciador
- referencia de multimedia, errores de secuenciador
- Interfaz de control multimedia (MCI), errores de secuenciador
- MCI (interfaz de control multimedia), errores de secuenciador
- referencia de MCI, errores de secuenciador
- Referencia de MCI, errores de secuenciador
- Interfaz de control multimedia (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- errores del secuenciador
- Errores del secuenciador de MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370286"
---
# <a name="sequencer-errors"></a>Errores del secuenciador

Los siguientes valores devueltos adicionales se definen para los secuenciadores de MCI:



| Value                          | Significado                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ SEQ \_ DIV \_ INCOMPATIBLE | Los formatos de hora del "puntero de canción" y SMPTE son singulares. No se pueden usar juntos.                                                              |
| MCIERR \_ SEQ \_ NOMIDIPRESENT     | Este sistema no tiene ningún dispositivo MIDI instalado. Use la opción Controladores del Panel de control para instalar un controlador MIDI.                                       |
| USO DEL PUERTO \_ MCIERR SEQ \_ \_       | El puerto MIDI especificado ya está en uso. Espere hasta que sea gratis; a continuación, inténtelo de nuevo.                                                                       |
| MAPA DE PUERTO \_ DE MCIERR \_ SEQNODEVICE \_ | La configuración actual del asignador de MIDI hace referencia a un dispositivo MIDI que no está instalado en el sistema. Use el Asignador de MIDI de la Panel de control para editar la configuración. |
| ERROR DE PUERTO \_ DE MCIERR SEQ \_ \_   | Se produjo un error con el puerto especificado.                                                                                                                   |
| PUERTO MCIERR \_ SEQ \_ \_ INEXISTENTE | El dispositivo MIDI especificado no está instalado en el sistema. Use la opción Controladores de la Panel de control para instalar un dispositivo MIDI.                        |
| MCIERR \_ SEQ \_ PORTUNSPECIFIED   | El sistema no tiene especificado un puerto MIDI actual.                                                                                                  |
| TEMPORIZADOR DE MCIERR \_ SEQ \_             | Otras aplicaciones usan todos los temporizadores multimedia. Salga de una de estas aplicaciones; a continuación, inténtelo de nuevo.                                             |



 

 

 




