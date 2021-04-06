---
title: Punteros únicos
description: En los programas de C, más de un puntero puede contener la dirección de los datos.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077788"
---
# <a name="unique-pointers"></a><span data-ttu-id="8cfdb-103">Punteros únicos</span><span class="sxs-lookup"><span data-stu-id="8cfdb-103">Unique Pointers</span></span>

<span data-ttu-id="8cfdb-104">En los programas de C, más de un puntero puede contener la dirección de los datos.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-104">In C programs, more than one pointer can contain the address of data.</span></span> <span data-ttu-id="8cfdb-105">Se dice que los punteros crean un [*alias*](a-glos.md) para los datos.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-105">The pointers are said to create an [*alias*](a-glos.md) for the data.</span></span> <span data-ttu-id="8cfdb-106">Los alias también se crean cuando los punteros apuntan a variables declaradas.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-106">Aliases are also created when pointers point at declared variables.</span></span> <span data-ttu-id="8cfdb-107">En el fragmento de código siguiente se muestran ambos métodos de alias:</span><span class="sxs-lookup"><span data-stu-id="8cfdb-107">The following code fragment illustrates both of these methods of aliasing:</span></span>


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



<span data-ttu-id="8cfdb-108">En un programa de C típico, puede especificar un árbol binario con la siguiente definición:</span><span class="sxs-lookup"><span data-stu-id="8cfdb-108">In a typical C program, you might specify a binary tree using the following definition:</span></span>


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



<span data-ttu-id="8cfdb-109">Más de un puntero puede tener acceso al contenido de un nodo de árbol.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-109">More than one pointer can access the contents of a tree node.</span></span> <span data-ttu-id="8cfdb-110">Normalmente, esto es correcto para las aplicaciones no distribuidas.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-110">This is generally fine for nondistributed applications.</span></span> <span data-ttu-id="8cfdb-111">Sin embargo, este estilo de programación genera código de compatibilidad con RPC más complicado.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-111">However, this style of programming generates more complicated RPC support code.</span></span> <span data-ttu-id="8cfdb-112">Los códigos auxiliares de cliente y servidor requieren el código adicional para administrar los datos y los punteros.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-112">The client and server stubs require the additional code to manage the data and the pointers.</span></span> <span data-ttu-id="8cfdb-113">El código auxiliar subyacente debe resolver los distintos punteros a las direcciones y determinar qué copia de los datos representan la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-113">The underlying stub code must resolve the various pointers to the addresses and determine which copy of the data represents the most recent version.</span></span>

<span data-ttu-id="8cfdb-114">Se puede reducir la cantidad de procesamiento si garantiza que el puntero es la única manera en que la aplicación puede tener acceso a ese área de memoria.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-114">The amount of processing can be reduced if you guarantee that your pointer is the only way the application can access that area of memory.</span></span> <span data-ttu-id="8cfdb-115">El puntero puede seguir teniendo muchas de las características de un puntero de C.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-115">The pointer can still have many of the features of a C pointer.</span></span> <span data-ttu-id="8cfdb-116">Por ejemplo, puede cambiar entre valores **null** y distintos de **null** o permanecer igual.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-116">For example, it can change between **null** and non-**null** values or stay the same.</span></span> <span data-ttu-id="8cfdb-117">Esto se ilustra en el siguiente ejemplo:</span><span class="sxs-lookup"><span data-stu-id="8cfdb-117">The following example illustrates this.</span></span> <span data-ttu-id="8cfdb-118">El puntero es **null** antes de la llamada y apunta a una cadena válida después de la llamada:</span><span class="sxs-lookup"><span data-stu-id="8cfdb-118">The pointer is **null** before the call and points to a valid string after the call:</span></span>

![cambio de puntero entre valores NULL y no NULL](images/prog-a01.png)

<span data-ttu-id="8cfdb-120">De forma predeterminada, el compilador MIDL aplica el \[ [](/windows/desktop/Midl/unique) \] atributo de puntero único a todos los punteros que no son parámetros.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-120">By default, the MIDL compiler applies the \[ [unique](/windows/desktop/Midl/unique)\] pointer attribute to all pointers that are not parameters.</span></span> <span data-ttu-id="8cfdb-121">Esta configuración predeterminada se puede cambiar con el \[ [atributo \_ default del puntero](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="8cfdb-121">This default setting can be changed with the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] attribute.</span></span>

<span data-ttu-id="8cfdb-122">Un puntero único tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="8cfdb-122">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="8cfdb-123">Puede tener el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-123">It can have the value **null**.</span></span>
-   <span data-ttu-id="8cfdb-124">Puede cambiar de **null** a un valor distinto de **null** durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-124">It can change from **null** to non-**null** during the call.</span></span> <span data-ttu-id="8cfdb-125">Cuando el valor cambia a no **null**, se asigna una nueva memoria al volver.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-125">When the value changes to non-**null**, new memory is allocated on return.</span></span>
-   <span data-ttu-id="8cfdb-126">Puede cambiar de un valor distinto de **null** a **null** durante la llamada.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-126">It can change from non-**null** to **null** during the call.</span></span> <span data-ttu-id="8cfdb-127">Cuando el valor cambia a **null**, la aplicación es responsable de liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-127">When the value changes to **NULL**, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="8cfdb-128">El valor puede cambiar de un valor distinto de **null** a otro.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-128">The value can change from one non-**null** value to another.</span></span>
-   <span data-ttu-id="8cfdb-129">No se puede tener acceso al almacenamiento al que apunta un puntero único en ningún otro puntero o nombre de la operación.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-129">The storage that a unique pointer points to cannot be accessed by any other pointer or name in the operation.</span></span>
-   <span data-ttu-id="8cfdb-130">Los datos devueltos se escriben en el almacenamiento existente si el puntero no tiene el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-130">Return data is written into existing storage if the pointer does not have the value **null**.</span></span>

<span data-ttu-id="8cfdb-131">En el ejemplo siguiente se muestra cómo definir un puntero único.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-131">The following example demonstrates how to define a unique pointer.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

<span data-ttu-id="8cfdb-132">En este ejemplo, el parámetro *ACH* es un puntero único a los datos de caracteres que se envía a un servidor que se va a procesar con la rutina RemoteFn.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-132">In this example, the parameter *ach* is a unique pointer to character data that is sent to a server to be processed with the RemoteFn routine.</span></span>

 

 