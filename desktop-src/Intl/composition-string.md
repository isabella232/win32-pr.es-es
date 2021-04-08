---
description: La cadena de composición es el texto actual de la ventana de composición.
ms.assetid: ab226567-f68d-4fa4-9ead-e9bfabde927e
title: Cadena de composición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5cb63163ca9a8076edc4d01053e4baeffc619c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002089"
---
# <a name="composition-string"></a>Cadena de composición

La cadena de composición es el texto actual de la ventana de composición. Este es el texto que el IME convierte en caracteres finales. Cada cadena de composición se compone de una o más "cláusulas". Una cláusula es la combinación más pequeña de caracteres que el IME puede convertir en un carácter final. Para obtener y establecer la cadena de composición, la aplicación llama a las funciones [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) y [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) , respectivamente.

A medida que el usuario escribe texto en la ventana de composición, el IME realiza un seguimiento del estado de la cadena de composición. Este estado incluye información de atributos, información de cláusulas, información de escritura y posición del cursor. La aplicación puede recuperar el estado de composición mediante la función [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) .

La información de atributos se representa en una matriz de valores de 8 bits que especifica el estado de los caracteres de la cadena de composición. Todos los caracteres de una cláusula deben tener el mismo atributo. La matriz incluye un valor para cada byte de la cadena, incluido un byte cada uno para el cliente potencial y el segundo bytes de cualquier carácter de doble byte de la cadena. Para cada valor de la matriz, los bits 0 a 3 pueden ser una combinación de los valores siguientes.



| Value                      | Significado                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| entrada de ATTR \_                | Carácter que está escribiendo el usuario. El IME todavía tiene que convertir este carácter.                           |
| \_error de entrada de ATTR \_         | Un carácter de error que el IME no puede convertir. Por ejemplo, el IME no puede unir algunas consonantes. |
| destino de atributo \_ \_ convertido    | Carácter seleccionado por el usuario y convertido por el IME.                                             |
| ATTR \_ convertido            | Carácter que el IME ya ha convertido.                                                             |
| destino de ATTR \_ \_ NOTCONVERTED | Carácter que se va a convertir. El usuario ha seleccionado este carácter, pero el IME todavía no lo ha convertido.     |
| ATTR \_ FIXEDCONVERTED       | Caracteres que el IME dejará de convertir.                                                           |



 

Todos los demás valores están reservados. En japonés, cualquier carácter no convertido que tenga el \_ atributo de entrada ATTR es un carácter hiragana, Katakana o alfanumérico. En Coreano, este atributo representa un carácter hangul que el IME todavía no ha convertido. En chino tradicional y chino simplificado, cada IME puede limitar su carácter dentro de algún intervalo.

La información de la cláusula incluida en el estado de la cadena de composición es una matriz de valores de 32 bits que especifica las posiciones de las cláusulas en la cadena de composición. La matriz incluye un valor para cada cláusula y un valor final que especifica la longitud de la cadena completa. Cada valor de la matriz especifica el desplazamiento, en bytes, desde el principio de la cadena hasta la cláusula. El primer valor siempre es 0 porque la primera cláusula siempre comienza al principio de la cadena. Por ejemplo, si una cadena tiene dos cláusulas, la información de la cláusula tiene tres valores: el primer valor es 0, el segundo valor es el desplazamiento de la segunda cláusula y el tercer valor es la longitud de la cadena. En el caso de Unicode, la posición de una cláusula se cuenta en caracteres Unicode y la longitud de una cadena es el tamaño en caracteres Unicode.

La información de escritura incluida en el estado de la cadena de composición es una cadena de caracteres terminada en null que representa los caracteres que el usuario escribe en el teclado.

La posición del cursor incluida en el estado de la cadena de composición es un valor que indica la posición del cursor con respecto a los caracteres de la cadena de composición. El valor es el desplazamiento, en bytes, desde el principio de la cadena. Si este valor es 0, el cursor está inmediatamente antes del primer carácter de la cadena. Si el valor es igual a la longitud de la cadena, el cursor está inmediatamente después del último carácter. Si el valor es 1, el cursor no está presente. En el caso de Unicode, la posición y la longitud se miden en caracteres Unicode.

La aplicación puede establecer la cadena o los elementos de composición del estado de composición mediante la función [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) . Para asegurarse de que la ventana de composición actualiza su apariencia en función de estos cambios, la función permite que la aplicación envíe un mensaje de notificación a la ventana. Las aplicaciones que establecen una combinación de elementos de estado de composición suelen deshabilitar las notificaciones de todas las llamadas a esta función, excepto la última, para que solo se genere un mensaje de notificación para la ventana de composición.

Por último, el control de edición admite dos mensajes para cambiar el control de las cadenas de composición por el IME. Para obtener más información, consulte [**em \_ GETIMESTATUS**](../controls/em-getimestatus.md) y [**em \_ SETIMESTATUS**](../controls/em-setimestatus.md). Para obtener más información sobre el control de edición, vea [control de edición](../controls/edit-controls.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
