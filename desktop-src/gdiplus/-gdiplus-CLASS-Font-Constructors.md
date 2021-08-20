---
description: En este tema se enumeran los constructores de la clase Font. Para obtener una lista de clases completa, vea Clase de fuente.
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: Constructores Font.Font
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ff876120655adcf58318a471ed66ddfa4502d625305d9fda37f01c966e19e0cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977905"
---
# <a name="fontfont-constructors"></a>Constructores Font.Font

En este tema se enumeran los constructores de la [**clase Font.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) Para obtener una lista de clases completa, vea **Font Class**.

### <a name="overload-list"></a>Lista de sobrecarga



| Constructor                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Font(HDC,HFONT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | Crea [**indirectamente un objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)) a partir de una fuente lógica GDI mediante un identificador para una **estructura LOGFONT de** GDI.<br/>                                                                                                                                   |
| [**Font(HDC,LOGFONTA \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | Crea un [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) directamente a partir de una fuente lógica GDI. La fuente lógica GDI es una **estructura LOGFONTA,** que es la versión de caracteres de un byte de una fuente lógica. Este constructor se proporciona para la compatibilidad con GDI.<br/> |
| [**Font(HDC,LOGFONTW \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | Crea un [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) directamente a partir de una fuente lógica GDI. La fuente lógica GDI es una **estructura LOGFONTW,** que es la versión de caracteres anchos de una fuente lógica. Este constructor se proporciona para la compatibilidad con GDI.<br/>     |
| [**Font(FontFamily \* ,REAL,INT,Unit)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | Crea un [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit)) basado en un objeto [**FontFamily,**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) un tamaño, un estilo de fuente y una unidad de medida.<br/>                                                                               |
| [**Font(WCHAR \* ,REAL,INT,Unit,FontCollection \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | Crea un [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) basado en una familia de fuentes, un tamaño, un estilo de fuente, una unidad de medida y un [**objeto FontCollection.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection)<br/>                                     |
| [**Fuente (HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | Crea un [**objeto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) basado en el objeto de fuente GDI que está seleccionado actualmente en un contexto de dispositivo especificado. Este constructor se proporciona para la compatibilidad con GDI. <br/>                                                                           |



 

 
