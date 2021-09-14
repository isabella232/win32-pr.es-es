---
title: Cómo usar el enlace de fuentes en controles Rich Edit
description: Microsoft Rich Edit 3.0 asigna un juego de caracteres a caracteres de texto sin formato en función de su contexto.
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17c2f8e0e8c1b57611839a5bbf992f9af6bf65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165418"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a>Cómo usar el enlace de fuentes en controles Rich Edit

Microsoft Rich Edit 3.0 asigna un juego de caracteres a caracteres de texto sin formato en función de su contexto. Ejemplos:

-   Los caracteres griegos se **asignan a GREEK \_ CHARSET.**
-   A los símbolos hangul se **les asigna HANGUL \_ CHARSET.**
-   A los caracteres chino se les asigna **MAYÚSJIS \_ CHARSET** si se encuentran caracteres kana cerca o **GB2312 \_ CHARSET** si no se encuentra ningún kana cerca.
-   Los caracteres ANSI no neutros se asignan **a ANSI \_ CHARSET** en cualquier evento.

> [!Note]  
> El control de edición enriquecido usa Unicode internamente, por lo que este uso de juegos de caracteres difiere del original que se usa en las especificaciones de fuente. Pero la [**estructura CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) tiene un lugar bien definido para el juego de caracteres.

 

A los caracteres neutros, como los espacios en blanco y los dígitos, se les asigna un juego de caracteres en función de su contexto. Por ejemplo, un espacio en blanco rodeado de caracteres del mismo juego de caracteres obtiene ese juego de caracteres. Los neutros y dígitos usados para el texto bidireccional se asignan a los juegos de caracteres de una manera que se basa en el algoritmo bidireccional Unicode.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-font-binding-in-a-rich-edit-control"></a>Usar enlace de fuentes en un control Rich Edit

Una vez asignados los juegos de caracteres, Rich Edit examina el texto alrededor del punto de inserción hacia delante y hacia atrás para buscar las fuentes más cercanas que se han usado para los juegos de caracteres. Si no se encuentra ninguna fuente para un juego de caracteres, Rich Edit usa la fuente elegida por el cliente para ese juego de caracteres. Si el cliente no ha especificado una fuente para el juego de caracteres, Rich Edit usa la fuente predeterminada para ese juego de caracteres. Si el cliente quiere alguna otra fuente, el cliente siempre puede cambiarla, pero este enfoque funcionará la mayoría de las veces. Las opciones de fuente predeterminadas actuales se basan en la tabla siguiente. Tenga en cuenta que las fuentes predeterminadas se establecen por proceso y hay listas independientes para el uso de la interfaz de usuario y para el uso que no es de la interfaz de usuario.



| Lenguaje                    | Nombre de fuente de la interfaz de usuario  | Tamaño de fuente de la interfaz de usuario | nombre de fuente que no es de interfaz de usuario | tamaño de fuente que no es de interfaz de usuario |
|-----------------------------|---------------|--------------|------------------|------------------|
| Oeste, CE, ME, Insólote | Tahoma        | 8            | Arial            | 10               |
| Japonés                    | MS UI Desasoyte  | 9            | MS P Desa eso      | 10               |
| Coreano                      | Gulim         | 9            | Gulim            | 9                |
| Chino simplificado          | Simsun        | 9            | SimSun           | 10               |
| Chino tradicional         | PMingLiU      | 9            | PMingLiU         | 9                |
| Tailandés                        | MS Sans Serif | 8            | Tahoma           | 14               |
| Símbolos                     | Wingdings     | 8            | Wingdings        | 10               |
| Devanagari                  | Mangal        | 8            | Mangal           | 10               |
| Tamil                       | Laxa         | 8            | Laxa            | 10               |
| Armenio, Armenio          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

Por lo tanto, en la tabla de enlace de fuentes predeterminada (las entradas tienen un juego de caracteres, un nombre de fuente y un tamaño), Rich Edit permite que ANSI CHARSET coincida con varios juegos de caracteres, mientras que el juego de caracteres adecuado coincide con otras fuentes uno \_ a uno. Más concretamente, la edición enriquecte usa la opción \_ ANSI CHARSET siempre que no se encuentra ninguna otra alternativa. Podrá especificar una granularidad más fina que esta; Por ejemplo, asigne un CHARSET árabe específico para las ejecuciones en árabe, una fuente de griego específica para \_ las ejecuciones de griego, y así sucesivamente. Esta granularidad más fina también se usará si se encuentra una fuente con la marca de juego de caracteres deseada en algún lugar del documento antes del área enlazada a la fuente.

Tenga en cuenta que la edición enriquecida no controla actualmente un glifo que falta en una fuente que dice admitir un juego de caracteres, pero está incompleta. En tiempo de presentación en un script complejo, La edición enriquecida termina sabiendo que falta un glifo de este tipo, pero no hace que el almacén de respaldo use una nueva fuente. Normalmente, la vinculación de fuente subyacente del sistema operativo lo logrará.

## <a name="remarks"></a>Observaciones

**Rich Edit 4.1:** Para establecer la fuente predeterminada de un script, llame a [**EM \_ SETCHARFORMAT**](em-setcharformat.md) con [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a), especificando valores para los miembros **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** y **lcid.** Además, para obtener la fuente predeterminada de una página de códigos específica, llame a [**EM \_ GETCHARFORMAT**](em-getcharformat.md) con **CHARFORMAT2,** especificando valores para los **miembros bCharSet** **y lcid.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles rich edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




