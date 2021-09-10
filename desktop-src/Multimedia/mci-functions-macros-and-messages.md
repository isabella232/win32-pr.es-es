---
title: Macros y mensajes de funciones de MCI
description: Macros y mensajes de funciones de MCI
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- Mensajes de MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade9ac3ea5c2a3c74f94bab899305cdae7ec51c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371624"
---
# <a name="mci-functions-macros-and-messages"></a>Macros y mensajes de funciones de MCI

La mayoría de las aplicaciones MCI usan las funciones [**mciSendString**](/previous-versions//dd757161(v=vs.85)) y [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) decenas de veces. MCI proporciona algunas otras funciones útiles que la aplicación usará con menos frecuencia.

El identificador de dispositivo requerido por la mayoría de los comandos MCI normalmente se recupera en una llamada al [**comando open**](open.md) [**(MCI \_ OPEN).**](mci-open.md) Si necesita un identificador de dispositivo pero no desea abrir el dispositivo (por ejemplo, si desea consultar las funcionalidades del dispositivo antes de realizar cualquier otra acción), puede llamar a la función [**mciGetDeviceID.**](/previous-versions//dd757156(v=vs.85))

La [**función mciGetCreatorTask permite**](/previous-versions//dd757155(v=vs.85)) a la aplicación usar un identificador de dispositivo para recuperar un identificador para la tarea que creó ese identificador.

Puede usar las funciones [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) y [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) para asignar y recuperar la dirección de la función de devolución de llamada asociada a la marca "wait" (MCI \_ WAIT).

La [**función mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) recupera una cadena que describe un valor de error de MCI. Cada cadena que devuelve MCI, ya sean datos o una descripción de error, tiene un máximo de 128 caracteres. Los campos de cuadro de diálogo que tienen menos de 128 caracteres truncarán las cadenas más largas devueltas por MCI. Para obtener más información sobre estas cadenas, vea [Valores devueltos de MCIERR.](mcierr-return-values.md)

Las macros de MCI son herramientas que puede usar para crear y desensamblar valores que especifican formatos de hora. Estos formatos de hora se usan en muchos comandos MCI. Los formatos que actúan las macros son horas/minutos/segundos (HMS), minutos/segundos/fotogramas (MSF) y pistas/minutos/segundos/fotogramas (TMSF). En la tabla siguiente se enumeran las macros y sus descripciones.



| Macro                                        | Descripción                                        |
|----------------------------------------------|----------------------------------------------------|
| [**MCI \_ HMS \_ HOUR**](mci-hms-hour.md)       | Recupera el componente hours de un valor de HMS.   |
| [**MCI \_ HMS \_ MINUTE**](mci-hms-minute.md)   | Recupera el componente minutes de un valor de HMS. |
| [**MCI \_ HMS \_ SECOND**](mci-hms-second.md)   | Recupera el componente de segundos de un valor de HMS. |
| [**MCI \_ MAKE \_ HMS**](mci-make-hms.md)       | Crea un valor de HMS.                              |
| [**MCI \_ MAKE \_ MSF**](mci-make-msf.md)       | Crea un valor msf.                              |
| [**MCI \_ MAKE \_ TMSF**](mci-make-tmsf.md)     | Crea un valor TMSF.                              |
| [**MARCO DE MSF de MCI \_ \_**](/previous-versions//dd743438(v=vs.85))     | Recupera el componente de fotogramas de un valor msf.  |
| [**MCI \_ MSF \_ MINUTE**](mci-msf-minute.md)   | Recupera el componente minutes de un valor msf. |
| [**MCI \_ MSF \_ SECOND**](mci-msf-second.md)   | Recupera el componente de segundos de un valor msf. |
| [**MCI \_ TMSF \_ FRAME**](mci-tmsf-frame.md)   | Recupera el componente de fotogramas de un valor TMSF.  |
| [**MCI \_ TMSF \_ MINUTE**](mci-tmsf-minute.md) | Recupera el componente minutes de un valor TMSF. |
| [**MCI \_ TMSF \_ SECOND**](mci-tmsf-second.md) | Recupera el componente de segundos de un valor TMSF. |
| [**MCI \_ TMSF \_ TRACK**](mci-tmsf-track.md)   | Recupera el componente tracks de un valor TMSF.  |



 

MCI también proporciona dos mensajes: [**MM \_ MXIATIFY**](mm-mcinotify.md) y [**MM \_ MCISIGNAL**](mm-mcisignal.md). El mensaje MM MXIATIFY notifica a una aplicación el resultado de un comando MCI cada vez que ese comando especifica la marca \_ "notify" (MCI \_ NOTIFY). El mensaje MM MCISIGNAL es específico de los dispositivos de vídeo digital; notifica a la aplicación cuando se alcanza \_ una posición especificada.

 

 