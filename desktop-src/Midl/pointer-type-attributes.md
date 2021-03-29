---
title: Atributos de tipo de puntero
description: Los atributos siguientes especifican las características de los punteros.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- MIDL, atributos, tipo de puntero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779891"
---
# <a name="pointer-type-attributes"></a><span data-ttu-id="3a749-104">Atributos de tipo de puntero</span><span class="sxs-lookup"><span data-stu-id="3a749-104">Pointer Type Attributes</span></span>

<span data-ttu-id="3a749-105">Los atributos siguientes especifican las características de los punteros.</span><span class="sxs-lookup"><span data-stu-id="3a749-105">The following attributes specify the characteristics of pointers.</span></span>



| <span data-ttu-id="3a749-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="3a749-106">Attribute</span></span>                                   | <span data-ttu-id="3a749-107">Uso</span><span class="sxs-lookup"><span data-stu-id="3a749-107">Usage</span></span>                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a749-108">**ptr**</span><span class="sxs-lookup"><span data-stu-id="3a749-108">**ptr**</span></span>](ptr.md)                          | <span data-ttu-id="3a749-109">Designa un puntero como un puntero completo, con todas las capacidades de un puntero de lenguaje C, incluido el alias.</span><span class="sxs-lookup"><span data-stu-id="3a749-109">Designates a pointer as a full pointer, with all the capabilities of a C-language pointer, including aliasing.</span></span>                                                                                       |
| [<span data-ttu-id="3a749-110">**ref**</span><span class="sxs-lookup"><span data-stu-id="3a749-110">**ref**</span></span>](ref.md)                          | <span data-ttu-id="3a749-111">Designa el tipo más simple de puntero en MIDL, uno que simplemente proporciona la dirección de algunos datos.</span><span class="sxs-lookup"><span data-stu-id="3a749-111">Designates the simplest type of pointer in MIDL—one that simply provides the address of some data.</span></span> <span data-ttu-id="3a749-112">Los punteros de referencia nunca pueden ser null.</span><span class="sxs-lookup"><span data-stu-id="3a749-112">Reference pointers can never be null.</span></span>                                                             |
| [<span data-ttu-id="3a749-113">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="3a749-113">**unique**</span></span>](unique.md)                    | <span data-ttu-id="3a749-114">Permite que un puntero sea NULL, pero no admite el alias.</span><span class="sxs-lookup"><span data-stu-id="3a749-114">Lets a pointer be null, but does not support aliasing.</span></span>                                                                                                                                               |
| [<span data-ttu-id="3a749-115">**puntero \_ predeterminado**</span><span class="sxs-lookup"><span data-stu-id="3a749-115">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="3a749-116">Se aplica a una interfaz para especificar el tipo de puntero predeterminado para todos los punteros de la interfaz, excepto para los punteros de parámetros de nivel superior, que automáticamente tienen como valor predeterminado los punteros de [**referencia**](ref.md) .</span><span class="sxs-lookup"><span data-stu-id="3a749-116">Applied to an interface to specify the default pointer type for all pointers in that interface, except for top-level parameter pointers, which automatically default to [**ref**](ref.md) pointers.</span></span> |
| [<span data-ttu-id="3a749-117">**IID \_ es**</span><span class="sxs-lookup"><span data-stu-id="3a749-117">**iid\_is**</span></span>](iid-is.md)                   | <span data-ttu-id="3a749-118">Proporciona el identificador de interfaz de la interfaz COM que es el objeto del puntero.</span><span class="sxs-lookup"><span data-stu-id="3a749-118">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                                                                                            |
| [<span data-ttu-id="3a749-119">**string**</span><span class="sxs-lookup"><span data-stu-id="3a749-119">**string**</span></span>](string.md)                    | <span data-ttu-id="3a749-120">Especifica que el puntero apunta a una cadena.</span><span class="sxs-lookup"><span data-stu-id="3a749-120">Specifies that the pointer points to a string.</span></span>                                                                                                                                                       |



 

 

 




