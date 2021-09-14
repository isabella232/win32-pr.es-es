---
title: Errores de mciSendString
description: Errores de mciSendString
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- MCIERR return values,mciSendString errors
- referencia multimedia, errores de mciSendString
- referencia de los errores multimedia,mciSendString
- Interfaz de control multimedia (MCI), errores mciSendString
- Errores de MCI (interfaz de control multimedia),mciSendString
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
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245799"
---
# <a name="mcisendstring-errors"></a>Errores de mciSendString

La función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) devuelve los siguientes errores, pero no [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):



| Value                             | Significado                                           |
|-----------------------------------|---------------------------------------------------|
| MCIERR \_ BAD \_ CONSTANT             | Se desconoce el valor especificado para un parámetro.   |
| ENTERO NO VÁLIDO DE MCIERR \_ \_              | Un entero del comando no era válido o faltaba. |
| MARCAS \_ DUPLICADAS DE MCIERR \_          | Se especificó dos veces una marca o un valor.              |
| FALTA LA CADENA \_ DE \_ COMANDOS DE \_ MCIERR  | No se especificó ningún comando.                         |
| FALTA EL NOMBRE \_ DEL DISPOSITIVO EN MCIERR \_ \_     | No se especificó ningún nombre de dispositivo.                     |
| FALTA EL ARGUMENTO \_ DE \_ CADENA DE \_ MCIERR | Faltaba un valor de cadena en el comando.      |
| MCIERR \_ NEW \_ REQUIERE \_ ALIAS      | Se debe usar un alias con el nombre del dispositivo "nuevo". |
| MCIERR \_ NO \_ CLOSING \_ QUOTE        | Falta una comilla de cierre.              |
| NOTIFICACIÓN DE MCIERR \_ \_ AL ABRIR \_ \_ AUTOMÁTICAMENTE    | La marca "notify" no es posible con la apertura automática.      |
| MCIERR \_ PARAM \_ OVERFLOW           | La cadena de salida no era lo suficientemente larga.            |
| MCIERR \_ PARSER \_ INTERNAL          | Error interno del analizador.                |
| PALABRA CLAVE MCIERR \_ NO \_ RECONOCIDA     | Se especificó un parámetro de comando desconocido.       |



 

 

 