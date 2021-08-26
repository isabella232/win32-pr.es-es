---
description: Estos escapes se usan con la función ImmEscape.
ms.assetid: ede886dc-8a92-428c-8975-3feadc1d4f90
title: IME Escapes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4764e884a65069d73c535d38d5ee2896b1d2ecaeb66600bd868f8830cddcfc4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107215"
---
# <a name="ime-escapes"></a>IME Escapes

Estos escapes se usan con la [**función ImmEscape.**](/windows/desktop/api/Imm/nf-imm-immescapea)



| Escape                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DICCIONARIO DE \_ \_ EUDC GET \_ DE \_ IME ESC  | Recupere la ruta de acceso del archivo de diccionario EUDC. En la entrada, el *parámetro lpData* debe ser el puntero al búfer para recibir la ruta de acceso. Este búfer debe ser igual o mayor que 80 \* sizeof(TCHAR). En la devolución, el búfer contiene la cadena terminada en NULL que especifica la ruta de acceso completa del diccionario. Para su uso solo en el editor eudc chino; no se usan en otras aplicaciones.                                                                                  |
| MODO IME \_ ESC \_ \_ HANJA            | Convertir de Hangul a Hanja. En la entrada, *lpData* debe apuntar al búfer que contiene el carácter Hangul que se debe convertir; en la salida, recibe el hanja convertido como una cadena terminada en NULL. Para su uso por parte del editor coreano; no se usan en otras aplicaciones.                                                                                                                                                                                                           |
| NOMBRE DE \_ IME ESC \_ de IME \_              | Recupere el nombre del IME. En la entrada, el *parámetro lpData* debe ser el puntero al búfer para recibir el nombre. En la devolución, el búfer contiene la cadena terminada en NULL que especifica el nombre de IME. Para su uso solo en el editor eudc chino; no se usan en otras aplicaciones. **Windows Me/98/95:** El búfer no debe ser inferior a 16 \* sizeof(TCHAR).<br/> **Windows NT, Windows 2000, Windows XP:** El búfer no debe tener menos de 64 caracteres.<br/> |
| TECLA MÁXIMA \_ DE ESC \_ DE IME \_               | El valor devuelto de la función es el número máximo de llaves para un carácter EUDC. Para su uso solo en el editor eudc chino; no se usan en otras aplicaciones.                                                                                                                                                                                                                                                                                                         |
| COMPATIBILIDAD CON CONSULTAS ESC de IME \_ \_ \_         | Compruebe la implementación. En la entrada, *lpData* apunta al búfer que contiene el valor escape de IME. La función devuelve 0 si no se implementa el escape.                                                                                                                                                                                                                                                                                                             |
| SECUENCIA ESC DE IME \_ \_ A \_ \_ INTERNA | Devuelve el código de carácter que coincide con el código de secuencia especificado. En la entrada, el *parámetro lpData* es el puntero a una variable de 32 bits que contiene el código de secuencia. Para su uso solo en el editor eudc chino; no se usan en otras aplicaciones. Normalmente, el IME chino codificará sus códigos de caracteres de lectura en la secuencia 1 a n.                                                                                                                               |
| DICCIONARIO DE \_ EUDC DEL \_ CONJUNTO DE ESC \_ DE \_ IME  | Establezca el archivo de diccionario EUDC. En la entrada, el *parámetro lpData* es el puntero a una cadena terminada en NULL que especifica la ruta de acceso completa. La ruta de acceso debe ser inferior a 80 \* sizeof(TCHAR). Para su uso solo en el editor eudc chino; no se usan en otras aplicaciones.                                                                                                                                                                                                           |
| IME \_ ESC \_ GETHELPFILENAME        | **Windows Me/98, Windows 2000, Windows XP:** Devuelve el nombre del archivo de ayuda del IME. Al devolver el *parámetro lpData* es la ruta de acceso completa del archivo de ayuda del IME. La ruta de acceso debe ser inferior a 80 \* sizeof(TCHAR).                                                                                                                                                                                                                                                           |



 

El sistema operativo reserva los escapes del intervalo IME \_ ESC RESERVED FIRST a \_ \_ IME ESC RESERVED LAST \_ para su propio \_ \_ uso.

El sistema operativo reserva los escapes del intervalo IME ESC PRIVATE FIRST a IME ESC PRIVATE LAST para su uso privado \_ por parte de los \_ \_ \_ \_ \_ IME.

 

 




