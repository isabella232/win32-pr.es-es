---
title: Uso de la información de saltos de línea y palabras
description: Un control de edición enriquecido llama a una función denominada procedimiento de salto de palabras para buscar saltos entre palabras y determinar dónde puede interrumpir las líneas.
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178770ce4a7206c18f6fbbc197d92e23ff0139ae637bd5f7ceb4159aee3270ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059699"
---
# <a name="how-to-use-word-and-line-break-information"></a>Uso de la información de saltos de línea y palabras

Un control de edición enriquecido llama a una función denominada procedimiento de salto de palabras para buscar saltos entre palabras y determinar dónde puede interrumpir las líneas. El control usa esta información al realizar operaciones de ajuste de palabras y al procesar las combinaciones de teclas CTRL+FLECHA IZQUIERDA y CTRL+FLECHA DERECHA. Una aplicación puede enviar mensajes a un control de edición enriquecido para reemplazar el procedimiento predeterminado de salto de palabras, recuperar información de salto de palabras y determinar en qué línea se encuentra un carácter determinado.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-word-and-line-break-information"></a>Usar información de saltos de línea y palabras

Los procedimientos de salto de palabras para controles de edición enriquecidos son similares a los de los controles de edición, pero tienen funcionalidades adicionales: los procedimientos de salto de palabras para ambos tipos de controles pueden determinar si un carácter es un delimitador y pueden encontrar el salto de palabras más cercano antes o después de la posición especificada. Un delimitador es un carácter que marca el final de una palabra, como un espacio. Normalmente, en un control de edición, solo se produce un salto de palabras después de los delimitadores. Sin embargo, se aplican reglas diferentes a la mayoría de los idiomas asiáticos.

Los procedimientos de salto de palabras para controles de edición enriquecidos también agrupan caracteres en clases de caracteres, cada una identificada por un valor del intervalo 0x00 a 0x0F. Los saltos se producen después de delimitadores o entre caracteres de clases diferentes. Por lo tanto, un procedimiento de salto de palabras con clases diferentes para caracteres alfanuméricos y de puntuación encontraría dos saltos de palabras en la cadena "Win.doc" (antes y después del punto).

La clase de un carácter se puede combinar con cero o más marcas de salto de palabras para formar un valor de 8 bits. Al realizar operaciones de ajuste de palabras, un control de edición enriquecido usa marcas de salto de palabras para determinar dónde puede interrumpir las líneas. Rich Edit usa las siguientes marcas de salto de palabras.



| Marca            | Descripción                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| WBF \_ BREAKAFTER | Las líneas se pueden dividir después del carácter.                                                                                          |
| WBF \_ BREAKLINE  | El carácter es un delimitador. Los delimitadores marcan los extremos de las palabras. Las líneas se pueden dividir después de los delimitadores.                            |
| WBF \_ ISWHITE    | El carácter es un carácter de espacio en blanco. Los caracteres de espacio en blanco finales no se incluyen en la longitud de una línea al ajustar. |



 

El valor WBF BREAKAFTER se usa para permitir el ajuste después de un carácter que no marca el final de una \_ palabra, como un guion.

Puede reemplazar el procedimiento predeterminado de salto de palabras para un control de edición enriquecido por su propio procedimiento mediante el mensaje [**\_ SETWORDBREAKPROC de EM.**](em-setwordbreakproc.md) Para obtener más información sobre los procedimientos de salto de palabras, vea la descripción de la [*función EditWordBreakProc.*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)

> [!Note]  
> Este reemplazo no se recomienda para Microsoft Rich Edit 2.0 y versiones posteriores, debido a la complejidad de la separación multilingüe de palabras.

 

Para Microsoft Rich Edit 1.0, puede usar el mensaje [**EM \_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) para reemplazar el procedimiento de salto de palabras extendido predeterminado por una [*función EditWordBreakProcEx.*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) Esta función proporciona información adicional sobre el texto, como el juego de caracteres. Puede usar el mensaje [**EM \_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) para recuperar la dirección del procedimiento de salto de palabras extendido actual. Tenga en cuenta que Microsoft Rich Edit 2.0 y versiones posteriores no *admiten EditWordBreakProcEx,* **EM \_ GETWORDBREAKPROCEX** y **EM \_ SETWORDBREAKPROCEX**.

Puede usar el mensaje [**EM \_ FINDWORDBREAK**](em-findwordbreak.md) para buscar saltos de palabras o para determinar las marcas de clase y de salto de palabras de un carácter. A su vez, el control llama a su procedimiento de separación de palabras para obtener la información solicitada.

Para determinar en qué línea se encuentra un carácter determinado, puede usar el [**mensaje EM \_ EXLINEFROMCHAR.**](em-exlinefromchar.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles rich edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 