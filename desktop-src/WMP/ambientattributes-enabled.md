---
title: AmbientAttributes. Enabled
description: El atributo Enabled especifica o recupera un valor que indica si el control está habilitado o deshabilitado.
ms.assetid: cf96ab7c-8acd-42b6-b7ca-d084a89c97e2
keywords:
- AmbientAttributes. Enabled Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.enabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c34d24e86118a1cca0939d535b6da6e86c2df34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698636"
---
# <a name="ambientattributesenabled"></a><span data-ttu-id="056df-104">AmbientAttributes. Enabled</span><span class="sxs-lookup"><span data-stu-id="056df-104">AmbientAttributes.enabled</span></span>

<span data-ttu-id="056df-105">El atributo **Enabled** especifica o recupera un valor que indica si el control está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="056df-105">The **enabled** attribute specifies or retrieves a value indicating whether the control is enabled or disabled.</span></span>

``` syntax
        elementID.enabled
```

## <a name="possible-values"></a><span data-ttu-id="056df-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="056df-106">Possible Values</span></span>

<span data-ttu-id="056df-107">Este atributo es un **valor booleano** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="056df-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="056df-108">Value</span><span class="sxs-lookup"><span data-stu-id="056df-108">Value</span></span> | <span data-ttu-id="056df-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="056df-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="056df-110">true</span><span class="sxs-lookup"><span data-stu-id="056df-110">true</span></span>  | <span data-ttu-id="056df-111">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="056df-111">Default.</span></span> <span data-ttu-id="056df-112">Control habilitado.</span><span class="sxs-lookup"><span data-stu-id="056df-112">Control enabled.</span></span> |
| <span data-ttu-id="056df-113">false</span><span class="sxs-lookup"><span data-stu-id="056df-113">false</span></span> | <span data-ttu-id="056df-114">Control deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="056df-114">Control disabled.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="056df-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="056df-115">Remarks</span></span>

<span data-ttu-id="056df-116">Si el control está habilitado, puede tener una tabulación y recibirá todos los eventos de ambiente.</span><span class="sxs-lookup"><span data-stu-id="056df-116">If the control is enabled, it can have a tab stop, and will receive all ambient events.</span></span> <span data-ttu-id="056df-117">Cuando está deshabilitado, el control no tiene una tabulación y no recibe ningún evento de mouse o teclado ambiente que se desencadene.</span><span class="sxs-lookup"><span data-stu-id="056df-117">When disabled, the control does not have a tab stop, and does not receive any ambient mouse or keyboard events fired to it.</span></span> <span data-ttu-id="056df-118">(Sin embargo, seguirá recibiendo todos los demás eventos de ambiente que se le hayan desencadenado).</span><span class="sxs-lookup"><span data-stu-id="056df-118">(However, it will continue to receive all other ambient events fired to it.)</span></span>

<span data-ttu-id="056df-119">Este atributo no se admite para el elemento de la **subvista** .</span><span class="sxs-lookup"><span data-stu-id="056df-119">This attribute is not supported for the **SUBVIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="056df-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="056df-120">Requirements</span></span>



| <span data-ttu-id="056df-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="056df-121">Requirement</span></span> | <span data-ttu-id="056df-122">Value</span><span class="sxs-lookup"><span data-stu-id="056df-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="056df-123">Versión</span><span class="sxs-lookup"><span data-stu-id="056df-123">Version</span></span><br/> | <span data-ttu-id="056df-124">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="056df-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="056df-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="056df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="056df-126">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="056df-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





