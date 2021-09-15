---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. Estas funciones de API planas se encapsulan mediante la clase C++ HatchBrush.
ms.assetid: c7d9e633-8c3d-4e77-811d-306cd785a7ad
title: Funciones de HatchBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa455c1194ca4f3397673d1a4412dc9ed7e3473
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566381"
---
# <a name="hatchbrush-functions"></a>Funciones de HatchBrush

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h. Las funciones de GDI+ API plana se encapsulan mediante una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo llamando a los métodos y funciones proporcionados por los contenedores de C++. Los Servicios de soporte técnico del producto de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos de contenedor, [consulte GDI+ Flat API](-gdiplus-flatapi-flat.md).

Las siguientes funciones de API planas se encapsulan mediante [**la clase C++ HatchBrush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush)

## <a name="hatchbrush-functions-and-corresponding-wrapper-methods"></a>Funciones HatchBrush y métodos de contenedor correspondientes



| Función plana                                                                                                               | Método de contenedor                                                                                                                                                                                   | Observaciones                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateHatchBrush(GpHatchStyle hatchstyle, ARGB forecol, ARGB backcol, GpHatch \* \* brush)<br/> | [**HatchBrush::HatchBrush(IN HatchStyle hatchStyle, IN const Color& foreColor, IN const Color& backColor = Color())**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)) | Crea un [**objeto HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) basado en un estilo de sombreado, un color de primer plano y un color de fondo. |
| GpStatus WINGDIPAPI GdipGetHatchStyle(GpHatch \* brush, GpHatchStyle \* hatchstyle)<br/>                                | [**HatchStyle HatchBrush::GetHatchStyle() const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-gethatchstyle)                                                                                                 | Obtiene el estilo de sombreado de este pincel de sombreado.                                                                                                  |
| GpStatus WINGDIPAPI GdipGetHatchForegroundColor(GpHatch \* brush, ARGB \* forecol)<br/>                                 | [**Status HatchBrush::GetForegroundColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor)                                                                    | Obtiene el color de primer plano de este pincel de sombreado.                                                                                             |
| GpStatus WINGDIPAPI GdipGetHatchBackgroundColor(GpHatch \* brush, ARGB \* backcol)<br/>                                 | [**Status HatchBrush::GetBackgroundColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getbackgroundcolor)                                                                    | Obtiene el color de fondo de este pincel de sombreado.                                                                                             |



 

 

 
