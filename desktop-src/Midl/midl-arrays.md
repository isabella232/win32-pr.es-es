---
title: Matrices de MIDL
description: Matrices de MIDL.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- tipos de datos MIDL, matrices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077697"
---
# <a name="midl-arrays"></a><span data-ttu-id="2ccb6-104">Matrices de MIDL</span><span class="sxs-lookup"><span data-stu-id="2ccb6-104">MIDL Arrays</span></span>

<span data-ttu-id="2ccb6-105">Los declaradores de matriz aparecen en el cuerpo de la interfaz del archivo IDL como uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2ccb6-105">Array declarators appear in the interface body of the IDL file as one of the following:</span></span>

-   <span data-ttu-id="2ccb6-106">Parte de una declaración general</span><span class="sxs-lookup"><span data-stu-id="2ccb6-106">Part of a general declaration</span></span>
-   <span data-ttu-id="2ccb6-107">Miembro de un declarador de estructura o Unión</span><span class="sxs-lookup"><span data-stu-id="2ccb6-107">A member of a structure or union declarator</span></span>
-   <span data-ttu-id="2ccb6-108">Un parámetro para una llamada a procedimiento remoto</span><span class="sxs-lookup"><span data-stu-id="2ccb6-108">A parameter to a remote procedure call</span></span>

<span data-ttu-id="2ccb6-109">Los límites de cada dimensión de la matriz se expresan dentro de un par independiente de corchetes.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-109">The bounds of each dimension of the array are expressed inside a separate pair of square brackets.</span></span> <span data-ttu-id="2ccb6-110">Una expresión que se evalúa como *n* significa un límite inferior de cero y un límite superior de *n-1*.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-110">An expression that evaluates to *n* signifies a lower bound of zero and an upper bound of *n - 1*.</span></span> <span data-ttu-id="2ccb6-111">Si los corchetes están vacíos o contienen un solo asterisco ( \* ), el límite inferior es cero y el límite superior se determina en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-111">If the square brackets are empty or contain a single asterisk (\*), the lower bound is zero and the upper bound is determined at runtime.</span></span>

<span data-ttu-id="2ccb6-112">La matriz también puede contener dos valores separados por puntos suspensivos que representan los límites inferior y superior de la matriz, como en la \[ *parte inferior*... *Upper* \] .</span><span class="sxs-lookup"><span data-stu-id="2ccb6-112">The array can also contain two values separated by an ellipsis that represent the lower and upper bounds of the array, as in \[*lower*...*upper*\].</span></span> <span data-ttu-id="2ccb6-113">Microsoft RPC requiere un límite inferior de cero.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-113">Microsoft RPC requires a lower bound of zero.</span></span> <span data-ttu-id="2ccb6-114">El compilador MIDL no reconoce las construcciones que especifican límites inferiores distintos de cero.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-114">The MIDL compiler does not recognize constructs that specify nonzero lower bounds.</span></span>

<span data-ttu-id="2ccb6-115">Las matrices se pueden asociar con el tamaño de los atributos de campo [**\_ es**](size-is.md), [**Max \_ es**](max-is.md), [**length \_**](length-is.md)es, [**First \_ is**](first-is.md)y [**Last \_ es**](last-is.md) para especificar el tamaño de la matriz o la parte de la matriz que contiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-115">Arrays can be associated with the field attributes [**size\_is**](size-is.md), [**max\_is**](max-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), and [**last\_is**](last-is.md) to specify the size of the array or the part of the array that contains valid data.</span></span> <span data-ttu-id="2ccb6-116">Estos atributos de campo identifican el parámetro, el campo de estructura o la constante que especifica la dimensión o el índice de la matriz.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-116">These field attributes identify the parameter, structure field, or constant that specifies the array dimension or index.</span></span>

<span data-ttu-id="2ccb6-117">La matriz debe estar asociada con el identificador especificado por el atributo de campo de la siguiente manera: cuando la matriz es un parámetro, el identificador también debe ser un parámetro de la misma función. Cuando la matriz es un campo de estructura, el identificador debe ser otro campo de estructura de la misma estructura.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-117">The array must be associated with the identifier specified by the field attribute in the following way: When the array is a parameter, the identifier must also be a parameter to the same function; when the array is a structure field, the identifier must be another structure field of that same structure.</span></span>

<span data-ttu-id="2ccb6-118">Una matriz se denomina "compatible" si el límite superior de cualquier dimensión se determina en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-118">An array is called "conformant" if the upper bound of any dimension is determined at runtime.</span></span> <span data-ttu-id="2ccb6-119">(Solo se pueden determinar en tiempo de ejecución los límites superiores). Para determinar el límite superior, la declaración de la matriz debe [**incluir \_ el atributo size**](size-is.md) o [**Max \_ is**](max-is.md) .</span><span class="sxs-lookup"><span data-stu-id="2ccb6-119">(Only upper bounds can be determined at runtime.) To determine the upper bound, the array declaration must include a [**size\_is**](size-is.md) or [**max\_is**](max-is.md) attribute.</span></span>

