---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: SolidBrush (funciones)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984434"
---
# <a name="solidbrush-functions"></a>SolidBrush (funciones)

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h. Las funciones de la API plana GDI+ se incluyen en una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, recomendamos que lo haga llamando a los métodos y las funciones proporcionados por los contenedores de C++. Los servicios de soporte técnico de Microsoft no proporcionarán soporte técnico para el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos de contenedor, consulte la [API plana de GDI+](-gdiplus-flatapi-flat.md).

Las siguientes funciones de la API plana están incluidas en la clase de C++ [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) .

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funciones de pincel y métodos contenedores correspondientes



| Función plana                                                                               | Wrapper (método)                                                                                       | Observaciones                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill (color ARGB, GpSolidFill \* \* Brush)**<br/>   | [**SolidBrush:: SolidBrush (en el color const& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Crea un objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basado en un color. |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* Brush, color ARGB)**<br/>   | [**SolidBrush:: SetColor (en el color const& color)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Establece el color de este pincel sólido                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* Brush, \* color ARGB)**<br/> | [**SolidBrush:: GetColor (color de salida \* del color) Const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Obtiene el color de este pincel sólido                                                      |



 

 

 
