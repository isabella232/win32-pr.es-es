---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.
ms.assetid: c7d9e633-8c3d-4e77-811d-306cd785a7ad
title: Funciones HatchBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d444fea500ce1e56e4c59420b913d5ff6cee965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997477"
---
# <a name="hatchbrush-functions"></a>Funciones HatchBrush

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h. Las funciones de la API plana GDI+ se incluyen en una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo mediante una llamada a los métodos y las funciones proporcionados por los contenedores de C++. Los servicios de soporte técnico de Microsoft no proporcionarán soporte técnico para el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos de contenedor, consulte la [API plana de GDI+](-gdiplus-flatapi-flat.md).

Las siguientes funciones de la API plana se incluyen en la clase [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) C++.

## <a name="hatchbrush-functions-and-corresponding-wrapper-methods"></a>Funciones HatchBrush y métodos contenedores correspondientes



| Función plana                                                                                                               | Wrapper (método)                                                                                                                                                                                   | Observaciones                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateHatchBrush (GpHatchStyle HatchStyle, ARGB forecol, ARGB backcol, GpHatch \* \* Brush)<br/> | [**HatchBrush:: HatchBrush (en HatchStyle hatchStyle, en const color& foreColor, en const color& BackColor = color ())**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)) | Crea un objeto [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) basado en un estilo de trama, un color de primer plano y un color de fondo. |
| GpStatus WINGDIPAPI GdipGetHatchStyle (GpHatch \* Brush, GpHatchStyle \* HatchStyle)<br/>                                | [**HatchStyle HatchBrush:: GetHatchStyle () Const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-gethatchstyle)                                                                                                 | Obtiene el estilo de sombreado de este pincel de sombreado.                                                                                                  |
| GpStatus WINGDIPAPI GdipGetHatchForegroundColor (GpHatch \* Brush, ARGB \* forecol)<br/>                                 | [**Status HatchBrush:: GetForegroundColor (OUT color \* color) Const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor)                                                                    | Obtiene el color de primer plano de este pincel de sombreado.                                                                                             |
| GpStatus WINGDIPAPI GdipGetHatchBackgroundColor (GpHatch \* Brush, ARGB \* backcol)<br/>                                 | [**Status HatchBrush:: GetBackgroundColor (OUT color \* color) Const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getbackgroundcolor)                                                                    | Obtiene el color de fondo de este pincel de sombreado.                                                                                             |



 

 

 
