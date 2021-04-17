---
description: La interfaz IDxtKey establece propiedades en la transición de clave. Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición de la clave.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interfaz IDxtKey (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680302"
---
# <a name="idxtkey-interface"></a><span data-ttu-id="5061a-103">Interfaz IDxtKey</span><span class="sxs-lookup"><span data-stu-id="5061a-103">IDxtKey interface</span></span>

> [!Note]  
> <span data-ttu-id="5061a-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="5061a-104">\[Deprecated.</span></span> <span data-ttu-id="5061a-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5061a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5061a-106">La `IDxtKey` interfaz establece las propiedades de la transición de [clave](key-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="5061a-106">The `IDxtKey` interface sets properties on the [Key](key-transition.md) transition.</span></span>

<span data-ttu-id="5061a-107">Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición de la clave.</span><span class="sxs-lookup"><span data-stu-id="5061a-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Key transition.</span></span> <span data-ttu-id="5061a-108">Las aplicaciones DES no necesitan usar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="5061a-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="5061a-109">Para establecer las propiedades de una transición en DES, use la interfaz [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="5061a-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="5061a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5061a-110">Members</span></span>

<span data-ttu-id="5061a-111">La interfaz **IDxtKey** hereda de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="5061a-111">The **IDxtKey** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="5061a-112">**IDxtKey** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5061a-112">**IDxtKey** also has these types of members:</span></span>

-   [<span data-ttu-id="5061a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="5061a-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5061a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5061a-114">Methods</span></span>

<span data-ttu-id="5061a-115">La interfaz **IDxtKey** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5061a-115">The **IDxtKey** interface has these methods.</span></span>



| <span data-ttu-id="5061a-116">Método</span><span class="sxs-lookup"><span data-stu-id="5061a-116">Method</span></span>                                            | <span data-ttu-id="5061a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5061a-117">Description</span></span>                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="5061a-118">**obtener \_ matiz**</span><span class="sxs-lookup"><span data-stu-id="5061a-118">**get\_Hue**</span></span>](idxtkey-get-hue.md)               | <span data-ttu-id="5061a-119">Recupera el valor de matiz en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="5061a-119">Retrieves the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="5061a-120">**obtener \_ invertir**</span><span class="sxs-lookup"><span data-stu-id="5061a-120">**get\_Invert**</span></span>](idxtkey-get-invert.md)         | <span data-ttu-id="5061a-121">Recupera un valor booleano que indica si se invierte la operación de clave.</span><span class="sxs-lookup"><span data-stu-id="5061a-121">Retrieves a Boolean value indicating whether the key operation is inverted.</span></span><br/> |
| [<span data-ttu-id="5061a-122">**obtener \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="5061a-122">**get\_KeyType**</span></span>](idxtkey-get-keytype.md)       | <span data-ttu-id="5061a-123">Recupera el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="5061a-123">Retrieves the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="5061a-124">**obtención de \_ luminancia**</span><span class="sxs-lookup"><span data-stu-id="5061a-124">**get\_Luminance**</span></span>](idxtkey-get-luminance.md)   | <span data-ttu-id="5061a-125">Recupera el valor de luminancia en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="5061a-125">Retrieves the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="5061a-126">**obtener \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="5061a-126">**get\_RGB**</span></span>](idxtkey-get-rgb.md)               | <span data-ttu-id="5061a-127">Recupera el color RGB en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="5061a-127">Retrieves the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="5061a-128">**obtener \_ similitud**</span><span class="sxs-lookup"><span data-stu-id="5061a-128">**get\_Similarity**</span></span>](idxtkey-get-similarity.md) | <span data-ttu-id="5061a-129">Recupera el intervalo de datos de color que se vuelve transparente.</span><span class="sxs-lookup"><span data-stu-id="5061a-129">Retrieves the range of color data that becomes transparent.</span></span><br/>                 |
| [<span data-ttu-id="5061a-130">**poner \_ matiz**</span><span class="sxs-lookup"><span data-stu-id="5061a-130">**put\_Hue**</span></span>](idxtkey-put-hue.md)               | <span data-ttu-id="5061a-131">Especifica el valor de matiz en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="5061a-131">Specifies the hue value on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="5061a-132">**poner \_ invertir**</span><span class="sxs-lookup"><span data-stu-id="5061a-132">**put\_Invert**</span></span>](idxtkey-put-invert.md)         | <span data-ttu-id="5061a-133">Especifica si se invierte la operación de clave.</span><span class="sxs-lookup"><span data-stu-id="5061a-133">Specifies whether the key operation is inverted.</span></span><br/>                            |
| [<span data-ttu-id="5061a-134">**poner \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="5061a-134">**put\_KeyType**</span></span>](idxtkey-put-keytype.md)       | <span data-ttu-id="5061a-135">Especifica el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="5061a-135">Specifies the type of key.</span></span><br/>                                                  |
| [<span data-ttu-id="5061a-136">**poner \_ luminancia**</span><span class="sxs-lookup"><span data-stu-id="5061a-136">**put\_Luminance**</span></span>](idxtkey-put-luminance.md)   | <span data-ttu-id="5061a-137">Especifica el valor de luminancia en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="5061a-137">Specifies the luminance value on which to key.</span></span><br/>                              |
| [<span data-ttu-id="5061a-138">**colocar \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="5061a-138">**put\_RGB**</span></span>](idxtkey-put-rgb.md)               | <span data-ttu-id="5061a-139">Especifica el color RGB en el que se va a hacer la tecla.</span><span class="sxs-lookup"><span data-stu-id="5061a-139">Specifies the RGB color on which to key.</span></span><br/>                                    |
| [<span data-ttu-id="5061a-140">**similitud de put \_**</span><span class="sxs-lookup"><span data-stu-id="5061a-140">**put\_Similarity**</span></span>](idxtkey-put-similarity.md) | <span data-ttu-id="5061a-141">Especifica el intervalo de datos de color que se vuelve transparente.</span><span class="sxs-lookup"><span data-stu-id="5061a-141">Specifies the range of color data that becomes transparent.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="5061a-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5061a-142">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5061a-143">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="5061a-143">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5061a-144">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5061a-144">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5061a-145">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5061a-145">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5061a-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5061a-146">Requirements</span></span>



| <span data-ttu-id="5061a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="5061a-147">Requirement</span></span> | <span data-ttu-id="5061a-148">Value</span><span class="sxs-lookup"><span data-stu-id="5061a-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5061a-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5061a-149">Header</span></span><br/>  | <dl> <span data-ttu-id="5061a-150"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="5061a-150"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5061a-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5061a-151">Library</span></span><br/> | <dl> <span data-ttu-id="5061a-152"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5061a-152"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




