---
description: Información general sobre los procedimientos recomendados al usar el objeto de panel de entrada de lápiz.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Procedimientos recomendados (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571444"
---
# <a name="best-practices-tablet-pc"></a>Procedimientos recomendados (Tablet PC)

Hay algunas directrices que debe tener en cuenta al usar el [**objeto PenInputPanel.**](peninputpanel-class.md)

-   [Preferir el control InkEdit](#prefer-inkedit-control)
-   [Deshabilitar el modo de entrada de lápiz en controles InkEdit](#disable-ink-mode-on-inkedit-controls)
-   [Usar controles sin ventanas](#using-windowless-controls)
-   [Temas relacionados](#related-topics)

## <a name="prefer-inkedit-control"></a>Preferir el control InkEdit

[InkEdit](inkedit-control-reference.md) es el control preferido al que se va a adjuntar [**el objeto PenInputPanel.**](peninputpanel-class.md) El control InkEdit proporciona compatibilidad con el [Text Services Framework (TSF).](text-services-framework.md)

## <a name="disable-ink-mode-on-inkedit-controls"></a>Deshabilitar el modo de entrada de lápiz en controles InkEdit

Cuando se adjunta a un control [InkEdit,](inkedit-control-reference.md) establezca la [**propiedad InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del control InkEdit en el [**valor InkMode.**](/windows/desktop/api/inked/ne-inked-inkmode) Si la **propiedad InkMode** no está establecida en el valor **InkMode,** el control InkEdit interpreta la primera pulsación como un trazo, la pasa al reconocedor e inserta el texto en el control InkEdit. Puesto que ya tiene un [**objeto PenInputPanel**](peninputpanel-class.md) asociado para aceptar la entrada de entrada de lápiz, no es necesario que el control InkEdit también esté habilitado para la entrada de lápiz.

## <a name="using-windowless-controls"></a>Usar controles sin ventanas

Cuando un objeto [**PenInputPanel**](peninputpanel-class.md) se adjunta a una ventana primaria que contiene más de un control sin ventana, el objeto **PenInputPanel** no sabe cómo realizar el seguimiento del elemento de referencia a medida que el foco se mueve entre los elementos secundarios sin ventana. La entrada de escritura a mano se puede enviar al elemento secundario incorrecto cuando el foco se mueve de un control sin ventana a otro mientras la entrada está pendiente.

Para usar el [**objeto PenInputPanel**](peninputpanel-class.md) en un entorno sin ventanas, se puede usar la siguiente técnica:

1.  Cree una instancia de un control [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) y posiciones sobre el control sin ventanas.
2.  [**Adjunte el objeto PenInputPanel**](peninputpanel-class.md) al nuevo control de cuadro de texto.
3.  Deje que el control de cuadro de texto recopile el texto reconocido del [**objeto PenInputPanel.**](peninputpanel-class.md)
4.  Cuando el foco cambie fuera del control de cuadro de texto, llame al [**método CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) del [**objeto PenInputPanel.**](peninputpanel-class.md)
5.  Copie el texto reconocido del control de cuadro de texto en el elemento secundario sin ventanas.
6.  Desasoyte el [**objeto PenInputPanel**](peninputpanel-class.md) estableciendo su propiedad [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (solo código administrado) o la propiedad [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) en null.
7.  Destruya el control de cuadro de texto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**PenInputPanel (clase)**](peninputpanel-class.md)
</dt> <dt>

[Microsoft.Ink.PenInputPanel](/previous-versions/ms583923(v=vs.100))
</dt> <dt>

[Text Services Framework (TSF)](../tsf/text-services-framework.md)
</dt> </dl>

 

 
