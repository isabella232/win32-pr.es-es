---
title: Cómo dar formato al texto en controles Rich Edit
description: Una aplicación puede enviar mensajes a un control de edición enriquecido para dar formato a caracteres y párrafos y recuperar información de formato.
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062012"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a>Cómo dar formato al texto en controles Rich Edit

Una aplicación puede enviar mensajes a un control de edición enriquecido para dar formato a caracteres y párrafos y recuperar información de formato. Los atributos de formato de párrafo incluyen alineación, tabulaciones, sangrías, numeración y tablas simples. Para los caracteres, puede especificar el nombre de fuente, el tamaño, el color y los efectos, como negrita, cursiva y protegido.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="format-text-in-a-rich-edit-control"></a>Dar formato al texto en un control Rich Edit

Puede aplicar formato de párrafo mediante el mensaje [**EM \_ SETPARAFORMAT.**](em-setparaformat.md) Para determinar el formato de párrafo actual para el texto seleccionado, use el [**mensaje EM \_ GETPARAFORMAT.**](em-getparaformat.md) La [**estructura PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) o [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) se usa con ambos mensajes para especificar atributos de formato de párrafo.

Puede aplicar el formato de caracteres mediante el mensaje [**EM \_ SETCHARFORMAT.**](em-setcharformat.md) Para determinar el formato de caracteres actual para el texto seleccionado, puede usar el [**mensaje EM \_ GETCHARFORMAT.**](em-getcharformat.md) La [**estructura CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) o [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) se usa con ambos mensajes para especificar atributos de caracteres.

También puede usar mensajes [**EM \_ SETCHARFORMAT**](em-setcharformat.md) y [**EM \_ GETCHARFORMAT**](em-getcharformat.md) para establecer y recuperar el formato de caracteres del punto de inserción, que es el formato que se aplica a los caracteres insertados posteriormente. Por ejemplo, si una aplicación establece el formato de caracteres predeterminado en negrita y el usuario, a continuación, los tipos de un carácter, ese carácter está en negrita.

El formato de caracteres del punto de inserción se aplica al texto recién insertado solo si la selección actual está vacía (si la selección actual es un punto de inserción). De lo contrario, el nuevo texto asume el formato de caracteres del texto que reemplaza. Si cambia la selección, el formato de caracteres predeterminado cambia para que coincida con el primer carácter de la nueva selección.

El efecto de carácter protegido es único, ya que no cambia la apariencia del texto. Si el usuario intenta modificar el texto protegido, un control rich edit envía a su ventana primaria un código de notificación [EN \_ PROTECTED,](en-protected.md) lo que permite que la ventana primaria permita o impida el cambio. Para recibir este código de notificación, debe habilitarlo mediante el mensaje [**EM \_ SETEVENTMASK.**](em-seteventmask.md)

El color de primer plano siempre es un atributo de carácter. En Microsoft Rich Edit 1.0, el color de fondo es solo una propiedad del control rich edit. Para establecer el color de fondo predeterminado, use el [**mensaje EM \_ SETBNDCOLOR.**](em-setbkgndcolor.md) Tenga en cuenta que Rich Edit no admite el [**mensaje \_ WM CTLCOLOREDIT.**](wm-ctlcoloredit.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles rich edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




