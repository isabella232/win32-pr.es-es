---
title: Recurso de menú
description: Define el contenido de un recurso de menú. | Recurso de menú
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- Menús de recursos de menú y otros recursos
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717516"
---
# <a name="menu-resource"></a><span data-ttu-id="070c3-105">Recurso de menú</span><span class="sxs-lookup"><span data-stu-id="070c3-105">MENU resource</span></span>

<span data-ttu-id="070c3-106">Define el contenido de un recurso de menú.</span><span class="sxs-lookup"><span data-stu-id="070c3-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="070c3-107">Un recurso de menú es una colección de información que define la apariencia y la función de un menú de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="070c3-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="070c3-108">Un menú es una herramienta de entrada especial que permite a un usuario seleccionar comandos y abrir submenús en una lista de elementos de menú.</span><span class="sxs-lookup"><span data-stu-id="070c3-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span>

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a><span data-ttu-id="070c3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="070c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="070c3-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span><span class="sxs-lookup"><span data-stu-id="070c3-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span></span>
</dt> <dd>

<span data-ttu-id="070c3-111">Número que identifica el menú.</span><span class="sxs-lookup"><span data-stu-id="070c3-111">Number that identifies the menu.</span></span> <span data-ttu-id="070c3-112">Este valor es una cadena única o un valor entero de 16 bits sin signo único en el intervalo de 1 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="070c3-112">This value is either a unique string or a unique 16-bit unsigned integer value in the range of 1 to 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="070c3-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instrucciones opcionales*</span><span class="sxs-lookup"><span data-stu-id="070c3-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="070c3-114">Este parámetro puede ser cero de las siguientes instrucciones.</span><span class="sxs-lookup"><span data-stu-id="070c3-114">This parameter can be zero of more of the following statements.</span></span>



| <span data-ttu-id="070c3-115">.</span><span class="sxs-lookup"><span data-stu-id="070c3-115">Statement</span></span>                                                        | <span data-ttu-id="070c3-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="070c3-116">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070c3-117">[**Características**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="070c3-117">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="070c3-118">Información definida por el usuario sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="070c3-118">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="070c3-119">Para obtener más información, vea [**características**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="070c3-119">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="070c3-120">[](language-statement.md) *Idioma* del idioma, *subidioma*</span><span class="sxs-lookup"><span data-stu-id="070c3-120">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="070c3-121">Idioma del recurso.</span><span class="sxs-lookup"><span data-stu-id="070c3-121">Language for the resource.</span></span> <span data-ttu-id="070c3-122">Para obtener más información, vea [**Language**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="070c3-122">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="070c3-123">[**Versión**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="070c3-123">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="070c3-124">Número de versión definido por el usuario para el recurso que pueden usar las herramientas que leen y escriben archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="070c3-124">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="070c3-125">Para obtener más información, vea [**versión**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="070c3-125">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> </dl>

<span data-ttu-id="070c3-126">Algunos atributos también se admiten por razones de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="070c3-126">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="070c3-127">Para obtener más información, vea [atributos comunes de recursos](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="070c3-127">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="070c3-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="070c3-128">Examples</span></span>

<span data-ttu-id="070c3-129">El siguiente es un ejemplo de una instrucción de **menú** completa:</span><span class="sxs-lookup"><span data-stu-id="070c3-129">The following is an example of a complete **MENU** statement:</span></span>

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a><span data-ttu-id="070c3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="070c3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="070c3-131">Uso de los menús</span><span class="sxs-lookup"><span data-stu-id="070c3-131">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="070c3-132">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="070c3-132">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="070c3-133">**SUS**</span><span class="sxs-lookup"><span data-stu-id="070c3-133">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="070c3-134">**MÓDULO**</span><span class="sxs-lookup"><span data-stu-id="070c3-134">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="070c3-135">**MENUEX**</span><span class="sxs-lookup"><span data-stu-id="070c3-135">**MENUEX**</span></span>](menuex-resource.md)
</dt> <dt>

[<span data-ttu-id="070c3-136">**OBJETOS**</span><span class="sxs-lookup"><span data-stu-id="070c3-136">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="070c3-137">**EMERGENTE**</span><span class="sxs-lookup"><span data-stu-id="070c3-137">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="070c3-138">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="070c3-138">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="070c3-139">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="070c3-139">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="070c3-140">**Versión**</span><span class="sxs-lookup"><span data-stu-id="070c3-140">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
