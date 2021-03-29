---
description: En esta sección se describen las estructuras que puede usar para desarrollar analizadores. Estas estructuras las utilizan las funciones que puede usar para desarrollar analizadores y funciones que puede usar para desarrollar analizadores o expertos.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Estructuras de analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a9b767974214472f24ea9e1ec9359c97d26fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003215"
---
# <a name="parser-structures"></a><span data-ttu-id="e66d8-104">Estructuras de analizador</span><span class="sxs-lookup"><span data-stu-id="e66d8-104">Parser Structures</span></span>

<span data-ttu-id="e66d8-105">En esta sección se describen las estructuras que puede usar para desarrollar analizadores.</span><span class="sxs-lookup"><span data-stu-id="e66d8-105">This section describes structures you can use to develop parsers.</span></span> <span data-ttu-id="e66d8-106">Estas estructuras las utilizan las funciones que puede usar para desarrollar analizadores y funciones que puede usar para desarrollar analizadores o expertos.</span><span class="sxs-lookup"><span data-stu-id="e66d8-106">These structures are used by functions you can use to develop parsers and functions you can use to develop either parsers or experts.</span></span>



| <span data-ttu-id="e66d8-107">Estructura</span><span class="sxs-lookup"><span data-stu-id="e66d8-107">Structure</span></span>                                 | <span data-ttu-id="e66d8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e66d8-108">Description</span></span>                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e66d8-109">MACFRAME</span><span class="sxs-lookup"><span data-stu-id="e66d8-109">MACFRAME</span></span>](macframe.md)                  | <span data-ttu-id="e66d8-110">Define los protocolos iniciales que se usan con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="e66d8-110">Defines the most commonly used initial protocols.</span></span>                                                                               |
| [<span data-ttu-id="e66d8-111">ENTRYPOINTS</span><span class="sxs-lookup"><span data-stu-id="e66d8-111">ENTRYPOINTS</span></span>](entrypoints.md)            | <span data-ttu-id="e66d8-112">Especifica punteros a los puntos de entrada de la DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="e66d8-112">Specifies pointers to the entry points for the Parser DLL.</span></span>                                                                      |
| [<span data-ttu-id="e66d8-113">PF \_ FOLLOWENTRY</span><span class="sxs-lookup"><span data-stu-id="e66d8-113">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)     | <span data-ttu-id="e66d8-114">Especifica el protocolo que sigue al protocolo actual.</span><span class="sxs-lookup"><span data-stu-id="e66d8-114">Specifies the protocol that follows the current protocol.</span></span>                                                                       |
| [<span data-ttu-id="e66d8-115">PF \_ FOLLOWSET</span><span class="sxs-lookup"><span data-stu-id="e66d8-115">PF\_FOLLOWSET</span></span>](pf-followset.md)         | <span data-ttu-id="e66d8-116">Especifica el conjunto de protocolos que sigue el protocolo actual.</span><span class="sxs-lookup"><span data-stu-id="e66d8-116">Specifies the set of protocols that follows the current protocol.</span></span>                                                               |
| [<span data-ttu-id="e66d8-117">PF \_ HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="e66d8-117">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)   | <span data-ttu-id="e66d8-118">Especifica el protocolo que se entrega en el protocolo actual o el protocolo al que el protocolo actual se entrega.</span><span class="sxs-lookup"><span data-stu-id="e66d8-118">Specifies either the protocol that hands off to the current protocol or the protocol that the current protocol hands off to.</span></span>    |
| [<span data-ttu-id="e66d8-119">PF \_ HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="e66d8-119">PF\_HANDOFFSET</span></span>](pf-handoffset.md)       | <span data-ttu-id="e66d8-120">Especifica el conjunto de protocolos que se entregan al protocolo actual o al conjunto de protocolos al que el protocolo actual se entrega.</span><span class="sxs-lookup"><span data-stu-id="e66d8-120">Specifies the set of protocols that hand off to the current protocol or the set of protocols the current protocol hands off to.</span></span> |
| [<span data-ttu-id="e66d8-121">PF \_ PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="e66d8-121">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md) | <span data-ttu-id="e66d8-122">Especifica el número de analizadores en el archivo DLL del analizador e información sobre cada analizador.</span><span class="sxs-lookup"><span data-stu-id="e66d8-122">Specifies the number of parsers in the parser DLL and information about each parser.</span></span>                                            |
| [<span data-ttu-id="e66d8-123">PF \_ PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="e66d8-123">PF\_PARSERINFO</span></span>](pf-parserinfo.md)       | <span data-ttu-id="e66d8-124">Especifica información sobre un analizador específico.</span><span class="sxs-lookup"><span data-stu-id="e66d8-124">Specifies information about a specific parser.</span></span>                                                                                  |
| [<span data-ttu-id="e66d8-125">BIT con etiqueta \_</span><span class="sxs-lookup"><span data-stu-id="e66d8-125">LABELED\_BIT</span></span>](labeled-bit.md)           | <span data-ttu-id="e66d8-126">Especifica los identificadores, los campos de bits o las marcas.</span><span class="sxs-lookup"><span data-stu-id="e66d8-126">Specifies handles, BIT fields, or flags.</span></span>                                                                                        |
| [<span data-ttu-id="e66d8-127">BYTE con etiqueta \_</span><span class="sxs-lookup"><span data-stu-id="e66d8-127">LABELED\_BYTE</span></span>](labeled-byte.md)         | <span data-ttu-id="e66d8-128">Especifica un par de etiqueta de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="e66d8-128">Specifies a **BYTE** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="e66d8-129">DWORD con etiqueta \_</span><span class="sxs-lookup"><span data-stu-id="e66d8-129">LABELED\_DWORD</span></span>](labeled-dword.md)       | <span data-ttu-id="e66d8-130">Especifica un par de etiquetas **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e66d8-130">Specifies a **DWORD** label pair.</span></span>                                                                                               |
| [<span data-ttu-id="e66d8-131">palabra con etiqueta \_</span><span class="sxs-lookup"><span data-stu-id="e66d8-131">LABELED\_WORD</span></span>](labeled-word.md)         | <span data-ttu-id="e66d8-132">Especifica un par de etiqueta de **palabra** .</span><span class="sxs-lookup"><span data-stu-id="e66d8-132">Specifies a **WORD** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="e66d8-133">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="e66d8-133">PROPERTYINFO</span></span>](propertyinfo.md)          | <span data-ttu-id="e66d8-134">Especifica las propiedades que el analizador de protocolo requiere para describir los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="e66d8-134">Specifies the properties that the protocol parser requires to describe frames.</span></span>                                                  |
| [<span data-ttu-id="e66d8-135">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="e66d8-135">PROPERTYINST</span></span>](propertyinst.md)          | <span data-ttu-id="e66d8-136">Especifica una instancia de una propiedad en un marco.</span><span class="sxs-lookup"><span data-stu-id="e66d8-136">Specifies an instance of a property in a frame.</span></span>                                                                                 |
| [<span data-ttu-id="e66d8-137">PROPERTYINSTEX</span><span class="sxs-lookup"><span data-stu-id="e66d8-137">PROPERTYINSTEX</span></span>](propertyinstex.md)      | <span data-ttu-id="e66d8-138">Especifica una instancia de propiedad extendida de forma libre.</span><span class="sxs-lookup"><span data-stu-id="e66d8-138">Specifies a free-form, extended property instance.</span></span>                                                                              |
| [<span data-ttu-id="e66d8-139">PROTOCOLINFO</span><span class="sxs-lookup"><span data-stu-id="e66d8-139">PROTOCOLINFO</span></span>](protocolinfo.md)          | <span data-ttu-id="e66d8-140">Especifica un protocolo.</span><span class="sxs-lookup"><span data-stu-id="e66d8-140">Specifies a protocol.</span></span>                                                                                                           |
| [<span data-ttu-id="e66d8-141">VARIEDAD</span><span class="sxs-lookup"><span data-stu-id="e66d8-141">RANGE</span></span>](range.md)                        | <span data-ttu-id="e66d8-142">Especifica un intervalo para un número.</span><span class="sxs-lookup"><span data-stu-id="e66d8-142">Specifies a range for a number.</span></span>                                                                                                 |
| [<span data-ttu-id="e66d8-143">SET</span><span class="sxs-lookup"><span data-stu-id="e66d8-143">SET</span></span>](set.md)                            | <span data-ttu-id="e66d8-144">Especifica una tabla de valores para una propiedad.</span><span class="sxs-lookup"><span data-stu-id="e66d8-144">Specifies a table of values for a property.</span></span>                                                                                     |



 

