---
description: Información general sobre los procedimientos recomendados al usar el objeto del panel de entrada del lápiz.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Prácticas recomendadas (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279386"
---
# <a name="best-practices-tablet-pc"></a>Prácticas recomendadas (Tablet PC)

Hay algunas instrucciones que deben tenerse en cuenta al usar el objeto [**PenInputPanel**](peninputpanel-class.md) .

-   [Preferir el control InkEdit](#prefer-inkedit-control)
-   [Deshabilitar el modo de tinta en los controles InkEdit](#disable-ink-mode-on-inkedit-controls)
-   [Usar controles sin ventana](#using-windowless-controls)
-   [Temas relacionados](#related-topics)

## <a name="prefer-inkedit-control"></a>Preferir el control InkEdit

[InkEdit](inkedit-control-reference.md) es el control preferido al que adjuntar el objeto [**PenInputPanel**](peninputpanel-class.md) . El control InkEdit proporciona compatibilidad con el [marco de trabajo de servicios de texto (TSF)](text-services-framework.md).

## <a name="disable-ink-mode-on-inkedit-controls"></a>Deshabilitar el modo de tinta en los controles InkEdit

Cuando se asocia a un control [InkEdit](inkedit-control-reference.md) , establezca la propiedad [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del control InkEdit en el valor [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) . Si la propiedad **InkMode** no se establece en el valor **InkMode** , el control InkEdit interpreta el primer punteo como un trazo, lo pasa al reconocedor e inserta el texto en el control InkEdit. Puesto que ya tiene un objeto [**PenInputPanel**](peninputpanel-class.md) asociado para aceptar la entrada de lápiz, no es necesario que el control InkEdit también esté habilitado para la entrada de lápiz.

## <a name="using-windowless-controls"></a>Usar controles sin ventana

Cuando un objeto [**PenInputPanel**](peninputpanel-class.md) se adjunta a una ventana primaria que contiene más de un control sin ventana, el objeto **PenInputPanel** no sabe cómo realizar un seguimiento del símbolo de intercalación a medida que el foco se mueve entre los elementos secundarios sin ventanas. La entrada de escritura a mano se puede enviar a un elemento secundario incorrecto cuando el foco se mueve de un control sin ventana a otro mientras está pendiente la entrada.

Para usar el objeto [**PenInputPanel**](peninputpanel-class.md) en un entorno sin ventanas, se puede usar la técnica siguiente:

1.  Cree una instancia de un control [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) y colóquelo sobre el control sin ventana.
2.  Adjunte el objeto [**PenInputPanel**](peninputpanel-class.md) al nuevo control cuadro de texto.
3.  Permita que el control de cuadro de texto recopile el texto reconocido del objeto [**PenInputPanel**](peninputpanel-class.md) .
4.  Cuando el foco cambie fuera del control cuadro de texto, llame al método [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) del objeto [**PenInputPanel**](peninputpanel-class.md) .
5.  Copie el texto reconocido del control de cuadro de texto en el elemento secundario sin ventanas.
6.  Desasocie el objeto [**PenInputPanel**](peninputpanel-class.md) estableciendo su propiedad [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (solo código administrado) o [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) en NULL.
7.  Destruya el control cuadro de texto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Clase PenInputPanel**](peninputpanel-class.md)
</dt> <dt>

[Microsoft. Ink. PenInputPanel](/previous-versions/ms583923(v=vs.100))
</dt> <dt>

[Text Services Framework (TSF)](../tsf/text-services-framework.md)
</dt> </dl>

 

 
