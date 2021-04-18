---
description: La propiedad Format del objeto ConfigurableItem devuelve el valor de la columna Format de la tabla ModuleConfiguration.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Propiedad ConfigurableItem. Format (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653625"
---
# <a name="configurableitemformat-property"></a><span data-ttu-id="88a49-103">ConfigurableItem. Format (propiedad)</span><span class="sxs-lookup"><span data-stu-id="88a49-103">ConfigurableItem.Format property</span></span>

<span data-ttu-id="88a49-104">La propiedad **Format** del objeto [**ConfigurableItem**](configurableitem-object.md) devuelve el valor de la columna Format de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="88a49-104">The **Format** property of the [**ConfigurableItem**](configurableitem-object.md) object returns the value from the Format column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="88a49-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="88a49-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="88a49-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88a49-106">Syntax</span></span>


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a><span data-ttu-id="88a49-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="88a49-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="88a49-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88a49-108">Remarks</span></span>

<span data-ttu-id="88a49-109">Esta propiedad solo puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="88a49-109">This property can only have the following values.</span></span>



| <span data-ttu-id="88a49-110">Constante</span><span class="sxs-lookup"><span data-stu-id="88a49-110">Constant</span></span>                        | <span data-ttu-id="88a49-111">Value</span><span class="sxs-lookup"><span data-stu-id="88a49-111">Value</span></span> |
|---------------------------------|-------|
| <span data-ttu-id="88a49-112">**msmConfigurableItemText**</span><span class="sxs-lookup"><span data-stu-id="88a49-112">**msmConfigurableItemText**</span></span>     | <span data-ttu-id="88a49-113">0</span><span class="sxs-lookup"><span data-stu-id="88a49-113">0</span></span>     |
| <span data-ttu-id="88a49-114">**msmConfigurableItemKey**</span><span class="sxs-lookup"><span data-stu-id="88a49-114">**msmConfigurableItemKey**</span></span>      | <span data-ttu-id="88a49-115">1</span><span class="sxs-lookup"><span data-stu-id="88a49-115">1</span></span>     |
| <span data-ttu-id="88a49-116">**msmConfigurableItemInteger**</span><span class="sxs-lookup"><span data-stu-id="88a49-116">**msmConfigurableItemInteger**</span></span>  | <span data-ttu-id="88a49-117">2</span><span class="sxs-lookup"><span data-stu-id="88a49-117">2</span></span>     |
| <span data-ttu-id="88a49-118">**msmConfigurableItemBitfield**</span><span class="sxs-lookup"><span data-stu-id="88a49-118">**msmConfigurableItemBitfield**</span></span> | <span data-ttu-id="88a49-119">3</span><span class="sxs-lookup"><span data-stu-id="88a49-119">3</span></span>     |



 

### <a name="c"></a><span data-ttu-id="88a49-120">C++</span><span class="sxs-lookup"><span data-stu-id="88a49-120">C++</span></span>

<span data-ttu-id="88a49-121">Consulte [**Get \_ Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.</span><span class="sxs-lookup"><span data-stu-id="88a49-121">See [**get\_Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="88a49-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88a49-122">Requirements</span></span>



| <span data-ttu-id="88a49-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="88a49-123">Requirement</span></span> | <span data-ttu-id="88a49-124">Value</span><span class="sxs-lookup"><span data-stu-id="88a49-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88a49-125">Versión</span><span class="sxs-lookup"><span data-stu-id="88a49-125">Version</span></span><br/> | <span data-ttu-id="88a49-126">Mergemod.dll 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="88a49-126">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="88a49-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88a49-127">Header</span></span><br/>  | <dl> <span data-ttu-id="88a49-128"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="88a49-128"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="88a49-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88a49-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="88a49-130"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88a49-130"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




