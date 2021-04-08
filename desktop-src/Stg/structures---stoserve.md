---
title: 'Estructuras: StoServe'
description: El copaper empaqueta el color, el ancho y las coordenadas del lápiz en estructuras INKDATA y los almacena en una matriz asignada dinámicamente que administra en la memoria.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9868f38d7915185b8d3511bd1bf6faa9c7a1e1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994128"
---
# <a name="structures---stoserve"></a>Estructuras: StoServe

El copaper empaqueta el color, el ancho y las coordenadas del lápiz en estructuras **INKDATA** y los almacena en una matriz asignada dinámicamente que administra en la memoria.

## <a name="inkdata-structure"></a>Estructura INKDATA

A continuación se muestran las declaraciones de la estructura **INKDATA** de Paper. H.

``` syntax
// The types of Ink Data.
#define INKTYPE_NONE  0
#define INKTYPE_START 1
#define INKTYPE_DRAW  2
#define INKTYPE_STOP  3

  // The Ink Data structure.
  typedef struct _INKDATA
  {
    SHORT nType;            // Ink Type.
    SHORT nX;               // X-coordinate of ink point.
    SHORT nY;               // Y-coordinate of ink point.
    SHORT nWidth;           // Ink line width in pixels.
    COLORREF crColor;       // Ink color.
  } INKDATA;
```

La matriz dinámica de estos paquetes **INKDATA** se apunta por m \_ paInkData, un miembro de la clase de implementación [**IPaper**](ipaper-methods.md) . La matriz se crea dentro del método **IPaper:: InitPaper** con una asignación inicial. Para obtener más información, vea el método **InitPaper** y el método Private NextSlot Utility de la implementación de CIMPIPAPER en Paper. H. Los métodos [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) usan NextSlot para obtener nuevas ranuras en la matriz. La matriz se expande dinámicamente mediante NextSlot, según sea necesario.

El cliente llama al método [**IPaper:: Erase**](ipaper-methods.md) para borrar el dibujo actual. Este método no reasigna la matriz; simplemente marca todos los datos de tinta actuales como INKTYPE \_ None y restablece el índice de final de datos de la matriz en cero.

El cliente llama a los métodos [**IPaper:: Lock**](ipaper-methods.md) y **Unlock** para administrar la propiedad de los copapers del dibujo. Estos métodos se proporcionan para organizar el acceso entre varios clientes al dibujo que se mantiene en un copaper compartido.

## <a name="paper_properties-structure"></a>\_Estructura de las propiedades del papel

El cliente llama al método [**IPaper:: Resize**](ipaper-methods.md) para indicar a las copapeles que el usuario ha cambiado el tamaño del rectángulo de papel del dibujo actual. Estos datos de coordenadas se guardan en una estructura de **\_ propiedades de papel** , que se almacena con los datos de tinta cuando todos los datos de papel se almacenan en un archivo compuesto.

La siguiente es la declaración de **\_ las propiedades del papel** de Paper. H.

``` syntax
#define PAPER_TITLE_SIZE 64
  typedef struct _PAPER_PROPERTIES
  {
    LONG lInkDataVersion;
    LONG lInkArraySize;
    COLORREF crWinColor;
    RECT WinRect;
    WCHAR wszTitle[PAPER_TITLE_SIZE];
    WCHAR wszAuthor[PAPER_TITLE_SIZE];
    WCHAR wszReserved1[PAPER_TITLE_SIZE];
    WCHAR wszReserved2[PAPER_TITLE_SIZE];
  } PAPER_PROPERTIES;
```

La estructura de **\_ las propiedades del papel** está diseñada para que se puedan agregar nuevos formatos de datos de entrada de lápiz en cualquier momento a medida que el componente DllPaper evolucione. La interfaz [**IPaper**](ipaper-methods.md) es lo suficientemente general como para que una versión posterior del componente DllPaper pueda almacenar un formato de datos de tinta diferente mientras se implementa la misma interfaz **IPaper** . Dado que los métodos de **IPaper** no dependen de un formato de datos de tinta específico, una nueva versión del componente DllPaper que admite un formato de datos de tinta diferente puede usar esta misma interfaz.

Las propiedades de papel almacenadas en un archivo compuesto registran el tamaño actual de la matriz de datos de tinta. A continuación, se puede asignar el tamaño de matriz adecuado para dar cabida a los datos de tinta leídos del archivo.

La estructura de **\_ propiedades del papel** también almacena el tamaño del rectángulo de dibujo y el color de la ventana del fondo.

Aunque no se usa en los ejemplos de **StoServe** / **StoClien** , también se pueden almacenar un título de dibujo y un nombre de autor.

La fecha de creación y las fechas de última modificación no se incluyen en estas propiedades de papel, porque la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) utilizada para tener acceso a los archivos compuestos administra esta información.

 

 




