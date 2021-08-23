---
description: Rich Edit 3.0 admite el IME HexToUnicode, que permite a un usuario convertir entre caracteres hexadecimales y Unicode mediante teclas de acceso rápido de una de estas dos maneras.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: HexToUnicode IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a57ce56821f200c9fd9ff80560908f5a72ecfdb0f51ce981e1aff40ce785b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068155"
---
# <a name="hextounicode-ime"></a>HexToUnicode IME

Rich Edit 3.0 admite el IME HexToUnicode, que permite a un usuario convertir entre caracteres hexadecimales y Unicode mediante teclas de acceso rápido de una de estas dos maneras.

Con el primer método de conversión, el usuario escribe el código de carácter en hexadecimal y, a continuación, escribe ALT+X. El IME reemplaza los dígitos hexadecimales que preceden al punto de inserción por el carácter Unicode. Si la fuente actual no admite el código de caracteres, se elige una fuente adecuada que la admita. Para convertir de Unicode a hexadecimal, el usuario escribe MAYÚS+ALT+X. Esta entrada reemplaza el carácter Unicode que precede al punto de inserción por los dígitos hexadecimales. En concreto, este método permite al usuario determinar el carácter indicado por un indicador de "glifo que falta". Si el código de caracteres hexadecimales sigue inmediatamente algunos caracteres hexadecimales legítimos (sin caracteres), el usuario selecciona los dígitos específicos que se convertirán antes de escribir ALT+X. Un problema con este primer método es que ALT+X a veces se usa como combinación de claves para el comando exit (es decir, eXit). Por ejemplo, en Microsoft Office, este comando solo aparece como una opción del **menú** Archivo.

El segundo método de conversión entre caracteres hexadecimales y Unicode implica el panel numérico. Con este método, el usuario escribe números ALT+NumPad (con valores mayores que 255) para escribir caracteres Unicode mediante valores decimales. Este método no es tan útil como el primero porque el usuario no puede ver qué dígitos hexadecimales se han especificado. Además, el usuario no puede corregir los dígitos hexadecimales excepto al volver a escribir todos los dígitos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del Administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 



