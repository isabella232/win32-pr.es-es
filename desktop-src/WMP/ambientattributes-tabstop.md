---
title: AmbientAttributes. tabStop
description: El atributo tabStop especifica o recupera un valor que indica si el control está en el orden de tabulación. Para establecer el orden de tabulación, coloque el control en el script general antes o después de otras etiquetas de control.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- AmbientAttributes. tabStop Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700197"
---
# <a name="ambientattributestabstop"></a><span data-ttu-id="d5ffd-105">AmbientAttributes. tabStop</span><span class="sxs-lookup"><span data-stu-id="d5ffd-105">AmbientAttributes.tabStop</span></span>

<span data-ttu-id="d5ffd-106">El atributo **tabStop** especifica o recupera un valor que indica si el control está en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="d5ffd-106">The **tabStop** attribute specifies or retrieves a value indicating whether the control is in the tabbing order.</span></span> <span data-ttu-id="d5ffd-107">Para establecer el orden de tabulación, coloque el control en el script general antes o después de otras etiquetas de control.</span><span class="sxs-lookup"><span data-stu-id="d5ffd-107">You set the tabbing order by placing the control in the overall script before or after other control tags.</span></span>

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a><span data-ttu-id="d5ffd-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="d5ffd-108">Possible Values</span></span>

<span data-ttu-id="d5ffd-109">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="d5ffd-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="d5ffd-110">Value</span><span class="sxs-lookup"><span data-stu-id="d5ffd-110">Value</span></span> | <span data-ttu-id="d5ffd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d5ffd-111">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ffd-112">true</span><span class="sxs-lookup"><span data-stu-id="d5ffd-112">true</span></span>  | <span data-ttu-id="d5ffd-113">El control está en el orden de tabulación (el control tendrá una tabulación: requisito de accesibilidad).</span><span class="sxs-lookup"><span data-stu-id="d5ffd-113">Control is in the tabbing order (control will have a tab stop: accessibility requirement).</span></span> |
| <span data-ttu-id="d5ffd-114">false</span><span class="sxs-lookup"><span data-stu-id="d5ffd-114">false</span></span> | <span data-ttu-id="d5ffd-115">El control no está en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="d5ffd-115">Control is not in the tabbing order.</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="d5ffd-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5ffd-116">Remarks</span></span>

<span data-ttu-id="d5ffd-117">El atributo **tabStop** no es aplicable al elemento **Effects** .</span><span class="sxs-lookup"><span data-stu-id="d5ffd-117">The **tabStop** attribute is not applicable to the **EFFECTS** element.</span></span>

<span data-ttu-id="d5ffd-118">El valor predeterminado de este atributo es true para todos los elementos excepto **automenu** y **Text**, que tienen un valor predeterminado de false.</span><span class="sxs-lookup"><span data-stu-id="d5ffd-118">The default value for this attribute is true for all elements except **AUTOMENU** and **TEXT**, which have a default value of false.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ffd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5ffd-119">Requirements</span></span>



| <span data-ttu-id="d5ffd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5ffd-120">Requirement</span></span> | <span data-ttu-id="d5ffd-121">Value</span><span class="sxs-lookup"><span data-stu-id="d5ffd-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d5ffd-122">Versión</span><span class="sxs-lookup"><span data-stu-id="d5ffd-122">Version</span></span><br/> | <span data-ttu-id="d5ffd-123">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="d5ffd-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5ffd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5ffd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ffd-125">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="d5ffd-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





