---
title: Elemento BASE
description: El elemento BASE define una cadena de dirección URL anexada al principio de las direcciones URL enviadas a Windows Media Player.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Windows Media Player de elementos BASE
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700007"
---
# <a name="base-element"></a><span data-ttu-id="89cc4-104">Elemento BASE</span><span class="sxs-lookup"><span data-stu-id="89cc4-104">BASE Element</span></span>

<span data-ttu-id="89cc4-105">El elemento **base** define una cadena de dirección URL anexada al principio de las direcciones URL enviadas a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="89cc4-105">The **BASE** element defines a URL string appended to the front of URLs sent to Windows Media Player.</span></span>

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="89cc4-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="89cc4-106">Attributes</span></span>

<span data-ttu-id="89cc4-107">**Href** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="89cc4-107">**HREF** (required)</span></span>

<span data-ttu-id="89cc4-108">Cadena anexada al frente a las direcciones URL enviadas a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="89cc4-108">The string appended to the front to URLs sent to Windows Media Player.</span></span> <span data-ttu-id="89cc4-109">El valor predeterminado es la cadena nula ("").</span><span class="sxs-lookup"><span data-stu-id="89cc4-109">The default value is the null string ("").</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="89cc4-110">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="89cc4-110">Parent/Child Elements</span></span>



| <span data-ttu-id="89cc4-111">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="89cc4-111">Hierarchy</span></span>       | <span data-ttu-id="89cc4-112">Elementos</span><span class="sxs-lookup"><span data-stu-id="89cc4-112">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="89cc4-113">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="89cc4-113">Parent elements</span></span> | <span data-ttu-id="89cc4-114">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="89cc4-114">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="89cc4-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="89cc4-115">Child elements</span></span>  | <span data-ttu-id="89cc4-116">Ninguno</span><span class="sxs-lookup"><span data-stu-id="89cc4-116">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="89cc4-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89cc4-117">Remarks</span></span>

<span data-ttu-id="89cc4-118">Este elemento define una cadena de dirección URL anexada al principio de las direcciones URL de volteo de URL enviadas a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="89cc4-118">This element defines a URL string appended to the front of URL-flip URLs sent to Windows Media Player.</span></span> <span data-ttu-id="89cc4-119">URL: el volteo es un mecanismo de scripting que hace que Windows Media Player abra una nueva dirección URL en un explorador o marco del explorador cuando recibe un comando de script.</span><span class="sxs-lookup"><span data-stu-id="89cc4-119">URL-flipping is a scripting mechanism that causes Windows Media Player to open a new URL in a browser or browser frame when it receives a script command.</span></span>

<span data-ttu-id="89cc4-120">El elemento **base** es similar a un directorio particular para los vínculos relativos.</span><span class="sxs-lookup"><span data-stu-id="89cc4-120">The **BASE** element is similar to a home directory for relative links.</span></span> <span data-ttu-id="89cc4-121">Solo afecta a las direcciones URL enviadas mediante comandos de script como parte del flujo de contenido que se reproduce en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="89cc4-121">It only affects URLs sent using script commands as part of the content stream that is playing in Windows Media Player.</span></span>

<span data-ttu-id="89cc4-122">Un elemento **base** definido como elemento secundario de un elemento **ASX** se convierte en el valor predeterminado para todo el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="89cc4-122">A **BASE** element defined as the child of an **ASX** element becomes the default for the entire metafile.</span></span> <span data-ttu-id="89cc4-123">Un elemento **base** definido en un elemento **entry** reemplaza cualquier elemento **base** del elemento **ASX** primario (solo para ese elemento **entry** ).</span><span class="sxs-lookup"><span data-stu-id="89cc4-123">A **BASE** element defined in an **ENTRY** element overrides any **BASE** element in the parent **ASX** element (for that **ENTRY** element only).</span></span>

> [!Note]  
> <span data-ttu-id="89cc4-124">Si el atributo **href** no termina con un carácter/, Windows Media Player anexa uno al final de la cadena.</span><span class="sxs-lookup"><span data-stu-id="89cc4-124">If the **HREF** attribute does not end with a / character, Windows Media Player appends one to the end of the string.</span></span>

 

## <a name="examples"></a><span data-ttu-id="89cc4-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="89cc4-125">Examples</span></span>


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a><span data-ttu-id="89cc4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89cc4-126">Requirements</span></span>



| <span data-ttu-id="89cc4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="89cc4-127">Requirement</span></span> | <span data-ttu-id="89cc4-128">Value</span><span class="sxs-lookup"><span data-stu-id="89cc4-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="89cc4-129">Versión</span><span class="sxs-lookup"><span data-stu-id="89cc4-129">Version</span></span><br/> | <span data-ttu-id="89cc4-130">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="89cc4-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89cc4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="89cc4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89cc4-132">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="89cc4-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="89cc4-133">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="89cc4-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





