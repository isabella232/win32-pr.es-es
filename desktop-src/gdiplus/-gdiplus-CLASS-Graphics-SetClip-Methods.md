---
description: En este tema se enumeran los métodos SetClip de la clase Graphics. Para obtener una lista completa de los métodos de la clase Graphics, vea Graphics.
ms.assetid: e8348373-da79-4d33-8bea-d594985493d4
title: Métodos Graphics.SetClip
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 616a78aa7dd251e888bba1186a3583c5d7f62d188dcc6313560f651ec6558827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037193"
---
# <a name="graphicssetclip-methods"></a>Métodos Graphics.SetClip

En este tema se enumeran los métodos SetClip de la [**clase Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Para obtener una lista completa de los métodos de la **clase Graphics,** vea [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetClip(HRGN,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode))                     | El [**método Graphics::SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode)) actualiza la región de recorte de este objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de sí mismo y una región GDI.<br/>                                                                                                                                                                                                          |
| [**SetClip(Rect&,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode))   | El [**método Graphics::SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode)) actualiza la región de recorte de este objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de sí mismo y un rectángulo.<br/>                                                                                                                                                                                          |
| [**SetClip(RectF&,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) | El [**método Graphics::SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) actualiza la región de recorte de este objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de sí mismo y un rectángulo.<br/>                                                                                                                                                                                         |
| [**SetClip(Region \* ,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))               | El [**método Graphics::SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) actualiza la región de recorte de este objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de sí mismo y la región especificada por un [**objeto Region.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region)<br/>                                                                                                                                      |
| [**SetClip(Graphics \* ,CombineMode)**](/previous-versions//ms535823(v=vs.85))                  | El [**método Graphics::SetClip**](/previous-versions//ms535823(v=vs.85)) actualiza la región de recorte de este objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de sí mismo y la región de recorte de otro **objeto Graphics.**<br/>                                                                                                                                                                       |
| [**SetClip(GraphicsPath \* ,CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode))           | El [**método Graphics::SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)) actualiza la región de recorte de este objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de sí mismo y la región especificada por una ruta de acceso gráfica. Si una figura de la ruta de acceso no está cerrada, este método trata la figura no incluida como si se hubiera cerrado mediante una línea recta que conecta los puntos inicial y final de la ilustración.<br/> |



 

 