<span data-ttu-id="2ccb6-120">Una matriz se denomina "varying" cuando sus límites se determinan en tiempo de compilación, pero el intervalo de elementos transmitidos se determina en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-120">An array is called "varying" when its bounds are determined at compile time, but the range of transmitted elements is determined at runtime.</span></span> <span data-ttu-id="2ccb6-121">Para determinar el intervalo de elementos transmitidos, la declaración de la matriz debe incluir una [**longitud \_**](length-is.md), el [**primero \_ es**](first-is.md)o el atributo [**Last \_**](last-is.md) .</span><span class="sxs-lookup"><span data-stu-id="2ccb6-121">To determine the range of transmitted elements, the array declaration must include a [**length\_is**](length-is.md), [**first\_is**](first-is.md), or [**last\_is**](last-is.md) attribute.</span></span>

<span data-ttu-id="2ccb6-122">Una matriz variable compatible (también denominada "abrir") es una matriz cuyo límite superior y el intervalo de elementos transmitidos se determinan en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-122">A conformant varying array (also called "open") is an array whose upper bound and range of transmitted elements are determined at runtime.</span></span> <span data-ttu-id="2ccb6-123">Como máximo, se puede anidar una matriz variable compatible o compatible en una estructura de C y debe ser el último elemento de la estructura.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-123">At most, one conformant or conformant varying array can be nested in a C structure and must be the last element of the structure.</span></span> <span data-ttu-id="2ccb6-124">En cambio, las matrices variables no conformes pueden aparecer en cualquier parte de una estructura.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-124">In contrast, nonconformant varying arrays can occur anywhere in a structure.</span></span>

## <a name="examples"></a><span data-ttu-id="2ccb6-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2ccb6-125">Examples</span></span>

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

