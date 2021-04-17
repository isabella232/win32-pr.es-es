---
title: EDITBOX. editStyle
description: El atributo editStyle especifica o recupera el estilo del control de cuadro de edición.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- EditStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699877"
---
# <a name="editboxeditstyle"></a><span data-ttu-id="897ae-104">EDITBOX. editStyle</span><span class="sxs-lookup"><span data-stu-id="897ae-104">EDITBOX.editStyle</span></span>

<span data-ttu-id="897ae-105">El atributo **editStyle** especifica o recupera el estilo del control de cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="897ae-105">The **editStyle** attribute specifies or retrieves the style of the edit box control.</span></span>

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a><span data-ttu-id="897ae-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="897ae-106">Possible Values</span></span>

<span data-ttu-id="897ae-107">Este atributo es una **cadena** de lectura/escritura que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="897ae-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="897ae-108">Value</span><span class="sxs-lookup"><span data-stu-id="897ae-108">Value</span></span>     | <span data-ttu-id="897ae-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="897ae-109">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="897ae-110">normal</span><span class="sxs-lookup"><span data-stu-id="897ae-110">normal</span></span>    | <span data-ttu-id="897ae-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="897ae-111">Default.</span></span> <span data-ttu-id="897ae-112">Muestra el texto normal en una sola línea.</span><span class="sxs-lookup"><span data-stu-id="897ae-112">Displays normal text on a single line.</span></span>                                 |
| <span data-ttu-id="897ae-113">password</span><span class="sxs-lookup"><span data-stu-id="897ae-113">password</span></span>  | <span data-ttu-id="897ae-114">Muestra asteriscos ( \* ) en lugar de texto.</span><span class="sxs-lookup"><span data-stu-id="897ae-114">Displays asterisks (\*) in place of text.</span></span> <span data-ttu-id="897ae-115">Solo se puede especificar en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="897ae-115">Can only be specified at design time.</span></span> |
| <span data-ttu-id="897ae-116">mayúsculas</span><span class="sxs-lookup"><span data-stu-id="897ae-116">uppercase</span></span> | <span data-ttu-id="897ae-117">Muestra el texto en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="897ae-117">Displays text as all uppercase.</span></span>                                                 |
| <span data-ttu-id="897ae-118">minúsculas</span><span class="sxs-lookup"><span data-stu-id="897ae-118">lowercase</span></span> | <span data-ttu-id="897ae-119">Muestra el texto en minúsculas.</span><span class="sxs-lookup"><span data-stu-id="897ae-119">Displays text as all lowercase.</span></span>                                                 |
| <span data-ttu-id="897ae-120">number</span><span class="sxs-lookup"><span data-stu-id="897ae-120">number</span></span>    | <span data-ttu-id="897ae-121">Solo muestra los números.</span><span class="sxs-lookup"><span data-stu-id="897ae-121">Only displays numbers.</span></span>                                                          |
| <span data-ttu-id="897ae-122">ocupa</span><span class="sxs-lookup"><span data-stu-id="897ae-122">multiline</span></span> | <span data-ttu-id="897ae-123">Muestra varias líneas de texto.</span><span class="sxs-lookup"><span data-stu-id="897ae-123">Displays multiple lines of text.</span></span> <span data-ttu-id="897ae-124">Solo se puede especificar en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="897ae-124">Can only be specified at design time.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="897ae-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="897ae-125">Remarks</span></span>

<span data-ttu-id="897ae-126">Este atributo solo se puede establecer en "Password" o "Multiline" en tiempo de diseño.</span><span class="sxs-lookup"><span data-stu-id="897ae-126">This attribute can only be set to "password" or "multiline" at design time.</span></span> <span data-ttu-id="897ae-127">Si se establece en "Multiline", no se puede cambiar el valor en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="897ae-127">If it is set to "multiline", the value cannot be changed at run time.</span></span>

## <a name="requirements"></a><span data-ttu-id="897ae-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="897ae-128">Requirements</span></span>



| <span data-ttu-id="897ae-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="897ae-129">Requirement</span></span> | <span data-ttu-id="897ae-130">Value</span><span class="sxs-lookup"><span data-stu-id="897ae-130">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="897ae-131">Versión</span><span class="sxs-lookup"><span data-stu-id="897ae-131">Version</span></span><br/> | <span data-ttu-id="897ae-132">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="897ae-132">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="897ae-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="897ae-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="897ae-134">**Elemento EDITBOX**</span><span class="sxs-lookup"><span data-stu-id="897ae-134">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> </dl>

 

 





