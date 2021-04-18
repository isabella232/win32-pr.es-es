---
title: Interfaz IWMPError (VB y C) (WMP. h)
description: Proporciona propiedades y métodos para tener acceso a una colección de interfaces IWMPErrorItem para recuperar información de error. La interfaz IWMPError expone las siguientes propiedades.
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- IWMPError (VB y C) interfaz de Windows Media Player
- IWMPError (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPError (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289a39093c38e7a4b0cc43cb8f318e321ae8ef53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690422"
---
# <a name="iwmperror-vb-and-c-interface"></a><span data-ttu-id="6807e-105">Interfaz IWMPError (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="6807e-105">IWMPError (VB and C#) interface</span></span>

<span data-ttu-id="6807e-106">Proporciona propiedades y métodos para tener acceso a una colección de interfaces **IWMPErrorItem** para recuperar información de error.</span><span class="sxs-lookup"><span data-stu-id="6807e-106">Provides properties and methods for accessing a collection of **IWMPErrorItem** interfaces for retrieving error information.</span></span>

<span data-ttu-id="6807e-107">La interfaz **IWMPError** expone las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="6807e-107">The **IWMPError** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="6807e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6807e-108">Members</span></span>

<span data-ttu-id="6807e-109">La interfaz **IWMPError (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6807e-109">The **IWMPError (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="6807e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6807e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="6807e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6807e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6807e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6807e-112">Methods</span></span>

<span data-ttu-id="6807e-113">La interfaz **IWMPError (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6807e-113">The **IWMPError (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="6807e-114">Método</span><span class="sxs-lookup"><span data-stu-id="6807e-114">Method</span></span>                                                                         | <span data-ttu-id="6807e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6807e-115">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6807e-116">**clearErrorQueue**</span><span class="sxs-lookup"><span data-stu-id="6807e-116">**clearErrorQueue**</span></span>](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | <span data-ttu-id="6807e-117">Borra los errores de la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="6807e-117">Clears the errors from the error queue.</span></span><br/>                                                                                            |
| [<span data-ttu-id="6807e-118">**WebHelp**</span><span class="sxs-lookup"><span data-stu-id="6807e-118">**webHelp**</span></span>](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | <span data-ttu-id="6807e-119">Inicia la página de ayuda Web de Microsoft Windows Media Player para mostrar información adicional sobre el primer error en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="6807e-119">Launches the Microsoft Windows Media Player Web Help page to display further information about the first error in the error queue.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6807e-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6807e-120">Properties</span></span>

<span data-ttu-id="6807e-121">La interfaz **IWMPError (VB y C#)** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6807e-121">The **IWMPError (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="6807e-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6807e-122">Property</span></span>                                                                        | <span data-ttu-id="6807e-123">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="6807e-123">Access type</span></span>           | <span data-ttu-id="6807e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6807e-124">Description</span></span>                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6807e-125">**errorCount**</span><span class="sxs-lookup"><span data-stu-id="6807e-125">**errorCount**</span></span>](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | <span data-ttu-id="6807e-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6807e-126">Read-only</span></span><br/>  | <span data-ttu-id="6807e-127">Obtiene el número de errores en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="6807e-127">Gets the number of errors in the error queue.</span></span><br/>                                                                            |
| [<span data-ttu-id="6807e-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6807e-128">**Item**</span></span>](iwmperror-item--vb-and-c.md)<br/>                             | <span data-ttu-id="6807e-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6807e-129">Read/write</span></span><br/> | <span data-ttu-id="6807e-130">Obtiene una interfaz **IWMPErrorItem** en el índice especificado de la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="6807e-130">Gets an **IWMPErrorItem** interface at the specified index in the error queue.</span></span> <span data-ttu-id="6807e-131">En C#, este es el método **Get \_ Item** .</span><span class="sxs-lookup"><span data-stu-id="6807e-131">In C#, this is the **get\_Item** method.</span></span><br/> |



 

<span data-ttu-id="6807e-132">Obtenga una interfaz **IWMPError** con la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="6807e-132">Get an **IWMPError** interface by using the following property.</span></span>



| <span data-ttu-id="6807e-133">Object</span><span class="sxs-lookup"><span data-stu-id="6807e-133">Object</span></span>                                                                   | <span data-ttu-id="6807e-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6807e-134">Property</span></span>                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="6807e-135">Objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="6807e-135">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="6807e-136">**Error**</span><span class="sxs-lookup"><span data-stu-id="6807e-136">**Error**</span></span>](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="6807e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6807e-137">Requirements</span></span>



| <span data-ttu-id="6807e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="6807e-138">Requirement</span></span> | <span data-ttu-id="6807e-139">Value</span><span class="sxs-lookup"><span data-stu-id="6807e-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6807e-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6807e-140">Header</span></span><br/> | <dl> <span data-ttu-id="6807e-141"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="6807e-141"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6807e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="6807e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6807e-143">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="6807e-143">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="6807e-144">**Interfaz IWMPErrorItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6807e-144">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





