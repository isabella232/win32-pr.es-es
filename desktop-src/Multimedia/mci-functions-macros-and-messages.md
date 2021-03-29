---
title: Mensajes y macros de funciones MCI
description: Mensajes y macros de funciones MCI
ms.assetid: 7cedc46f-f67b-4b1a-b1e0-7ac32c250132
keywords:
- Mensajes de MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ade9ac3ea5c2a3c74f94bab899305cdae7ec51c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791397"
---
# <a name="mci-functions-macros-and-messages"></a>Mensajes y macros de funciones MCI

La mayoría de las aplicaciones MCI usan las funciones [**mciSendString**](/previous-versions//dd757161(v=vs.85)) y [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) docenas de veces. MCI proporciona algunas otras funciones útiles que la aplicación usará con menos frecuencia.

El identificador de dispositivo que requiere la mayoría de los comandos MCI se recupera normalmente en una llamada al comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)). Si necesita un identificador de dispositivo pero no desea abrir el dispositivo (por ejemplo, si desea consultar las funcionalidades del dispositivo antes de realizar cualquier otra acción), puede llamar a la función [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) .

La función [**mciGetCreatorTask**](/previous-versions//dd757155(v=vs.85)) permite que la aplicación use un identificador de dispositivo para recuperar un identificador de la tarea que creó dicho identificador.

Puede usar las funciones [**mciGetYieldProc**](/previous-versions//dd757159(v=vs.85)) y [**mciSetYieldProc**](/previous-versions//dd757163(v=vs.85)) para asignar y recuperar la dirección de la función de devolución de llamada asociada a la marca "Wait" (espera de MCI \_ ).

La función [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) recupera una cadena que describe un valor de error de MCI. Cada cadena devuelto por MCI, ya sea un valor de datos o una descripción de error, tiene un máximo de 128 caracteres. Los campos de cuadro de diálogo de menos de 128 caracteres truncarán las cadenas más largas devueltas por MCI. Para obtener más información sobre estas cadenas, vea [valores devueltos de MCIERR](mcierr-return-values.md).

Las macros de MCI son herramientas que se pueden usar para crear y desensamblar valores que especifican formatos de hora. Estos formatos de hora se usan en muchos comandos MCI. Los formatos a los que se aplican las macros son horas/minutos/segundos (HMS), minutos/segundos/marcos (MSF) y pistas/minutos/segundos/fotogramas (TMSF). En la tabla siguiente se enumeran las macros y sus descripciones.



| Macro                                        | Descripción                                        |
|----------------------------------------------|----------------------------------------------------|
| [**MCI \_ HMS \_ hora**](mci-hms-hour.md)       | Recupera el componente de horas de un valor de HMS.   |
| [**HMS de MCI \_ \_**](mci-hms-minute.md)   | Recupera el componente de minutos de un valor de HMS. |
| [**MCI \_ HMS \_ segundo**](mci-hms-second.md)   | Recupera el componente de segundos de un valor de HMS. |
| [**\_HMS MCI make \_**](mci-make-hms.md)       | Crea un valor de HMS.                              |
| [**MCI \_ Make \_ MSF**](mci-make-msf.md)       | Crea un valor de MSF.                              |
| [**\_TMSF MCI make \_**](mci-make-tmsf.md)     | Crea un valor de TMSF.                              |
| [**\_marco MCI MSF \_**](/previous-versions//dd743438(v=vs.85))     | Recupera el componente de marcos de un valor de MSF.  |
| [**MCI \_ en \_ minuto de MSF**](mci-msf-minute.md)   | Recupera el componente de minutos de un valor de MSF. |
| [**MCI \_ MSF \_ Second**](mci-msf-second.md)   | Recupera el componente de segundos de un valor de MSF. |
| [**fotograma TMSF de MCI \_ \_**](mci-tmsf-frame.md)   | Recupera el componente de marcos de un valor de TMSF.  |
| [**TMSF de MCI \_ \_**](mci-tmsf-minute.md) | Recupera el componente de minutos de un valor de TMSF. |
| [**MCI \_ TMSF \_ segundo**](mci-tmsf-second.md) | Recupera el componente de segundos de un valor de TMSF. |
| [**\_pista de TMSF de MCI \_**](mci-tmsf-track.md)   | Recupera el componente de seguimientos de un valor de TMSF.  |



 

MCI también proporciona dos mensajes: [**mm \_ MCINOTIFY**](mm-mcinotify.md) y [**mm \_ MCISIGNAL**](mm-mcisignal.md). El \_ mensaje mm MCINOTIFY notifica a una aplicación el resultado de un comando MCI siempre que ese comando especifique la marca "notificar" (notificación de MCI \_ ). El \_ mensaje mm MCISIGNAL es específico de los dispositivos de vídeo digital; notifica a la aplicación cuando se alcanza una posición especificada.

 

 