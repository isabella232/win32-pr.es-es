---
description: Los objetos de datos contienen los datos reales o una referencia a esos datos. Cada objeto de datos tiene una plantilla correspondiente que especifica el tipo de datos. En las secciones siguientes se describen el formulario y los elementos de los objetos de datos.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Datos (formato de archivo X, codificación de texto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422967"
---
# <a name="data-x-file-format-text-encoding"></a><span data-ttu-id="ce0ce-105">Datos (formato de archivo X, codificación de texto)</span><span class="sxs-lookup"><span data-stu-id="ce0ce-105">Data (X file format, text encoding)</span></span>

<span data-ttu-id="ce0ce-106">Los objetos de datos contienen los datos reales o una referencia a esos datos.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-106">Data objects contain the actual data or a reference to that data.</span></span> <span data-ttu-id="ce0ce-107">Cada objeto de datos tiene una plantilla correspondiente que especifica el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-107">Each data object has a corresponding template that specifies the data type.</span></span> <span data-ttu-id="ce0ce-108">En las secciones siguientes se describen el formulario y los elementos de los objetos de datos.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-108">The following sections discuss the form and parts of data objects.</span></span>

## <a name="form-identifier-and-name"></a><span data-ttu-id="ce0ce-109">Formulario, identificador y nombre</span><span class="sxs-lookup"><span data-stu-id="ce0ce-109">Form, Identifier, and Name</span></span>

<span data-ttu-id="ce0ce-110">Los objetos de datos tienen el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-110">Data objects have the following form.</span></span>


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



<span data-ttu-id="ce0ce-111">El identificador es obligatorio y debe coincidir con un tipo de datos o primitivo definido previamente.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-111">The identifier is compulsory and must match a previously defined data type or primitive.</span></span> <span data-ttu-id="ce0ce-112">Sin embargo, el nombre es opcional.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-112">However, the name is optional.</span></span>

## <a name="data-members"></a><span data-ttu-id="ce0ce-113">Miembros de datos</span><span class="sxs-lookup"><span data-stu-id="ce0ce-113">Data Members</span></span>

<span data-ttu-id="ce0ce-114">Los miembros de datos pueden ser uno de los siguientes: objeto de datos, referencia de datos, lista de enteros, lista flotante o lista de cadenas.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-114">Data members can be one of the following: data object, data reference, integer list, float list, or string list.</span></span>

<span data-ttu-id="ce0ce-115">Un objeto de datos es un objeto de datos anidados.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-115">A data object is a nested data object.</span></span> <span data-ttu-id="ce0ce-116">Esto permite expresar la naturaleza jerárquica del formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-116">This enables the hierarchical nature of the file format to be expressed.</span></span> <span data-ttu-id="ce0ce-117">Los tipos de objetos de datos anidados permitidos en la jerarquía pueden estar restringidos.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-117">The types of nested data objects allowed in the hierarchy may be restricted.</span></span>

<span data-ttu-id="ce0ce-118">Una referencia de datos es una referencia a un objeto de datos encontrado anteriormente, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-118">A data reference is a reference to a previously encountered data object as shown in the following example.</span></span>


```
{
  name |
  UUID |
  name UUID
}
```



<span data-ttu-id="ce0ce-119">Una lista de enteros es una lista de enteros separada por punto y coma, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-119">An integer list is a semicolon-separated list of integers, as shown in the following example.</span></span>


```
1; 2; 3;
```



<span data-ttu-id="ce0ce-120">Una lista Float es una lista separada por punto y coma de valores Float, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-120">A float list is a semicolon-separated list of floats, as shown in the following example.</span></span>


```
1.0; 2.0; 3.0;
```



<span data-ttu-id="ce0ce-121">Una lista de cadenas es una lista separada por punto y coma de cadenas, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ce0ce-121">A string list is a semicolon-separated list of strings, as shown in the following example.</span></span>


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a><span data-ttu-id="ce0ce-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce0ce-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce0ce-123">Codificación de texto</span><span class="sxs-lookup"><span data-stu-id="ce0ce-123">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



