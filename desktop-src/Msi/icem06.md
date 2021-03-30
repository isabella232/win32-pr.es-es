---
description: ICEM06 comprueba las referencias directas no válidas a las características del módulo.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910381"
---
# <a name="icem06"></a><span data-ttu-id="11c57-103">ICEM06</span><span class="sxs-lookup"><span data-stu-id="11c57-103">ICEM06</span></span>

<span data-ttu-id="11c57-104">ICEM06 comprueba las referencias directas no válidas a las características del módulo.</span><span class="sxs-lookup"><span data-stu-id="11c57-104">ICEM06 checks for invalid direct references to features by the module.</span></span>

<span data-ttu-id="11c57-105">El módulo de combinación ICEs se almacena en un archivo. Cub de módulo de combinación denominado Mergemod. Cub y no en el archivo. Cub que contiene el ICEs usado para la validación del paquete.</span><span class="sxs-lookup"><span data-stu-id="11c57-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="11c57-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="11c57-106">Result</span></span>

<span data-ttu-id="11c57-107">ICEM06 expone un error cuando la base de datos del módulo contiene referencias directas a una característica.</span><span class="sxs-lookup"><span data-stu-id="11c57-107">ICEM06 posts an error when the module database contains direct references to a feature.</span></span> <span data-ttu-id="11c57-108">El usuario del módulo debe proporcionar la información de características.</span><span class="sxs-lookup"><span data-stu-id="11c57-108">Feature information must be provided by the user of the module.</span></span>

## <a name="example"></a><span data-ttu-id="11c57-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11c57-109">Example</span></span>

<span data-ttu-id="11c57-110">ICEM06 expone los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="11c57-110">ICEM06 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

<span data-ttu-id="11c57-111">[Tabla de acceso directo](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="11c57-111">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="11c57-112">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="11c57-112">Shortcut</span></span>          | <span data-ttu-id="11c57-113">Destino</span><span class="sxs-lookup"><span data-stu-id="11c57-113">Target</span></span>                                 |
|-------------------|----------------------------------------|
| <span data-ttu-id="11c57-114">Shortcut1. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="11c57-114">Shortcut1.*GUID1*</span></span> | <span data-ttu-id="11c57-115">cmd.exe</span><span class="sxs-lookup"><span data-stu-id="11c57-115">cmd.exe</span></span>                                |
| <span data-ttu-id="11c57-116">Shortcut2. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="11c57-116">Shortcut2.*GUID1*</span></span> | <span data-ttu-id="11c57-117">\[Propiedades de\]</span><span class="sxs-lookup"><span data-stu-id="11c57-117">\[MyProp\]</span></span>                             |
| <span data-ttu-id="11c57-118">Shortcut3. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="11c57-118">Shortcut3.*GUID1*</span></span> | {00000000-0000-0000-0000-000000000000} |



 

<span data-ttu-id="11c57-119">[Tabla de clases](class-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="11c57-119">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="11c57-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="11c57-120">CLSID</span></span>   | <span data-ttu-id="11c57-121">Context</span><span class="sxs-lookup"><span data-stu-id="11c57-121">Context</span></span>       | <span data-ttu-id="11c57-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="11c57-122">Component\_</span></span> | <span data-ttu-id="11c57-123">Característica\_</span><span class="sxs-lookup"><span data-stu-id="11c57-123">Feature\_</span></span>                              |
|---------|---------------|-------------|----------------------------------------|
| <span data-ttu-id="11c57-124">*GUID1*</span><span class="sxs-lookup"><span data-stu-id="11c57-124">*GUID1*</span></span> | <span data-ttu-id="11c57-125">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="11c57-125">LocalServer32</span></span> | <span data-ttu-id="11c57-126">Component1</span><span class="sxs-lookup"><span data-stu-id="11c57-126">Component1</span></span>  | {00000000-0000-0000-0000-000000000000} |
| <span data-ttu-id="11c57-127">*GUID2*</span><span class="sxs-lookup"><span data-stu-id="11c57-127">*GUID2*</span></span> | <span data-ttu-id="11c57-128">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="11c57-128">LocalServer32</span></span> | <span data-ttu-id="11c57-129">Component2</span><span class="sxs-lookup"><span data-stu-id="11c57-129">Component2</span></span>  | <span data-ttu-id="11c57-130">Mi característica</span><span class="sxs-lookup"><span data-stu-id="11c57-130">MyFeature</span></span>                              |



 

<span data-ttu-id="11c57-131">ICEM06 informa del primer error porque el primer registro de la tabla de acceso directo tiene una entrada en el campo de destino que no es una propiedad o un GUID nulo.</span><span class="sxs-lookup"><span data-stu-id="11c57-131">ICEM06 reports the first error because the first record in the Shortcut table has an entry in the Target field that is not a property or a null GUID.</span></span> <span data-ttu-id="11c57-132">Un módulo no puede hacer referencia directamente a una característica.</span><span class="sxs-lookup"><span data-stu-id="11c57-132">A module cannot reference a feature directly.</span></span> <span data-ttu-id="11c57-133">El usuario del módulo debe proporcionar la información de características.</span><span class="sxs-lookup"><span data-stu-id="11c57-133">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="11c57-134">Para corregir este error, las referencias a una característica deben reemplazarse por un GUID nulo.</span><span class="sxs-lookup"><span data-stu-id="11c57-134">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

<span data-ttu-id="11c57-135">ICEM06 informa del segundo error porque el segundo registro de la tabla de la clase tiene una entrada en el campo de característica que no es un GUID nulo.</span><span class="sxs-lookup"><span data-stu-id="11c57-135">ICEM06 reports the second error because the second record in the Class table has an entry in the Feature field that is not a null GUID.</span></span> <span data-ttu-id="11c57-136">Un módulo no puede hacer referencia directamente a una característica.</span><span class="sxs-lookup"><span data-stu-id="11c57-136">A module cannot reference a feature directly.</span></span> <span data-ttu-id="11c57-137">El usuario del módulo debe proporcionar la información de características.</span><span class="sxs-lookup"><span data-stu-id="11c57-137">Feature information must be provided by the user of the module.</span></span> <span data-ttu-id="11c57-138">Para corregir este error, las referencias a una característica deben reemplazarse por un GUID nulo.</span><span class="sxs-lookup"><span data-stu-id="11c57-138">To fix this error, references to a feature should be replaced by a null GUID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11c57-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11c57-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11c57-140">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="11c57-140">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



