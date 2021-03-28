---
description: En este tema se enumeran los constructores de la clase Font. Para obtener una lista completa de clases, vea Font (clase).
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: Fonts. Font (constructores)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: bdf533e292734956c02d3f8a424ca619cb722c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279051"
---
# <a name="fontfont-constructors"></a>Fonts. Font (constructores)

En este tema se enumeran los constructores de la clase [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . Para obtener una lista completa de clases, vea **Font (clase**).

### <a name="overload-list"></a>Lista de sobrecarga



| Constructor                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fuente (HDC, HFONT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | Crea indirectamente un objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)) a partir de una fuente lógica de GDI mediante un identificador a una estructura de **LOGFONT** de GDI.<br/>                                                                                                                                   |
| [**Fuente (HDC, LOGFONTA \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | Crea un objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) directamente a partir de una fuente lógica de GDI. La fuente lógica de GDI es una estructura **LOGFONTA** , que es la versión de caracteres de un byte de una fuente lógica. Este constructor se proporciona por compatibilidad con GDI.<br/> |
| [**Fuente (HDC, LOGFONTW \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | Crea un objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) directamente a partir de una fuente lógica de GDI. La fuente lógica de GDI es una estructura **LOGFONTW** , que es la versión de caracteres anchos de una fuente lógica. Este constructor se proporciona por compatibilidad con GDI.<br/>     |
| [**Fuente (FontFamily \* , real, int, Unit)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | Crea un objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit)) basado en un objeto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) , un tamaño, un estilo de fuente y una unidad de medida.<br/>                                                                               |
| [**Fuente (WCHAR \* , real, int, Unit, FontCollection \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | Crea un objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) basado en una familia de fuentes, un tamaño, un estilo de fuente, una unidad de medida y un objeto [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .<br/>                                     |
| [**Fuente (HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | Crea un objeto [**Font:: Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) basado en el objeto de fuente GDI que está seleccionado actualmente en un contexto de dispositivo especificado. Este constructor se proporciona por compatibilidad con GDI. <br/>                                                                           |



 

 
