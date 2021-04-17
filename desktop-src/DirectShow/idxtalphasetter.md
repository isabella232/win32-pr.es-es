---
description: La interfaz IDxtAlphaSetter establece propiedades en el efecto del establecedor alfa. Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa el efecto del establecedor alfa.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interfaz IDxtAlphaSetter (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680567"
---
# <a name="idxtalphasetter-interface"></a><span data-ttu-id="afb33-103">Interfaz IDxtAlphaSetter</span><span class="sxs-lookup"><span data-stu-id="afb33-103">IDxtAlphaSetter interface</span></span>

> [!Note]  
> <span data-ttu-id="afb33-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="afb33-104">\[Deprecated.</span></span> <span data-ttu-id="afb33-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="afb33-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="afb33-106">La `IDxtAlphaSetter` interfaz establece las propiedades en el efecto del [establecedor alfa](alpha-setter-effect.md) .</span><span class="sxs-lookup"><span data-stu-id="afb33-106">The `IDxtAlphaSetter` interface sets properties on the [Alpha Setter](alpha-setter-effect.md) effect.</span></span>

<span data-ttu-id="afb33-107">Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa el efecto del establecedor alfa.</span><span class="sxs-lookup"><span data-stu-id="afb33-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Alpha Setter effect.</span></span> <span data-ttu-id="afb33-108">Las aplicaciones DES no tienen que usar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="afb33-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="afb33-109">Para establecer las propiedades de una transición en DES, use la interfaz [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="afb33-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="afb33-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="afb33-110">Members</span></span>

<span data-ttu-id="afb33-111">La interfaz **IDxtAlphaSetter** hereda de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="afb33-111">The **IDxtAlphaSetter** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="afb33-112">**IDxtAlphaSetter** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="afb33-112">**IDxtAlphaSetter** also has these types of members:</span></span>

-   [<span data-ttu-id="afb33-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="afb33-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="afb33-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="afb33-114">Methods</span></span>

<span data-ttu-id="afb33-115">La interfaz **IDxtAlphaSetter** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="afb33-115">The **IDxtAlphaSetter** interface has these methods.</span></span>



| <span data-ttu-id="afb33-116">Método</span><span class="sxs-lookup"><span data-stu-id="afb33-116">Method</span></span>                                                  | <span data-ttu-id="afb33-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="afb33-117">Description</span></span>                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="afb33-118">**obtener \_ alfa**</span><span class="sxs-lookup"><span data-stu-id="afb33-118">**get\_Alpha**</span></span>](idxtalphasetter-get-alpha.md)         | <span data-ttu-id="afb33-119">Recupera el valor alfa de toda la imagen.</span><span class="sxs-lookup"><span data-stu-id="afb33-119">Retrieves the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="afb33-120">**obtener \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="afb33-120">**get\_AlphaRamp**</span></span>](idxtalphasetter-get-alpharamp.md) | <span data-ttu-id="afb33-121">Recupera la propiedad de rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="afb33-121">Retrieves the alpha ramp property.</span></span><br/>              |
| [<span data-ttu-id="afb33-122">**poner \_ alfa**</span><span class="sxs-lookup"><span data-stu-id="afb33-122">**put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)         | <span data-ttu-id="afb33-123">Especifica el valor alfa de la imagen completa.</span><span class="sxs-lookup"><span data-stu-id="afb33-123">Specifies the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="afb33-124">**Put \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="afb33-124">**put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md) | <span data-ttu-id="afb33-125">Especifica la propiedad de rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="afb33-125">Specifies the alpha ramp property.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="afb33-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afb33-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="afb33-127">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="afb33-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="afb33-128">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="afb33-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="afb33-129">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="afb33-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="afb33-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afb33-130">Requirements</span></span>



| <span data-ttu-id="afb33-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="afb33-131">Requirement</span></span> | <span data-ttu-id="afb33-132">Value</span><span class="sxs-lookup"><span data-stu-id="afb33-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afb33-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afb33-133">Header</span></span><br/>  | <dl> <span data-ttu-id="afb33-134"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="afb33-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="afb33-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="afb33-135">Library</span></span><br/> | <dl> <span data-ttu-id="afb33-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afb33-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




