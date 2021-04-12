---
description: El uso de comas y puntos y comas puede ser el problema de sintaxis más complejo en el formato de archivo, y este uso es muy estricto. Las comas se usan para separar los miembros de la matriz; los puntos y comas terminan cada elemento de datos.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Uso de comas y puntos y comas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba238d50ff5d0dace017f16b75547df6b016e14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152686"
---
# <a name="use-of-commas-and-semicolons"></a><span data-ttu-id="7e218-104">Uso de comas y puntos y comas</span><span class="sxs-lookup"><span data-stu-id="7e218-104">Use of Commas and Semicolons</span></span>

<span data-ttu-id="7e218-105">El uso de comas y puntos y comas puede ser el problema de sintaxis más complejo en el formato de archivo, y este uso es muy estricto.</span><span class="sxs-lookup"><span data-stu-id="7e218-105">Using commas and semicolons can be the most complex syntax issue in the file format, and this usage is very strict.</span></span> <span data-ttu-id="7e218-106">Las comas se usan para separar los miembros de la matriz; los puntos y comas terminan cada elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="7e218-106">Commas are used to separate array members; semicolons terminate each data item.</span></span>

<span data-ttu-id="7e218-107">Por ejemplo, si una plantilla se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7e218-107">For example, if a template is defined in the following manner:</span></span>


```
template mytemp {
DWORD myvar;
}
```



<span data-ttu-id="7e218-108">Después, una instancia de esta plantilla tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="7e218-108">Then an instance of this template looks like the following:</span></span>


```
mytemp dataTemp {
1;
}
```



<span data-ttu-id="7e218-109">Si una plantilla que contiene otra plantilla se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7e218-109">If a template containing another template is defined in the following manner;</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



<span data-ttu-id="7e218-110">Después, una instancia de esta plantilla tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="7e218-110">Then an instance of this template looks like the following:</span></span>


```
container dataContainer {
1.1;
2; 
3;;
}
```



<span data-ttu-id="7e218-111">Tenga en cuenta que la segunda línea que representa el contenedor de mi Temp tiene dos puntos y coma al final de la línea.</span><span class="sxs-lookup"><span data-stu-id="7e218-111">Note that the second line that represents the mytemp inside container has two semicolons at the end of the line.</span></span> <span data-ttu-id="7e218-112">El primer punto y coma indica el final del elemento de datos, aTemp (dentro del contenedor) y el segundo punto y coma indica el final del contenedor.</span><span class="sxs-lookup"><span data-stu-id="7e218-112">The first semicolon indicates the end of the data item, aTemp (inside container), and the second semicolon indicates the end of the container.</span></span>

<span data-ttu-id="7e218-113">Si una matriz se define de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="7e218-113">If an array is defined in the following manner:</span></span>


```
Template mytemp {

array DWORD myvar[3];

}
```



<span data-ttu-id="7e218-114">Después, una instancia de se parece a la siguiente:</span><span class="sxs-lookup"><span data-stu-id="7e218-114">Then an instance of this looks like the following:</span></span>


```
mytemp aTemp {
1, 2, 3;
}
```



<span data-ttu-id="7e218-115">En el ejemplo de matriz, no es necesario separar los elementos de datos con punto y coma, porque se delimitan mediante comas.</span><span class="sxs-lookup"><span data-stu-id="7e218-115">In the array example, there is no need for the data items to be separated by semicolons because they are delineated by commas.</span></span> <span data-ttu-id="7e218-116">El punto y coma al final marca el final de la matriz.</span><span class="sxs-lookup"><span data-stu-id="7e218-116">The semicolon at the end marks the end of the array.</span></span>

<span data-ttu-id="7e218-117">Considere una plantilla que contiene una matriz de elementos de datos definida por una plantilla.</span><span class="sxs-lookup"><span data-stu-id="7e218-117">Consider a template that contains an array of data items defined by a template.</span></span>


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



<span data-ttu-id="7e218-118">Una instancia de esto sería similar al ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="7e218-118">An instance of this would look like the following example.</span></span>


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a><span data-ttu-id="7e218-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e218-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e218-120">Codificación de texto</span><span class="sxs-lookup"><span data-stu-id="7e218-120">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



