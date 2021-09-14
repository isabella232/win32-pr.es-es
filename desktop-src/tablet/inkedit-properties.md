---
description: Esta sección contiene propiedades que pertenecen al control InkEdit.
ms.assetid: 6aa476b3-97ad-4289-836b-f46fe4d04280
title: Propiedades de InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e7fa3156ef38013ab099e6440b6796505f21d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256688"
---
# <a name="inkedit-properties"></a>Propiedades de InkEdit

Esta sección contiene propiedades que pertenecen al control InkEdit.



| Propiedad                                                 | Descripción                                                                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aspecto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Obtiene o establece un valor que determina si el control [InkEdit](inkedit-control-reference.md) aparece plano o 3D.<br/>                                                                      |
| [**Backcolor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Obtiene o establece el color de fondo del control [InkEdit.](inkedit-control-reference.md)<br/>                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Obtiene o establece un valor que determina si el control [InkEdit](inkedit-control-reference.md) tiene un borde.<br/>                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Obtiene o establece un valor que determina si las barras de desplazamiento del control [InkEdit](inkedit-control-reference.md) están deshabilitadas.<br/>                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Obtiene o establece los atributos de dibujo para la entrada de lápiz que aún no se han dibujado en el control [InkEdit.](inkedit-control-reference.md)<br/>                                                                |
| [**Enabled**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Obtiene o establece un valor que determina si el control [InkEdit](inkedit-control-reference.md) puede responder a eventos generados por el usuario.<br/>                                                     |
| [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Obtiene o establece la [constante Factoid](factoid-constants.md) que usa un [**objeto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para restringir su búsqueda para el resultado del reconocimiento.<br/>                  |
| [**Font**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Obtiene o establece la fuente del texto que muestra el control [InkEdit.](inkedit-control-reference.md)<br/>                                                                                       |
| [**Hwnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Obtiene el identificador de ventana al que está enlazado el control [**InkDisp.**](inkdisp-class.md)<br/>                                                                                                      |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Obtiene o establece un valor que especifica cómo se inserta la entrada de lápiz en el control [InkEdit,](inkedit-control-reference.md) ya sea como texto o como entrada de lápiz.<br/>                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Obtiene o establece un valor que especifica si la colección de entrada de lápiz está deshabilitada, se recopila la entrada de lápiz o se recopilan los gestos y la entrada de lápiz.<br/>                                                                |
| [**Bloqueado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Obtiene o establece un valor que especifica si el control [InkEdit](inkedit-control-reference.md) es de solo lectura o no.<br/>                                                                       |
| [**Maxlength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Obtiene o establece un valor que indica si un control [InkEdit](inkedit-control-reference.md) puede contener un número máximo de caracteres y, si es así, especifica el número máximo de caracteres.<br/> |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Obtiene o establece el icono del mouse personalizado actual.<br/>                                                                                                                                                 |
| [**Mousepointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está sobre una parte determinada del control [InkEdit.](inkedit-control-reference.md)<br/>                |
| [**Multilínea**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Obtiene o establece un valor que indica si se trata de un control [InkEdit multilínea.](inkedit-control-reference.md)<br/>                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Obtiene o establece el tiempo, en milisegundos, entre el último objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) recopilado y el principio del reconocimiento de texto.<br/>                         |
| [**Reconocedor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Obtiene o establece el [**objeto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) que se va a usar para el reconocimiento.<br/>                                                                                                    |
| [**ScrollBars**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Obtiene o establece el tipo de barras de desplazamiento que aparecen en el control [InkEdit.](inkedit-control-reference.md)<br/>                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Obtiene o establece la alineación que se va a aplicar al punto de inserción o selección actual (solo en tiempo de ejecución).<br/>                                                                                            |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control [InkEdit](inkedit-control-reference.md) está en negrita (solo en tiempo de ejecución).<br/>                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Obtiene o establece si el texto del control [InkEdit](inkedit-control-reference.md) aparece en la línea base, como un superíndice o como un subíndice (solo en tiempo de ejecución).<br/>                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Obtiene o establece el color del texto del punto de inserción o selección de texto actual (solo en tiempo de ejecución).<br/>                                                                                               |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Obtiene o establece el nombre de fuente del texto seleccionado en el control [InkEdit](inkedit-control-reference.md) (solo en tiempo de ejecución).<br/>                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Obtiene o establece el tamaño de fuente del texto seleccionado en el control [InkEdit](inkedit-control-reference.md) (solo en tiempo de ejecución).<br/>                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Obtiene o establece la matriz de objetos [**InkDisp**](inkdisp-class.md) incrustados (si se muestran como entrada de lápiz) que contiene la selección actual.<br/>                                                      |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Obtiene o establece un valor que permite alternar la apariencia de la selección entre la entrada de lápiz y el texto.<br/>                                                                                             |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control [InkEdit](inkedit-control-reference.md) está en cursiva (solo en tiempo de ejecución).<br/>                |
| [**Sellength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Obtiene o establece el número de caracteres seleccionados en el control [InkEdit](inkedit-control-reference.md) (solo en tiempo de ejecución).<br/>                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Obtiene o establece el texto con formato Formato de texto enriquecido (RTF) seleccionado actualmente en el control [InkEdit](inkedit-control-reference.md) (solo en tiempo de ejecución).<br/>                                          |
| [**Selstart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Obtiene o establece el punto inicial del texto seleccionado en el cuadro de texto (solo en tiempo de ejecución).<br/>                                                                                               |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Obtiene o establece el texto seleccionado en el control [InkEdit](inkedit-control-reference.md) (solo en tiempo de ejecución).<br/>                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Obtiene o establece un valor que especifica si el estilo de fuente del texto seleccionado actualmente en el control [InkEdit](inkedit-control-reference.md) está subrayado (solo en tiempo de ejecución).<br/>            |
| [**Estado**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Obtiene un valor que especifica si el control [InkEdit](inkedit-control-reference.md) está inactivo, recopilando entrada de lápiz o reconociendo la entrada de lápiz (solo en tiempo de ejecución).<br/>                                       |
| [**Texto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Obtiene o establece el texto actual del cuadro de texto.<br/>                                                                                                                                              |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Obtiene o establece el texto del control [InkEdit,](inkedit-control-reference.md) incluidos todos los códigos RTF.<br/>                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Obtiene o establece un valor que indica si el mouse se puede usar como dispositivo de entrada.<br/>                                                                                                       |



 

 

 




