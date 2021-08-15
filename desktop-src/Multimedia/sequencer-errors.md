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
- referencia de MCI,errors
- Referencia de MCI, errores
- errores del secuenciador
- Errores del secuenciador de MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea7e5b38d5541041e8ec065c8cad31f9d31ed1bfa9f22562aba1bf1ff04039b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371133"
---
# <a name="sequencer-errors"></a>Errores del secuenciador

Los siguientes valores devueltos adicionales se definen para los secuenciadores de MCI:



| Valor                          | Significado                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ SEQ \_ DIV \_ INCOMPATIBLE | Los formatos de hora del "puntero de canción" y SMPTE son singulares. No se pueden usar juntos.                                                              |
| MCIERR \_ SEQ \_ NOMIDIPRESENT     | Este sistema no tiene ningún dispositivo MIDI instalado. Use la opción Controladores de la Panel de control para instalar un controlador MIDI.                                       |
| USO DEL PUERTO \_ MCIERR \_ \_ SEQ       | El puerto MIDI especificado ya está en uso. Espere hasta que sea gratis; a continuación, inténtelo de nuevo.                                                                       |
| MAPNODEVICE DE PUERTO DE MCIERR \_ SEQ \_ \_ | La configuración actual del asignador de MIDI hace referencia a un dispositivo MIDI que no está instalado en el sistema. Use el Asignador de MIDI de la Panel de control para editar la configuración. |
| ERROR DE PUERTO DE MCIERR \_ SEQ \_ \_   | Error con el puerto especificado.                                                                                                                   |
| PUERTO MCIERR \_ SEQ \_ \_ INEXISTENTE | El dispositivo MIDI especificado no está instalado en el sistema. Use la opción Controladores de la Panel de control para instalar un dispositivo MIDI.                        |
| MCIERR \_ SEQ \_ PORTUNSPECIFIED   | El sistema no tiene especificado un puerto MIDI actual.                                                                                                  |
| TEMPORIZADOR DE MCIERR \_ \_ SEQ             | Otras aplicaciones usan todos los temporizadores multimedia. Salga de una de estas aplicaciones; a continuación, inténtelo de nuevo.                                             |



 

 

 




