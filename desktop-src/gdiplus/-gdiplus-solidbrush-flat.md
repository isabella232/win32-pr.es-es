---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. Estas funciones de API planas se encapsulan mediante la clase solidBrush de C++.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funciones SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395560"
---
# <a name="solidbrush-functions"></a>Funciones SolidBrush

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h. Las funciones de la API plana de GDI+ se encapsulan mediante una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, se recomienda que lo haga llamando a los métodos y funciones proporcionados por los contenedores de C++. Los Servicios de soporte técnico de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos de contenedor, vea [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Las siguientes funciones de API planas se encapsulan mediante la [**clase solidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) de C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funciones brush y métodos contenedores correspondientes



| Función plana                                                                               | Método de contenedor                                                                                       | Observaciones                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill(color ARGB, pincel GpSolidFill) \* \***<br/>   | [**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Crea un [**objeto SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basado en un color |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor(Pincel GpSolidFill, \* color ARGB)**<br/>   | [**SolidBrush::SetColor(IN const Color& color)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Establece el color de este pincel sólido.                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor(Pincel GpSolidFill, \* \* color ARGB)**<br/> | [**SolidBrush::GetColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Obtiene el color de este pincel sólido.                                                      |



 

 

 
