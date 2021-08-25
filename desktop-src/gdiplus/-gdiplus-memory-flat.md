---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. La clase GdiplusBase de C++ encapsula estas funciones de API planas.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funciones de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce4e75de3cf5c7ff96a794416b75a9bacadda5a0aade2f5a61e2607e620e3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943815"
---
# <a name="memory-functions"></a>Funciones de memoria

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h. Las funciones del GDI+ API plana se encapsulan mediante una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo llamando a los métodos y funciones proporcionados por los contenedores de C++. Los Servicios de soporte técnico de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos contenedor, [consulte GDI+ Flat API](-gdiplus-flatapi-flat.md).

La clase [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) de C++ encapsula las siguientes funciones de API planas.

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>Funciones de memoria y métodos contenedor correspondientes



| Función plana                                          | Método contenedor                                                                                                                                      | Comentarios                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipAlloc(tamaño \_ t)<br/> | [**GpStatus WINGDIPAPI GdiplusBase void \* (operator new)(size \_ t in \_ size)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | Asigna memoria para un Windows GDI+ objeto . <br/> GdipAlloc se declara en GdiplusMem.h.<br/>  |
| GpStatus WINGDIPAPI GdipFree(void \* ptr);<br/>   | [**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void \* in \_ pVoid)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | Desasigna la memoria de Windows GDI+ objeto. <br/> GdipFree se declara en GdiplusMem.h.<br/> |



 

 

 
