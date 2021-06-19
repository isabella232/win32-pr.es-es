---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. La clase GdiplusBase de C++ encapsula estas funciones de API planas.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funciones de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395830"
---
# <a name="memory-functions"></a>Funciones de memoria

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h. Las funciones de la API plana de GDI+ están encapsuladas por una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo llamando a los métodos y funciones proporcionados por los contenedores de C++. Los Servicios de soporte técnico de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos contenedor, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).

La clase [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) de C++ encapsula las siguientes funciones de API planas.

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>Funciones de memoria y métodos contenedor correspondientes



| Función plana                                          | Método contenedor                                                                                                                                      | Observaciones                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipAlloc(tamaño \_ t)<br/> | [**GpStatus WINGDIPAPI GdiplusBase void \* (operator new)(size \_ t in \_ size)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | Asigna memoria para un objeto GDI+ de Windows. <br/> GdipAlloc se declara en GdiplusMem.h.<br/>  |
| GpStatus WINGDIPAPI GdipFree(void \* ptr);<br/>   | [**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void \* in \_ pVoid)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | Desasigna la memoria de un objeto GDI+ de Windows. <br/> GdipFree se declara en GdiplusMem.h.<br/> |



 

 

 
