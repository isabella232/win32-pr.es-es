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
# <a name="structures---stoserve"></a><span data-ttu-id="0d071-103">Estructuras: StoServe</span><span class="sxs-lookup"><span data-stu-id="0d071-103">Structures - StoServe</span></span>

<span data-ttu-id="0d071-104">El copaper empaqueta el color, el ancho y las coordenadas del lápiz en estructuras **INKDATA** y los almacena en una matriz asignada dinámicamente que administra en la memoria.</span><span class="sxs-lookup"><span data-stu-id="0d071-104">COPaper packages the pen color, width, and coordinates into **INKDATA** structures and stores them in a dynamically allocated array that it manages in memory.</span></span>

## <a name="inkdata-structure"></a><span data-ttu-id="0d071-105">Estructura INKDATA</span><span class="sxs-lookup"><span data-stu-id="0d071-105">INKDATA Structure</span></span>

<span data-ttu-id="0d071-106">A continuación se muestran las declaraciones de la estructura **INKDATA** de Paper. H.</span><span class="sxs-lookup"><span data-stu-id="0d071-106">The following are the declarations for the **INKDATA** structure from PAPER.H.</span></span>

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

<span data-ttu-id="0d071-107">La matriz dinámica de estos paquetes **INKDATA** se apunta por m \_ paInkData, un miembro de la clase de implementación [**IPaper**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="0d071-107">The dynamic array of these **INKDATA** packets is pointed to by m\_paInkData, a member of the [**IPaper**](ipaper-methods.md) implementation class.</span></span> <span data-ttu-id="0d071-108">La matriz se crea dentro del método **IPaper:: InitPaper** con una asignación inicial.</span><span class="sxs-lookup"><span data-stu-id="0d071-108">The array is created within the **IPaper::InitPaper** method with an initial allocation.</span></span> <span data-ttu-id="0d071-109">Para obtener más información, vea el método **InitPaper** y el método Private NextSlot Utility de la implementación de CIMPIPAPER en Paper. H.</span><span class="sxs-lookup"><span data-stu-id="0d071-109">For details, see the **InitPaper** method and the private NextSlot utility method of the CImpIPaper implementation in PAPER.H.</span></span> <span data-ttu-id="0d071-110">Los métodos [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) usan NextSlot para obtener nuevas ranuras en la matriz.</span><span class="sxs-lookup"><span data-stu-id="0d071-110">The [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods use NextSlot to obtain new slots in the array.</span></span> <span data-ttu-id="0d071-111">La matriz se expande dinámicamente mediante NextSlot, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="0d071-111">The array is expanded dynamically by NextSlot as the need arises.</span></span>

<span data-ttu-id="0d071-112">El cliente llama al método [**IPaper:: Erase**](ipaper-methods.md) para borrar el dibujo actual.</span><span class="sxs-lookup"><span data-stu-id="0d071-112">The client calls the [**IPaper::Erase**](ipaper-methods.md) method to erase the current drawing.</span></span> <span data-ttu-id="0d071-113">Este método no reasigna la matriz; simplemente marca todos los datos de tinta actuales como INKTYPE \_ None y restablece el índice de final de datos de la matriz en cero.</span><span class="sxs-lookup"><span data-stu-id="0d071-113">This method does not reallocate the array; it simply marks all current ink data as INKTYPE\_NONE and resets the array's end-of-data index to zero.</span></span>

<span data-ttu-id="0d071-114">El cliente llama a los métodos [**IPaper:: Lock**](ipaper-methods.md) y **Unlock** para administrar la propiedad de los copapers del dibujo.</span><span class="sxs-lookup"><span data-stu-id="0d071-114">The client calls the [**IPaper::Lock**](ipaper-methods.md) and **Unlock** methods to manage ownership of COPaper for drawing.</span></span> <span data-ttu-id="0d071-115">Estos métodos se proporcionan para organizar el acceso entre varios clientes al dibujo que se mantiene en un copaper compartido.</span><span class="sxs-lookup"><span data-stu-id="0d071-115">These methods are provided to organize access among multiple clients to the drawing held in a shared COPaper.</span></span>

## <a name="paper_properties-structure"></a><span data-ttu-id="0d071-116">\_Estructura de las propiedades del papel</span><span class="sxs-lookup"><span data-stu-id="0d071-116">PAPER\_PROPERTIES Structure</span></span>

<span data-ttu-id="0d071-117">El cliente llama al método [**IPaper:: Resize**](ipaper-methods.md) para indicar a las copapeles que el usuario ha cambiado el tamaño del rectángulo de papel del dibujo actual.</span><span class="sxs-lookup"><span data-stu-id="0d071-117">The client calls the [**IPaper::Resize**](ipaper-methods.md) method to tell COPaper that the user resized the current drawing paper rectangle.</span></span> <span data-ttu-id="0d071-118">Estos datos de coordenadas se guardan en una estructura de **\_ propiedades de papel** , que se almacena con los datos de tinta cuando todos los datos de papel se almacenan en un archivo compuesto.</span><span class="sxs-lookup"><span data-stu-id="0d071-118">This coordinate data is kept in a **PAPER\_PROPERTIES** structure, which is stored with the ink data when all the paper data is stored in a compound file.</span></span>

<span data-ttu-id="0d071-119">La siguiente es la declaración de **\_ las propiedades del papel** de Paper. H.</span><span class="sxs-lookup"><span data-stu-id="0d071-119">The following is the **PAPER\_PROPERTIES** declaration from PAPER.H.</span></span>

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

<span data-ttu-id="0d071-120">La estructura de **\_ las propiedades del papel** está diseñada para que se puedan agregar nuevos formatos de datos de entrada de lápiz en cualquier momento a medida que el componente DllPaper evolucione.</span><span class="sxs-lookup"><span data-stu-id="0d071-120">The **PAPER\_PROPERTIES** structure is designed so that new ink data formats can be added at any time as the DllPaper component evolves.</span></span> <span data-ttu-id="0d071-121">La interfaz [**IPaper**](ipaper-methods.md) es lo suficientemente general como para que una versión posterior del componente DllPaper pueda almacenar un formato de datos de tinta diferente mientras se implementa la misma interfaz **IPaper** .</span><span class="sxs-lookup"><span data-stu-id="0d071-121">The [**IPaper**](ipaper-methods.md) interface is general enough that a subsequent version of the DllPaper component may store a different ink data format while implementing the same **IPaper** interface.</span></span> <span data-ttu-id="0d071-122">Dado que los métodos de **IPaper** no dependen de un formato de datos de tinta específico, una nueva versión del componente DllPaper que admite un formato de datos de tinta diferente puede usar esta misma interfaz.</span><span class="sxs-lookup"><span data-stu-id="0d071-122">Because the methods of **IPaper** do not depend on a specific ink data format, a new version of the DllPaper component that does support a different ink data format can use this same interface.</span></span>

<span data-ttu-id="0d071-123">Las propiedades de papel almacenadas en un archivo compuesto registran el tamaño actual de la matriz de datos de tinta.</span><span class="sxs-lookup"><span data-stu-id="0d071-123">The paper properties stored in a compound file record the current size of the ink data array.</span></span> <span data-ttu-id="0d071-124">A continuación, se puede asignar el tamaño de matriz adecuado para dar cabida a los datos de tinta leídos del archivo.</span><span class="sxs-lookup"><span data-stu-id="0d071-124">The proper array size can then be allocated to accommodate the ink data read from the file.</span></span>

<span data-ttu-id="0d071-125">La estructura de **\_ propiedades del papel** también almacena el tamaño del rectángulo de dibujo y el color de la ventana del fondo.</span><span class="sxs-lookup"><span data-stu-id="0d071-125">The **PAPER\_PROPERTIES** structure also stores the paper surface's drawing rectangle size and background window color.</span></span>

<span data-ttu-id="0d071-126">Aunque no se usa en los ejemplos de **StoServe** / **StoClien** , también se pueden almacenar un título de dibujo y un nombre de autor.</span><span class="sxs-lookup"><span data-stu-id="0d071-126">Though not used in the **StoServe**/**StoClien** samples, a drawing title and an author name can also be stored.</span></span>

<span data-ttu-id="0d071-127">La fecha de creación y las fechas de última modificación no se incluyen en estas propiedades de papel, porque la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) utilizada para tener acceso a los archivos compuestos administra esta información.</span><span class="sxs-lookup"><span data-stu-id="0d071-127">Creation date and last modified dates are not included in these paper properties, because the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface used to access compound files manages this information.</span></span>

 

 




