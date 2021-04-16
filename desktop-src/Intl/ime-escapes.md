---
description: Estos escapes se usan con la función ImmEscape.
ms.assetid: ede886dc-8a92-428c-8975-3feadc1d4f90
title: Escapes de IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ff93751450ee6eb6957482362cc8bc22f41d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686920"
---
# <a name="ime-escapes"></a>Escapes de IME

Estos escapes se usan con la función [**ImmEscape**](/windows/desktop/api/Imm/nf-imm-immescapea) .



| Escape                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IME \_ Esc \_ Get \_ EUDC \_ Dictionary  | Recupere la ruta de acceso del archivo de diccionario EUDC. En la entrada, el parámetro *lpData* debe ser el puntero al búfer para recibir la ruta de acceso. Este búfer debe ser igual o mayor que 80 \* sizeof (TCHAR). En la devolución, el búfer contiene la cadena terminada en null que especifica la ruta de acceso completa del diccionario. Solo para uso del editor de EUDC de Chino; No use en otras aplicaciones.                                                                                  |
| \_modo de Esc \_ hanja \_ de IME            | Convertir de hangul a hanja. En la entrada, *lpData* debe apuntar al búfer que contiene el carácter hangul que se va a convertir. en la salida, recibe el hanja convertido como una cadena terminada en NULL. Para que lo use el editor Coreano; No use en otras aplicaciones.                                                                                                                                                                                                           |
| nombre IME de IME \_ Esc \_ \_              | Recupere el nombre del IME. En la entrada, el parámetro *lpData* debe ser el puntero al búfer para recibir el nombre. En la devolución, el búfer contiene la cadena terminada en null que especifica el nombre del IME. Solo para uso del editor de EUDC de Chino; No use en otras aplicaciones. **Windows Me/98/95:** El búfer no debe ser inferior a 16 \* sizeof (TCHAR).<br/> **Windows NT, windows 2000 y Windows XP:** El búfer no debe tener menos de 64 caracteres.<br/> |
| \_tecla ESC de IME \_ máx. \_               | El valor devuelto de la función es el número máximo de Stokes realiza de clave para un carácter EUDC. Solo para uso del editor de EUDC de Chino; No use en otras aplicaciones.                                                                                                                                                                                                                                                                                                         |
| \_ \_ compatibilidad con consultas ESC de IME \_         | Compruebe la implementación. En la entrada, *lpData* apunta al búfer que contiene el valor de escape del IME. La función devuelve 0 si no se implementa el escape.                                                                                                                                                                                                                                                                                                             |
| \_secuencia Esc \_ \_ de IME a \_ Internal | Devuelve el código de carácter que coincide con el código de secuencia especificado. En la entrada, el parámetro *lpData* es el puntero a una variable de 32 bits que contiene el código de secuencia. Solo para uso del editor de EUDC de Chino; No use en otras aplicaciones. Normalmente, el IME de chino codificará sus códigos de carácter de lectura en la secuencia 1 a n.                                                                                                                               |
| IME \_ Esc \_ set \_ EUDC \_ Dictionary  | Establezca el archivo de diccionario EUDC. En la entrada, el parámetro *lpData* es el puntero a una cadena terminada en null que especifica la ruta de acceso completa. La ruta de acceso debe ser inferior a 80 \* sizeof (TCHAR). Solo para uso del editor de EUDC de Chino; No use en otras aplicaciones.                                                                                                                                                                                                           |
| IME \_ Esc \_ GETHELPFILENAME        | **Windows Me/98, windows 2000 y Windows XP:** Devuelve el nombre del archivo de ayuda del IME. En la devolución, el parámetro *lpData* es la ruta de acceso completa del archivo de ayuda del IME. La ruta de acceso debe ser inferior a 80 \* sizeof (TCHAR).                                                                                                                                                                                                                                                           |



 

El sistema operativo reserva los escapes en el intervalo IME \_ Esc \_ Reserved \_ First to IME \_ Esc \_ Reserved \_ Last para su propio uso.

El sistema operativo reserva los escapes en el intervalo IME \_ Esc \_ Private \_ First to IME \_ Esc \_ Private \_ Last for Private by IME.

 

 