<span data-ttu-id="e66d8-145">Para obtener información acerca de las funciones utilizadas para desarrollar archivos dll de analizador, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="e66d8-145">For information about functions used to develop parser DLLs, see the following topics.</span></span>



| <span data-ttu-id="e66d8-146">Para información acerca de</span><span class="sxs-lookup"><span data-stu-id="e66d8-146">For information about</span></span>                                         | <span data-ttu-id="e66d8-147">Vea</span><span class="sxs-lookup"><span data-stu-id="e66d8-147">See</span></span>                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e66d8-148">Funciones que exportan los archivos DLL del analizador.</span><span class="sxs-lookup"><span data-stu-id="e66d8-148">Functions that the parser DLLs export.</span></span>                        | [<span data-ttu-id="e66d8-149">Funciones de exportación de DLL de analizador</span><span class="sxs-lookup"><span data-stu-id="e66d8-149">Parser DLL Export Functions</span></span>](parser-dll-export-functions.md)               |
| <span data-ttu-id="e66d8-150">Funciones que se pueden usar para desarrollar archivos dll de analizador.</span><span class="sxs-lookup"><span data-stu-id="e66d8-150">Functions that you can use to develop parser DLLs.</span></span>            | [<span data-ttu-id="e66d8-151">Funciones de analizador</span><span class="sxs-lookup"><span data-stu-id="e66d8-151">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="e66d8-152">Funciones que puede usar para desarrollar archivos dll de analizador y expertos.</span><span class="sxs-lookup"><span data-stu-id="e66d8-152">Functions that you can use to develop parser and expert DLLs.</span></span> | [<span data-ttu-id="e66d8-153">Funciones comunes de experto y analizador</span><span class="sxs-lookup"><span data-stu-id="e66d8-153">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



