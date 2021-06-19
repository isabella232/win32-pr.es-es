---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. Estas funciones de API planas se encapsulan mediante la clase Brush de C++.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funciones brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395090"
---
# <a name="brush-functions-gdi"></a>Funciones brush (GDI+)

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h. Las funciones de la API plana de GDI+ están encapsuladas por una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo llamando a los métodos y funciones proporcionados por los contenedores de C++. Los Servicios de soporte técnico de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos contenedor, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Las siguientes funciones de API planas se encapsulan mediante la [**clase Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) de C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funciones brush y métodos contenedor correspondientes



| Función plana                                                                        | Método contenedor                                          | Descripción                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \* brush, GpBrush \* \* cloneBrush)          | [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | El [**método Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crea un nuevo [**objeto Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basado en este pincel. |
| GpStatus WINGDIPAPI GdipDeleteBrush(Pincel \* GpBrush)                                 | virtual ~Brush()                                        | Limpia los recursos utilizados por un [**objeto Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)                                                                    |
| GpStatus WINGDIPAPI GdipGetBrushType(pincel \* GpBrush, tipo \* GpBrushType)<br/> | [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | El [**método Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) obtiene el tipo de este pincel.                                                      |



 

 

 




