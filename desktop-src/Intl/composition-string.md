---
description: La cadena de composición es el texto actual de la ventana de composición.
ms.assetid: ab226567-f68d-4fa4-9ead-e9bfabde927e
title: Cadena de composición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a547b4383c95b99025b779de2950c8325af56a3397603db10199474dfe20ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430995"
---
# <a name="composition-string"></a>Cadena de composición

La cadena de composición es el texto actual de la ventana de composición. Este es el texto que el IME convierte en caracteres finales. Cada cadena de composición consta de una o varias "cláusulas". Una cláusula es la combinación más pequeña de caracteres que el IME puede convertir en un carácter final. Para obtener y establecer la cadena de composición, la aplicación llama a las funciones [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) e [**ImmSetCompositionString,**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) respectivamente.

A medida que el usuario escribe texto en la ventana de composición, el IME realiza un seguimiento del estado de la cadena de composición. Este estado incluye información de atributos, información de cláusulas, información de escritura y posición del cursor. La aplicación puede recuperar el estado de composición mediante la [**función ImmGetCompositionString.**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)

La información del atributo se representa en una matriz de valores de 8 bits que especifica el estado de los caracteres de la cadena de composición. Todos los caracteres de una cláusula deben tener el mismo atributo. La matriz incluye un valor para cada byte de la cadena, incluido un byte cada uno para el cliente potencial y los segundos bytes de cualquier carácter de doble byte de la cadena. Para cada valor de la matriz, los bits del 0 al 3 pueden ser una combinación de los valores siguientes.



| Value                      | Significado                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| ENTRADA \_ ATTR                | Carácter especificado por el usuario. El IME aún no ha convertido este carácter.                           |
| ERROR DE ENTRADA DE ATTR \_ \_         | Carácter de error que el IME no puede convertir. Por ejemplo, el IME no puede reunir algunas consonantes. |
| DESTINO ATTR \_ \_ CONVERTIDO    | Carácter seleccionado por el usuario y convertido por el IME.                                             |
| ATTR \_ CONVERTIDO            | Carácter que el IME ya ha convertido.                                                             |
| DESTINO DE ATTR \_ \_ NO CONVERTIDO | Carácter que se va a convertir. El usuario ha seleccionado este carácter, pero el IME aún no lo ha convertido.     |
| ATTR \_ FIXEDCONVERTED       | Caracteres que el IME ya no convertirá.                                                           |



 

Todos los demás valores están reservados. En japonés, cualquier carácter sin convertir que tenga el atributo ATTR INPUT es un \_ carácter hiragana, katakana o alfanumérico. En coreano, este atributo representa un carácter Hangul que el IME aún no ha convertido. En chino tradicional y chino simplificado, cada IME puede limitar su carácter dentro de un intervalo.

La información de cláusula incluida en el estado de la cadena de composición es una matriz de valores de 32 bits que especifica las posiciones de las cláusulas en la cadena de composición. La matriz incluye un valor para cada cláusula y un valor final que especifica la longitud de la cadena completa. Cada valor de la matriz especifica el desplazamiento, en bytes, desde el principio de la cadena hasta la cláusula . El primer valor siempre es 0 porque la primera cláusula siempre comienza al principio de la cadena. Por ejemplo, si una cadena tiene dos cláusulas, la información de la cláusula tiene tres valores: el primer valor es 0, el segundo es el desplazamiento de la segunda cláusula y el tercer valor es la longitud de la cadena. Para Unicode, la posición de una cláusula se cuenta en caracteres Unicode y la longitud de una cadena es el tamaño en caracteres Unicode.

La información de escritura incluida en el estado de la cadena de composición es una cadena de caracteres terminada en NULL que representa los caracteres que el usuario escribe en el teclado.

La posición del cursor incluida en el estado de la cadena de composición es un valor que indica la posición del cursor con respecto a los caracteres de la cadena de composición. El valor es el desplazamiento, en bytes, del principio de la cadena. Si este valor es 0, el cursor está inmediatamente antes del primer carácter de la cadena. Si el valor es igual a la longitud de la cadena, el cursor está inmediatamente después del último carácter. Si el valor es 1, el cursor no está presente. Para Unicode, tanto la posición como la longitud se miden en caracteres Unicode.

La aplicación puede establecer la cadena de composición o los elementos del estado de composición mediante la [**función ImmSetCompositionString.**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) Para asegurarse de que la ventana de composición actualiza su apariencia en función de estos cambios, la función permite a la aplicación enviar un mensaje de notificación a la ventana. Las aplicaciones que establecen una combinación de elementos de estado de composición suelen deshabilitar las notificaciones de todas las llamadas, menos la última llamada a esta función, para que solo se genere un mensaje de notificación para la ventana de composición.

Por último, el control de edición admite dos mensajes para cambiar el control de cadenas de composición por parte del IME. Para obtener más información, [**vea EM \_ GETIMESTATUS**](../controls/em-getimestatus.md) y [**EM \_ SETIMESTATUS**](../controls/em-setimestatus.md). Para obtener más información sobre el control de edición, vea [Editar control](../controls/edit-controls.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del Administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
