---
title: Cómo usar la información de saltos de línea y de palabra
description: Un control Rich Edit llama a una función denominada procedimiento de separación de palabras para buscar saltos entre palabras y para determinar dónde se pueden dividir las líneas.
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb90064e455bfeb8ee126e6107d75ef29b3a4f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656423"
---
# <a name="how-to-use-word-and-line-break-information"></a>Cómo usar la información de saltos de línea y de palabra

Un control Rich Edit llama a una función denominada procedimiento de separación de palabras para buscar saltos entre palabras y para determinar dónde se pueden dividir las líneas. El control utiliza esta información al realizar operaciones de ajuste de texto y al procesar las combinaciones de teclas CTRL + flecha izquierda y CTRL + flecha derecha. Una aplicación puede enviar mensajes a un control Rich Edit para reemplazar el procedimiento predeterminado de separación de palabras, para recuperar información de separación de palabras y para determinar en qué línea cae un carácter determinado.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-word-and-line-break-information"></a>Usar información de saltos de línea y de palabra

Los procedimientos de separación de palabras para controles Rich Edit son similares a los de los controles de edición, pero tienen funcionalidades adicionales: los procedimientos de separación de palabras para ambos tipos de controles pueden determinar si un carácter es un delimitador y buscar el salto de palabra más cercano antes o después de la posición especificada. Un delimitador es un carácter que marca el final de una palabra, como un espacio. Normalmente, en un control de edición, se produce un salto de palabra solo después de los delimitadores. Sin embargo, las diferentes reglas se aplican a la mayoría de los idiomas asiáticos.

Los procedimientos de separación de palabras para controles Rich Edit también agrupan caracteres en clases de caracteres, cada una identificada por un valor en el intervalo de 0x00 a 0x0F. Los saltos se producen después de los delimitadores o entre los caracteres de clases diferentes. Por lo tanto, un procedimiento de separación de palabras con diferentes clases para caracteres alfanuméricos y de puntuación encontraría dos saltos de palabra en la cadena "Win.doc" (antes y después del punto).

La clase de un carácter puede combinarse con cero o más marcas de separación de palabras para formar un valor de 8 bits. Cuando se realizan operaciones de ajuste automático de línea, un control Rich Edit usa marcas de separación de palabras para determinar dónde se pueden dividir las líneas. Rich Edit usa las siguientes marcas de salto de palabra.



| Marca            | Descripción                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| WBF ( \_ BREAKAFTER) | Las líneas pueden romperse después del carácter.                                                                                          |
| WBF \_ BreakLine  | El carácter es un delimitador. Los delimitadores marcan los extremos de las palabras. Las líneas pueden romperse después de los delimitadores.                            |
| WBF \_ ISWHITE    | El carácter es un carácter de espacio en blanco. Los caracteres de espacio en blanco finales no se incluyen en la longitud de una línea al ajustar. |



 

El \_ valor de BREAKAFTER WBF se usa para permitir el ajuste después de un carácter que no marca el final de una palabra, como un guión.

Puede reemplazar el procedimiento predeterminado de separación de palabras para un control Rich Edit por su propio procedimiento mediante el mensaje [**\_ SETWORDBREAKPROC em**](em-setwordbreakproc.md) . Para obtener más información sobre los procedimientos de separación de palabras, vea la descripción de la función [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .

> [!Note]  
> Este reemplazo no se recomienda para Microsoft Rich Edit 2,0 y versiones posteriores, debido a la complejidad de la separación de palabras multilingües.

 

En el caso de Microsoft Rich Edit 1,0, puede usar el mensaje [**em \_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) para reemplazar el procedimiento extendido de separación de palabras predeterminado por una función [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) . Esta función proporciona información adicional sobre el texto, como el juego de caracteres. Puede usar el mensaje [**\_ GETWORDBREAKPROCEX em**](em-getwordbreakprocex.md) para recuperar la dirección del procedimiento extendido de separación de palabras actual. Tenga en cuenta que Microsoft Rich Edit 2,0 y versiones posteriores no admiten *EditWordBreakProcEx*, **em \_ GETWORDBREAKPROCEX** y **em \_ SETWORDBREAKPROCEX**.

Puede usar el mensaje [**\_ FINDWORDBREAK em**](em-findwordbreak.md) para buscar saltos de palabra o para determinar la clase de un carácter y las marcas de separación de palabras. A su vez, el control llama a su procedimiento de separación de palabras para obtener la información solicitada.

Para determinar en qué línea cae un carácter determinado, puede usar el mensaje [**\_ EXLINEFROMCHAR em**](em-exlinefromchar.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 