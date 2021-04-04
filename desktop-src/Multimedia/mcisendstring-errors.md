---
title: Errores de mciSendString
description: Errores de mciSendString
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- Valores devueltos de MCIERR, errores de mciSendString
- referencia multimedia, errores mciSendString
- referencia para multimedia, errores mciSendString
- Media control Interface (MCI), errores mciSendString
- MCI (media control Interface), errores mciSendString
- referencia para MCI, errores mciSendString
- Referencia de MCI, errores mciSendString
- Media control Interface (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- errores de mciSendString
- mciSendString función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904566"
---
# <a name="mcisendstring-errors"></a>Errores de mciSendString

La función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) devuelve los siguientes errores, pero no [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):



| Value                             | Significado                                           |
|-----------------------------------|---------------------------------------------------|
| MCIERR \_ ( \_ constante incorrecta)             | El valor especificado para un parámetro es desconocido.   |
| MCIERR \_ \_ entero incorrecto              | Falta un entero en el comando o no era válido. |
| MCIERR \_ marcas duplicadas \_          | Una marca o un valor se especificó dos veces.              |
| MCIERR \_ falta \_ la \_ cadena de comandos  | No se especificó ningún comando.                         |
| MCIERR \_ falta \_ \_ el nombre del dispositivo     | No se especificó ningún nombre de dispositivo.                     |
| MCIERR \_ \_ argumento de cadena ausente \_ | Falta un valor de cadena en el comando.      |
| MCIERR \_ nuevo \_ requiere \_ alias      | Se debe usar un alias con el nombre de dispositivo "nuevo". |
| MCIERR \_ no \_ hay \_ comilla de cierre        | Falta una comilla de cierre.              |
| MCIERR \_ notificar \_ al \_ \_ abrir automáticamente    | El indicador "notificar" no es válido con apertura automática.      |
| \_desbordamiento del parámetro MCIERR \_           | La cadena de salida no era lo suficientemente larga.            |
| \_analizador \_ interno de MCIERR          | Se produjo un error interno del analizador.                |
| \_ \_ palabra clave MCIERR desconocida     | Se especificó un parámetro de comando desconocido.       |



 

 

 