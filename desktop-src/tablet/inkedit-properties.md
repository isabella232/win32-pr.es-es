---
description: Esta sección contiene propiedades que pertenecen al control InkEdit.
ms.assetid: 6aa476b3-97ad-4289-836b-f46fe4d04280
title: Propiedades de InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e7fa3156ef38013ab099e6440b6796505f21d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648437"
---
# <a name="inkedit-properties"></a>Propiedades de InkEdit

Esta sección contiene propiedades que pertenecen al control InkEdit.



| Propiedad                                                 | Descripción                                                                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aspecto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Obtiene o establece un valor que determina si el control [InkEdit](inkedit-control-reference.md) aparece plano o 3D.<br/>                                                                      |
| [**BackColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Obtiene o establece el color de fondo del control [InkEdit](inkedit-control-reference.md) .<br/>                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Obtiene o establece un valor que determina si el control [InkEdit](inkedit-control-reference.md) tiene un borde.<br/>                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Obtiene o establece un valor que determina si las barras de desplazamiento del control [InkEdit](inkedit-control-reference.md) están deshabilitadas.<br/>                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Obtiene o establece los atributos de dibujo de la tinta que todavía se va a dibujar en el control [InkEdit](inkedit-control-reference.md) .<br/>                                                                |
| [**habilitado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Obtiene o establece un valor que determina si el control [InkEdit](inkedit-control-reference.md) puede responder a los eventos generados por el usuario.<br/>                                                     |
| [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Obtiene o establece la constante [Factoid](factoid-constants.md) que usa un objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para restringir su búsqueda para el resultado del reconocimiento.<br/>                  |
| [**Tipo**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Obtiene o establece la fuente del texto que muestra el control [InkEdit](inkedit-control-reference.md) .<br/>                                                                                       |
| [**Identificador**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Obtiene el identificador de ventana al que está enlazado el control [**InkDisp**](inkdisp-class.md) .<br/>                                                                                                      |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Obtiene o establece un valor que especifica cómo se inserta la entrada de lápiz en el control [InkEdit](inkedit-control-reference.md) , ya sea como texto o como entrada de lápiz.<br/>                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Obtiene o establece un valor que especifica si la colección de tintas está deshabilitada, se recopila la tinta o se recopilan los movimientos y las entradas de lápiz.<br/>                                                                |
| [**Bloqueado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Obtiene o establece un valor que especifica si el control [InkEdit](inkedit-control-reference.md) es de solo lectura o no.<br/>                                                                       |
| [**Longitud**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Obtiene o establece un valor que indica si un control [InkEdit](inkedit-control-reference.md) puede contener un número máximo de caracteres y, si es así, especifica el número máximo de caracteres.<br/> |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Obtiene o establece el icono actual del mouse.<br/>                                                                                                                                                 |
| [**MousePointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está sobre una parte determinada del control [InkEdit](inkedit-control-reference.md) .<br/>                |
| [**Ocupa**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Obtiene o establece un valor que indica si se trata de un control [InkEdit](inkedit-control-reference.md) multilínea.<br/>                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Obtiene o establece el período de tiempo, en milisegundos, entre el último objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado y el principio del reconocimiento de texto.<br/>                         |
| [**Reconocedor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Obtiene o establece el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que se va a usar para el reconocimiento.<br/>                                                                                                    |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Obtiene o establece el tipo de barras de desplazamiento que aparecen en el control [InkEdit](inkedit-control-reference.md) .<br/>                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Obtiene o establece la alineación que se va a aplicar a la selección o al punto de inserción actual (solo en tiempo de ejecución).<br/>                                                                                            |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control [InkEdit](inkedit-control-reference.md) está en negrita (solo en tiempo de ejecución).<br/>                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Obtiene o establece si el texto del control [InkEdit](inkedit-control-reference.md) aparece en la línea base, como superíndice o como subíndice (solo en tiempo de ejecución).<br/>                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Obtiene o establece el color del texto de la selección de texto o punto de inserción actual (solo en tiempo de ejecución).<br/>                                                                                               |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Obtiene o establece el nombre de fuente del texto seleccionado en el control [InkEdit](inkedit-control-reference.md) (solo en tiempo de ejecución).<br/>                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Obtiene o establece el tamaño de fuente del texto seleccionado en el control [InkEdit](inkedit-control-reference.md) (solo en tiempo de ejecución).<br/>                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Obtiene o establece la matriz de objetos [**InkDisp**](inkdisp-class.md) insertados (si se muestra como entrada de lápiz) que contiene la selección actual.<br/>                                                      |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Obtiene o establece un valor que permite alternar la apariencia de la selección entre la tinta y el texto.<br/>                                                                                             |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control [InkEdit](inkedit-control-reference.md) está en cursiva (solo en tiempo de ejecución).<br/>                |
| [**LongitudDeSel**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Obtiene o establece el número de caracteres seleccionados en el control [InkEdit](inkedit-control-reference.md) (solo en tiempo de ejecución).<br/>                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Obtiene o establece el texto con formato RTF (formato de texto enriquecido) seleccionado actualmente en el control [InkEdit](inkedit-control-reference.md) (solo en tiempo de ejecución).<br/>                                          |
| [**ComienzoDeSel**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Obtiene o establece el punto inicial del texto que se selecciona en el cuadro de texto (solo en tiempo de ejecución).<br/>                                                                                               |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Obtiene o establece el texto seleccionado en el control [InkEdit](inkedit-control-reference.md) (solo en tiempo de ejecución).<br/>                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control [InkEdit](inkedit-control-reference.md) está subrayado (solo en tiempo de ejecución).<br/>            |
| [**Status**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Obtiene un valor que especifica si el control [InkEdit](inkedit-control-reference.md) está inactivo, recopilando entradas de lápiz o reconocimiento de tinta (solo en tiempo de ejecución).<br/>                                       |
| [**Texto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Obtiene o establece el texto actual del cuadro de texto.<br/>                                                                                                                                              |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Obtiene o establece el texto del control [InkEdit](inkedit-control-reference.md) , incluidos todos los códigos RTF.<br/>                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Obtiene o establece un valor que indica si se puede usar el mouse como dispositivo de entrada.<br/>                                                                                                       |



 

 

 




