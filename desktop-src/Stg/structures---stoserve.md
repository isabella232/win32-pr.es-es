---
title: 'Estructuras: StoServe'
description: COPaper empaqueta el color, el ancho y las coordenadas del lápiz en estructuras INKDATA y las almacena en una matriz asignada dinámicamente que administra en memoria.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81b46f2f0a992f27ed405361734fe53db98cf9272697b88866451ef1d7d4b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796895"
---
# <a name="structures---stoserve"></a>Estructuras: StoServe

COPaper empaqueta el color, el ancho y las coordenadas del lápiz en estructuras **INKDATA** y las almacena en una matriz asignada dinámicamente que administra en memoria.

## <a name="inkdata-structure"></a>INKDATA (estructura)

Estas son las declaraciones para la **estructura INKDATA** de PAPER.H.

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

M paInkData, miembro de la clase de implementación  \_ [**IPaper,**](ipaper-methods.md) apunta a la matriz dinámica de estos paquetes INKDATA. La matriz se crea dentro **del método IPaper::InitPaper** con una asignación inicial. Para más información, consulte el **método InitPaper** y el método de utilidad NextSlot privado de la implementación de CImpIPaper en PAPER.H. Los [**métodos InkStart,**](inkstart-method.md) [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) usan NextSlot para obtener ranuras nuevas en la matriz. NextSlot expande dinámicamente la matriz a medida que surge la necesidad.

El cliente llama al [**método IPaper::Erase**](ipaper-methods.md) para borrar el dibujo actual. Este método no reallocate la matriz; simplemente marca todos los datos de entrada de lápiz actuales como INKTYPE NONE y restablece el índice de fin de datos de la matriz \_ a cero.

El cliente llama a los [**métodos IPaper::Lock**](ipaper-methods.md) y **Unlock** para administrar la propiedad de COPaper para dibujar. Estos métodos se proporcionan para organizar el acceso entre varios clientes al dibujo contenido en un COPaper compartido.

## <a name="paper_properties-structure"></a>PAPER \_ PROPERTIES (Estructura)

El cliente llama al [**método IPaper::Resize**](ipaper-methods.md) para decir a COPaper que el usuario ha cambiado el tamaño del rectángulo de papel de dibujo actual. Estos datos de coordenadas se mantienen en una **estructura PAPER \_ PROPERTIES,** que se almacena con los datos de entrada de lápiz cuando todos los datos de papel se almacenan en un archivo compuesto.

A continuación se muestra **la declaración PAPER \_ PROPERTIES** de PAPER.H.

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

La **estructura PAPER \_ PROPERTIES** está diseñada para que se puedan agregar nuevos formatos de datos de entrada de lápiz en cualquier momento a medida que evoluciona el componente DllPaper. La [**interfaz IPaper**](ipaper-methods.md) es lo suficientemente general como para que una versión posterior del componente DllPaper pueda almacenar un formato de datos de entrada de lápiz diferente al implementar la misma **interfaz IPaper.** Dado que los métodos de **IPaper** no dependen de un formato de datos de entrada de lápiz específico, una nueva versión del componente DllPaper que admita un formato de datos de entrada de lápiz diferente puede usar esta misma interfaz.

Las propiedades de papel almacenadas en un archivo compuesto registran el tamaño actual de la matriz de datos de entrada de lápiz. A continuación, se puede asignar el tamaño de matriz adecuado para alojar los datos de entrada de lápiz leídos del archivo.

La **estructura PAPER PROPERTIES \_ también** almacena el tamaño del rectángulo de dibujo de la superficie de papel y el color de la ventana de fondo.

Aunque no se usa en **los ejemplos de StoServe** / **StoClien,** también se pueden almacenar un título de dibujo y un nombre de autor.

La fecha de creación y las fechas de última modificación no se incluyen en estas propiedades de papel, ya que la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) usada para acceder a archivos compuestos administra esta información.

 

 




