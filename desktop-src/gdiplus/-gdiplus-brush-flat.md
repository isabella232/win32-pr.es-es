---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funciones de pincel (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490cc641312014987b2fb847979de640c28c47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360620"
---
# <a name="brush-functions-gdi"></a>Funciones de pincel (GDI+)

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h. Las funciones de la API plana GDI+ se incluyen en una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo mediante una llamada a los métodos y las funciones proporcionados por los contenedores de C++. Los servicios de soporte técnico de Microsoft no proporcionarán soporte técnico para el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos de contenedor, consulte la [API plana de GDI+](-gdiplus-flatapi-flat.md).

Las siguientes funciones de la API sin formato se ajustan mediante la clase de C++ [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funciones de pincel y métodos contenedores correspondientes



| Función plana                                                                        | Wrapper (método)                                          | Descripción                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* Brush, GpBrush \* \* cloneBrush)          | [**Brush:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | El método [**Brush:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crea un nuevo objeto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basado en este pincel. |
| GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* Brush)                                 | Pincel ~ de virtual ()                                        | Limpia los recursos usados por un objeto [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .                                                                    |
| GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* Brush, GpBrushType \* Type)<br/> | [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | El método [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) obtiene el tipo de este pincel.                                                      |



 

 

 