<span data-ttu-id="2ccb6-126">Para obtener más información, vea [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="2ccb6-126">For more information, see [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

## <a name="multidimensional-arrays"></a><span data-ttu-id="2ccb6-127">Matrices multidimensionales</span><span class="sxs-lookup"><span data-stu-id="2ccb6-127">Multidimensional Arrays</span></span>

<span data-ttu-id="2ccb6-128">El usuario puede declarar tipos que son matrices y, a continuación, declarar matrices de objetos de estos tipos.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-128">The user can declare types that are arrays and then declare arrays of objects of such types.</span></span> <span data-ttu-id="2ccb6-129">La *semántica de las* Matrices unidimensionales de tipos de matriz de *n* dimensiones es la misma que la semántica de las  + matrices de *n* dimensiones de m.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-129">The semantics of *m*-dimensional arrays of *n*-dimensional array types are the same as the semantics of *m*+*n*-dimensional arrays.</span></span>

<span data-ttu-id="2ccb6-130">Por ejemplo, el tipo RECT Type \_ se puede definir como una matriz bidimensional y la variable *Rect* se puede definir como una matriz de tipo Rect \_ .</span><span class="sxs-lookup"><span data-stu-id="2ccb6-130">For example, the type RECT\_TYPE can be defined as a two-dimensional array and the variable *rect* can be defined as an array of RECT\_TYPE.</span></span> <span data-ttu-id="2ccb6-131">Esto es equivalente a la matriz tridimensional *equivalente \_ Rect*:</span><span class="sxs-lookup"><span data-stu-id="2ccb6-131">This is equivalent to the three-dimensional array *equivalent\_rect*:</span></span>

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

<span data-ttu-id="2ccb6-132">Microsoft RPC está orientado a C.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-132">Microsoft RPC is C oriented.</span></span> <span data-ttu-id="2ccb6-133">Según las convenciones del lenguaje C, solo la primera dimensión de una matriz multidimensional se puede determinar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-133">Following C-language conventions, only the first dimension of a multidimensional array can be determined at runtime.</span></span> <span data-ttu-id="2ccb6-134">La interoperación con matrices de DCE IDL que admiten otros idiomas se limita a:</span><span class="sxs-lookup"><span data-stu-id="2ccb6-134">Interoperation with DCE IDL arrays that support other languages is limited to:</span></span>

-   <span data-ttu-id="2ccb6-135">Matrices multidimensionales con límites constantes (determinadas en tiempo de compilación).</span><span class="sxs-lookup"><span data-stu-id="2ccb6-135">Multidimensional arrays with constant (compile-time-determined) bounds.</span></span>
-   <span data-ttu-id="2ccb6-136">Matrices multidimensionales con todos los límites constantes excepto la primera dimensión.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-136">Multidimensional arrays with all constant bounds except the first dimension.</span></span> <span data-ttu-id="2ccb6-137">El límite superior y el intervalo de elementos transmitidos de la primera dimensión dependen del tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-137">The upper bound and range of transmitted elements of the first dimension are dependent on runtime.</span></span>
-   <span data-ttu-id="2ccb6-138">Cualquier matriz unidimensional con un límite inferior de cero.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-138">Any one-dimensional arrays with a lower bound of zero.</span></span>

<span data-ttu-id="2ccb6-139">Cuando el **\[** [](string.md) **\]** atributo de cadena se usa en matrices multidimensionales, el atributo se aplica a la matriz situada más a la derecha.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-139">When the **\[**[**string**](string.md)**\]** attribute is used on multidimensional arrays, the attribute applies to the rightmost array.</span></span>

## <a name="arrays-of-pointers"></a><span data-ttu-id="2ccb6-140">Matrices de punteros</span><span class="sxs-lookup"><span data-stu-id="2ccb6-140">Arrays of Pointers</span></span>

<span data-ttu-id="2ccb6-141">Los punteros de referencia deben apuntar a datos válidos.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-141">Reference pointers must point to valid data.</span></span> <span data-ttu-id="2ccb6-142">La aplicación cliente debe asignar toda la memoria para una **\[** [](in.md) **\]** matriz de punteros de referencia en, o **\[** **en,**[**fuera**](out-idl.md) **\]** de, en especial cuando la matriz está asociada a los valores **\[ en \]**, o **\[** **en, fuera \]** de la **\[** [**longitud \_**](length-is.md)o en el **\]** **\[** [**último \_**](last-is.md) **\]** valor.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-142">The client application must allocate all memory for an **\[**[**in**](in.md)**\]** or **\[** **in,**[**out**](out-idl.md)**\]** array of reference pointers, especially when the array is associated with **\[in\]**, or **\[** **in,out\]**, **\[**[**length\_is**](length-is.md)**\]**, or **\[**[**last\_is**](last-is.md)**\]** values.</span></span> <span data-ttu-id="2ccb6-143">La aplicación cliente también debe inicializar todos los elementos de la matriz antes de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-143">The client application must also initialize all array elements before the call.</span></span> <span data-ttu-id="2ccb6-144">Antes de volver al cliente, la aplicación de servidor debe comprobar que todos los elementos de matriz del punto de intervalo transmitido sean de almacenamiento válido.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-144">Before returning to the client, the server application must verify that all array elements in the transmitted range point to valid storage.</span></span>

<span data-ttu-id="2ccb6-145">En el lado del servidor, el código auxiliar asigna almacenamiento a todos los elementos de la matriz, independientemente de que la **\[** [**longitud \_ sea**](length-is.md) **\]** o la **\[** [**última \_ sea**](last-is.md) **\]** el valor en el momento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-145">On the server side, the stub allocates storage for all array elements, regardless of the **\[**[**length\_is**](length-is.md)**\]** or **\[**[**last\_is**](last-is.md)**\]** value at the time of the call.</span></span> <span data-ttu-id="2ccb6-146">Esta característica puede afectar al rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-146">This feature can affect the performance of your application.</span></span>

<span data-ttu-id="2ccb6-147">No se aplican restricciones a las matrices de punteros únicos.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-147">No restrictions are placed on arrays of unique pointers.</span></span> <span data-ttu-id="2ccb6-148">En el cliente y en el servidor, el almacenamiento se asigna para punteros nulos.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-148">On both the client and the server, storage is allocated for null pointers.</span></span> <span data-ttu-id="2ccb6-149">Cuando los punteros no son NULL, los datos se colocan en el almacenamiento preasignado.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-149">When pointers are non-null, data is placed in preallocated storage.</span></span>

<span data-ttu-id="2ccb6-150">Un declarador de puntero opcional puede preceder al declarador de matriz.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-150">An optional pointer declarator can precede the array declarator.</span></span>

<span data-ttu-id="2ccb6-151">Cuando los punteros de referencia incrustados son **\[** [](out-idl.md) **\]** de solo salida, el código del administrador del servidor debe asignar valores válidos a la matriz de punteros de referencia.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-151">When embedded reference pointers are **\[**[**out**](out-idl.md)**\]**-only parameters, the server-manager code must assign valid values to the array of reference pointers.</span></span> <span data-ttu-id="2ccb6-152">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2ccb6-152">For example:</span></span>

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

<span data-ttu-id="2ccb6-153">El código auxiliar generado asigna la matriz y asigna valores NULL a todos los punteros incrustados en la matriz.</span><span class="sxs-lookup"><span data-stu-id="2ccb6-153">The generated stubs allocate the array and assign null values to all pointers embedded in the array.</span></span>

 

 