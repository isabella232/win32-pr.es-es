---
title: pointer_default (atributo)
description: El atributo \ Pointer \_ default \ especifica el atributo de puntero predeterminado para todos los punteros, excepto los punteros de nivel superior que aparecen en las listas de parámetros.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default el atributo MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077606"
---
# <a name="pointer_default-attribute"></a><span data-ttu-id="8f211-104">\_atributo default del puntero</span><span class="sxs-lookup"><span data-stu-id="8f211-104">pointer\_default attribute</span></span>

<span data-ttu-id="8f211-105">El atributo **\[ \_ default \] Pointer** especifica el atributo de puntero predeterminado para todos los punteros, excepto los punteros de nivel superior que aparecen en las listas de parámetros.</span><span class="sxs-lookup"><span data-stu-id="8f211-105">The **\[pointer\_default\]** attribute specifies the default pointer attribute for all pointers except top-level pointers that appear in parameter lists.</span></span>

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a><span data-ttu-id="8f211-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f211-106">Parameters</span></span>

<span data-ttu-id="8f211-107">Este atributo no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8f211-107">This attribute has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="8f211-108">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8f211-108">Examples</span></span>

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="8f211-109">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f211-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f211-110">**interfaz**</span><span class="sxs-lookup"><span data-stu-id="8f211-110">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="8f211-111">Atributos array y Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="8f211-111">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="8f211-112">**matrices**</span><span class="sxs-lookup"><span data-stu-id="8f211-112">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="8f211-113">Matrices y punteros</span><span class="sxs-lookup"><span data-stu-id="8f211-113">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="8f211-114">**ptr**</span><span class="sxs-lookup"><span data-stu-id="8f211-114">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="8f211-115">**ref**</span><span class="sxs-lookup"><span data-stu-id="8f211-115">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="8f211-116">**espeficarse**</span><span class="sxs-lookup"><span data-stu-id="8f211-116">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="8f211-117">Tipos de puntero predeterminados</span><span class="sxs-lookup"><span data-stu-id="8f211-117">Default Pointer Types</span></span>](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 