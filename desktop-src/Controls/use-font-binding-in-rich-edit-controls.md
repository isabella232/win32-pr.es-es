---
title: Cómo usar el enlace de fuentes en controles Rich Edit
description: Microsoft Rich Edit 3,0 asigna un juego de caracteres a caracteres de texto sin formato en función de su contexto.
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17c2f8e0e8c1b57611839a5bbf992f9af6bf65
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103904458"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a>Cómo usar el enlace de fuentes en controles Rich Edit

Microsoft Rich Edit 3,0 asigna un juego de caracteres a caracteres de texto sin formato en función de su contexto. Ejemplos:

-   A los caracteres griegos se les asigna el **\_ juego** de caracteres griego.
-   Los símbolos hangul están asignados al **\_ juego de caracteres hangul**.
-   A los caracteres chinos se les asigna **SHIFTJIS \_ CharSet** si los caracteres kana se encuentran cerca o **GB2312 \_ CharSet** si no se encuentra ningún Kana cerca.
-   A los caracteres ANSI no neutros se les asigna **ANSI \_ CharSet** en cualquier evento.

> [!Note]  
> El control Rich Edit utiliza Unicode internamente, por lo que este uso de juegos de caracteres difiere del original utilizado en las especificaciones de fuente. Sin embargo, la estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) tiene un lugar bien definido para el juego de caracteres.

 

A los caracteres neutros, como los espacios en blanco y los dígitos, se les asigna un juego de caracteres en función de su contexto. Por ejemplo, un espacio en blanco rodeado por caracteres del mismo juego de caracteres obtiene ese juego de caracteres. Los neutros y los dígitos usados para el texto bidireccional son conjuntos de caracteres asignados de forma que se basa en el algoritmo bidireccional Unicode.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-font-binding-in-a-rich-edit-control"></a>Usar el enlace de fuentes en un control Rich Edit

Una vez asignados los juegos de caracteres, la edición enriquecida examina el texto alrededor del punto de inserción hacia delante y hacia atrás para buscar las fuentes más próximas que se han usado para los juegos de caracteres. Si no se encuentra ninguna fuente para un juego de caracteres, Rich Edit usa la fuente elegida por el cliente para ese juego de caracteres. Si el cliente no ha especificado una fuente para el juego de caracteres, Rich Edit usa la fuente predeterminada para ese juego de caracteres. Si el cliente desea algún otro tipo de fuente, el cliente siempre puede cambiarlo, pero este enfoque funcionará la mayor parte del tiempo. Las opciones de fuente predeterminadas actuales se basan en la tabla siguiente. Tenga en cuenta que las fuentes predeterminadas se establecen por proceso y hay listas independientes para el uso de la interfaz de usuario y para el uso de la interfaz de usuario.



| Idioma                    | Nombre de fuente de la interfaz de usuario  | Tamaño de fuente de la interfaz de usuario | nombre de fuente que no es de interfaz de usuario | tamaño de fuente que no es de interfaz de usuario |
|-----------------------------|---------------|--------------|------------------|------------------|
| Western, CE, ME, vietnamita | Tahoma        | 8            | Arial            | 10               |
| Japonés                    | MS UI Gothic  | 9            | MS P Gothic      | 10               |
| Coreano                      | Gulim         | 9            | Gulim            | 9                |
| Chino simplificado          | Simsun        | 9            | SimSun           | 10               |
| Chino tradicional         | PMingLiU      | 9            | PMingLiU         | 9                |
| Tailandés                        | MS Sans Serif | 8            | Tahoma           | 14               |
| Símbolos                     | Wingdings     | 8            | Wingdings        | 10               |
| Devanagari                  | Mangal        | 8            | Mangal           | 10               |
| Tamil                       | Torno         | 8            | Torno            | 10               |
| Georgiano, armenio          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

Por lo tanto, en la tabla de enlace de fuentes predeterminada (las entradas tienen un juego de caracteres, un nombre de fuente y un tamaño), Rich Edit permite \_ que el juego de caracteres ANSI coincida con varios conjuntos de caracteres, mientras que el juego de caracteres adecuado coincide con otras fuentes de uno en uno. Más concretamente, la edición enriquecida utiliza la \_ opción de juego de caracteres ANSI cuando no se encuentra ninguna otra alternativa. Podrá especificar una granularidad más fina que esta; por ejemplo, asigne un juego de \_ caracteres arábigo específico para las ejecuciones árabes, una fuente griega específica para las ejecuciones de griego, etc. Esta granularidad más fina también se utilizará si se encuentra una fuente con el sello del juego de caracteres deseado en alguna parte del documento delante del área a la que se enlaza la fuente.

Tenga en cuenta que la edición enriquecida no controla actualmente un glifo que falta en una fuente que notifica que admite un juego de caracteres pero está incompleto. En el momento de la presentación en un script complejo, la edición enriquecida termina sabiendo que falta dicho glifo, pero no hace que la memoria auxiliar use una nueva fuente. Normalmente, la vinculación de fuentes subyacente del sistema operativo se llevará a cabo.

## <a name="remarks"></a>Observaciones

**Rich Edit 4,1:** Para establecer la fuente predeterminada para un script, llame [**a \_ em SETCHARFORMAT**](em-setcharformat.md) con [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a), especificando valores para los miembros **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** y **LCID** . Además, para obtener la fuente predeterminada de una página de códigos específica, llame a [**em \_ GETCHARFORMAT**](em-getcharformat.md) con **CHARFORMAT2**, especificando los valores de los miembros **bCharSet** y **LCID** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




