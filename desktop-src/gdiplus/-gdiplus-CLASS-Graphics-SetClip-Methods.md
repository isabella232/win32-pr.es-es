---
description: En este tema se enumeran los métodos SetClip de la clase Graphics. Para obtener una lista completa de los métodos de la clase Graphics, vea Graphics.
ms.assetid: e8348373-da79-4d33-8bea-d594985493d4
title: Graphics. SetClip (métodos)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 488d617dfb53343fc728fff722c0c0bc1db57335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276431"
---
# <a name="graphicssetclip-methods"></a>Graphics. SetClip (métodos)

En este tema se enumeran los métodos SetClip de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Para obtener una lista completa de los métodos de la clase **Graphics** , vea [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetClip (HRGN, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode))                     | El método [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode)) actualiza la región de recorte de este objeto de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de ella misma y una región de GDI.<br/>                                                                                                                                                                                                          |
| [**SetClip (Rect&, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode))   | El método [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode)) actualiza la región de recorte de este objeto de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de sí mismo y de un rectángulo.<br/>                                                                                                                                                                                          |
| [**SetClip (RectF&, CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) | El método [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) actualiza la región de recorte de este objeto de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de sí mismo y de un rectángulo.<br/>                                                                                                                                                                                         |
| [**SetClip (region \* , CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))               | El método [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) actualiza la región de recorte de este objeto de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de ella misma y la región especificada por un objeto [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) .<br/>                                                                                                                                      |
| [**SetClip (Graphics \* , CombineMode)**](/previous-versions//ms535823(v=vs.85))                  | El método [**Graphics:: SetClip**](/previous-versions//ms535823(v=vs.85)) actualiza la región de recorte de este objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) en una región que es la combinación de ella misma y la región de recorte de otro objeto **Graphics** .<br/>                                                                                                                                                                       |
| [**SetClip (GraphicsPath \* , CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode))           | El método [**Graphics:: SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode)) actualiza la región de recorte de este objeto de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) a una región que es la combinación de ella misma y la región especificada por una ruta de acceso de gráficos. Si una figura de la ruta de acceso no está cerrada, este método trata la figura sin cerrar como si se hubiera cerrado con una línea recta que conecta los puntos inicial y final de la figura.<br/> |



 

 
