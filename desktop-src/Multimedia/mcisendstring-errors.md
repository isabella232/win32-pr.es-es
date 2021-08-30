---
title: Errores de mciSendString
description: Errores de mciSendString
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- MCIERR devuelve valores, errores mciSendString
- referencia multimedia, errores de mciSendString
- referencia de los errores multimedia,mciSendString
- Interfaz de control multimedia (MCI), errores de mciSendString
- MCI (interfaz de control multimedia), errores de mciSendString
- referencia de errores MCI,mciSendString
- Referencia de MCI, errores de mciSendString
- Interfaz de control multimedia (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- Errores de mciSendString
- Función mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d7603821a20dd154548cdf3cc69b84d54df1d549e9f3c87362e10a03e8e9bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783445"
---
# <a name="mcisendstring-errors"></a>Errores de mciSendString

La función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) devuelve los siguientes errores, pero no [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):



| Value                             | Significado                                           |
|-----------------------------------|---------------------------------------------------|
| CONSTANTE MALA DE MCIERR \_ \_             | El valor especificado para un parámetro es desconocido.   |
| ENTERO NEGATIVO DE MCIERR \_ \_              | Un entero del comando no era válido o faltaba. |
| MARCAS \_ DUPLICADAS DE MCIERR \_          | Se especificó dos veces una marca o un valor.              |
| FALTA LA \_ CADENA DE COMANDO \_ DE \_ MCIERR  | No se especificó ningún comando.                         |
| FALTA EL NOMBRE \_ DEL DISPOSITIVO EN MCIERR \_ \_     | No se especificó ningún nombre de dispositivo.                     |
| FALTA EL ARGUMENTO \_ DE \_ CADENA DE \_ MCIERR | Faltaba un valor de cadena en el comando.      |
| MCIERR \_ NEW \_ REQUIERE \_ ALIAS      | Se debe usar un alias con el nombre de dispositivo "nuevo". |
| MCIERR \_ NO \_ CLOSING \_ QUOTE        | Falta una comilla de cierre.              |
| NOTIFICACIÓN DE MCIERR \_ \_ AL ABRIR \_ \_ AUTOMÁTICAMENTE    | La marca "notify" no es posible con la apertura automática.      |
| MCIERR \_ PARAM \_ OVERFLOW           | La cadena de salida no era lo suficientemente larga.            |
| MCIERR \_ PARSER \_ INTERNAL          | Error interno del analizador.                |
| PALABRA CLAVE MCIERR \_ NO \_ RECONOCIDA     | Se especificó un parámetro de comando desconocido.       |



 

 

 