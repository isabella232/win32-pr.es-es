---
title: Cómo dar formato al texto en los controles Rich Edit
description: Una aplicación puede enviar mensajes a un control Rich Edit con el fin de dar formato a caracteres y párrafos y recuperar información de formato.
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789363"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a>Cómo dar formato al texto en los controles Rich Edit

Una aplicación puede enviar mensajes a un control Rich Edit con el fin de dar formato a caracteres y párrafos y recuperar información de formato. Los atributos de formato de párrafo incluyen alineación, tabulaciones, sangrías, numeración y tablas simples. En el caso de los caracteres, puede especificar el nombre, el tamaño, el color y los efectos de la fuente, como Bold, Italic y protected.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="format-text-in-a-rich-edit-control"></a>Dar formato al texto en un control Rich Edit

Puede aplicar formato de párrafo mediante el mensaje [**em \_ SETPARAFORMAT**](em-setparaformat.md) . Para determinar el formato de párrafo actual del texto seleccionado, use el [**mensaje \_ GETPARAFORMAT em**](em-getparaformat.md) . La estructura [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) o [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) se usa con ambos mensajes para especificar los atributos de formato de párrafo.

Puede aplicar el formato de caracteres mediante el [**mensaje \_ SETCHARFORMAT em**](em-setcharformat.md) . Para determinar el formato de caracteres actual del texto seleccionado, puede usar el mensaje [**\_ GETCHARFORMAT em**](em-getcharformat.md) . La estructura [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) o [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) se usa con ambos mensajes para especificar atributos de caracteres.

También puede usar los mensajes [**em \_ SETCHARFORMAT**](em-setcharformat.md) y [**em \_ GETCHARFORMAT**](em-getcharformat.md) para establecer y recuperar el formato de caracteres del punto de inserción, que es el formato que se aplica a los caracteres insertados posteriormente. Por ejemplo, si una aplicación establece el formato de caracteres predeterminado en negrita y el usuario escribe un carácter, ese carácter está en negrita.

El formato de caracteres del punto de inserción se aplica al texto recién insertado solo si la selección actual está vacía (si la selección actual es un punto de inserción). De lo contrario, el nuevo texto asume el formato de caracteres del texto que reemplaza. Si cambia la selección, el formato de caracteres predeterminado cambia para coincidir con el primer carácter de la nueva selección.

El efecto de carácter protegido es único en el sentido de que no cambia la apariencia del texto. Si el usuario intenta modificar texto protegido, un control Rich Edit envía a su ventana primaria un código de notificación [ \_ protegido](en-protected.md) , lo que permite a la ventana primaria permitir o impedir el cambio. Para recibir este código de notificación, debe habilitarlo mediante el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

El color de primer plano es siempre un atributo de carácter. En Microsoft Rich Edit 1,0, el color de fondo solo es una propiedad del control Rich Edit. Para establecer el color de fondo predeterminado, utilice el mensaje [**\_ SETBKGNDCOLOR em**](em-setbkgndcolor.md) . Tenga en cuenta que la edición enriquecida no admite el mensaje [**\_ CTLCOLOREDIT de WM**](wm-ctlcoloredit.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




