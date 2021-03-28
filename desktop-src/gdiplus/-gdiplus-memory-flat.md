---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funciones de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e748f8a68cc6f04deba3c9676638ee48ee2e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985154"
---
# <a name="memory-functions"></a>Funciones de memoria

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h. Las funciones de la API plana GDI+ se incluyen en una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo mediante una llamada a los métodos y las funciones proporcionados por los contenedores de C++. Los servicios de soporte técnico de Microsoft no proporcionarán soporte técnico para el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos de contenedor, consulte la [API plana de GDI+](-gdiplus-flatapi-flat.md).

Las siguientes funciones de la API plana están incluidas en la clase [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) de C++.

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>Funciones de memoria y métodos contenedores correspondientes



| Función plana                                          | Wrapper (método)                                                                                                                                      | Observaciones                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipAlloc (tamaño \_ t tamaño)<br/> | [**GpStatus WINGDIPAPI GdiplusBase void \* (operador New) (tamaño \_ t de \_ tamaño)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | Asigna memoria para un objeto GDI+ de Windows. <br/> GdipAlloc se declara en GdiplusMem. h.<br/>  |
| GpStatus WINGDIPAPI GdipFree (void \* ptr);<br/>   | [**GpStatus WINGDIPAPI GdiplusBase void (operador Delete) (void \* en \_ pVoid)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | Desasigna memoria para un objeto GDI+ de Windows. <br/> GdipFree se declara en GdiplusMem. h.<br/> |



 

 

 
