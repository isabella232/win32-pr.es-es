---
description: La propiedad ProductState es una propiedad de solo lectura que devuelve la información de estado de instalación de un producto.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Instalador. ProductState (método de propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653713"
---
# <a name="installerproductstate-property-method"></a><span data-ttu-id="e6f28-103">Instalador. ProductState (método de propiedad)</span><span class="sxs-lookup"><span data-stu-id="e6f28-103">Installer.ProductState Property method</span></span>

<span data-ttu-id="e6f28-104">La **propiedad ProductState** es una propiedad de solo lectura que devuelve la información de estado de instalación de un producto.</span><span class="sxs-lookup"><span data-stu-id="e6f28-104">The **ProductState property** is a read-only property that returns the install state information for a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f28-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6f28-105">Syntax</span></span>


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="e6f28-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6f28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6f28-107">*Producto*</span><span class="sxs-lookup"><span data-stu-id="e6f28-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="e6f28-108">Especifica el código de producto del producto.</span><span class="sxs-lookup"><span data-stu-id="e6f28-108">Specifies the product code of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6f28-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6f28-109">Return value</span></span>

<span data-ttu-id="e6f28-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e6f28-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6f28-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6f28-111">Remarks</span></span>

<span data-ttu-id="e6f28-112">Devuelve uno de los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e6f28-112">Returns one of the values shown in the following table.</span></span>



| <span data-ttu-id="e6f28-113">Estado de instalación</span><span class="sxs-lookup"><span data-stu-id="e6f28-113">Installation state</span></span>        | <span data-ttu-id="e6f28-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6f28-114">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="e6f28-115">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="e6f28-115">msiInstallStateAbsent</span></span>     | <span data-ttu-id="e6f28-116">El producto se instala para un usuario diferente.</span><span class="sxs-lookup"><span data-stu-id="e6f28-116">The product is installed for a different user.</span></span>   |
| <span data-ttu-id="e6f28-117">msiInstallStateDefault</span><span class="sxs-lookup"><span data-stu-id="e6f28-117">msiInstallStateDefault</span></span>    | <span data-ttu-id="e6f28-118">El producto está instalado para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="e6f28-118">The product is installed for the current user.</span></span>   |
| <span data-ttu-id="e6f28-119">msiInstallStateAdvertised</span><span class="sxs-lookup"><span data-stu-id="e6f28-119">msiInstallStateAdvertised</span></span> | <span data-ttu-id="e6f28-120">El producto se anuncia pero no se instala.</span><span class="sxs-lookup"><span data-stu-id="e6f28-120">The product is advertised but not installed.</span></span>     |
| <span data-ttu-id="e6f28-121">msiInstallStateInvalidArg</span><span class="sxs-lookup"><span data-stu-id="e6f28-121">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="e6f28-122">Se pasó un parámetro no válido a la función.</span><span class="sxs-lookup"><span data-stu-id="e6f28-122">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="e6f28-123">msiInstallStateUnknown</span><span class="sxs-lookup"><span data-stu-id="e6f28-123">msiInstallStateUnknown</span></span>    | <span data-ttu-id="e6f28-124">El producto no se anuncia ni se instala.</span><span class="sxs-lookup"><span data-stu-id="e6f28-124">The product is neither advertised nor installed.</span></span> |
| <span data-ttu-id="e6f28-125">msiInstallStateBadConfig</span><span class="sxs-lookup"><span data-stu-id="e6f28-125">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="e6f28-126">Los datos de configuración están dañados.</span><span class="sxs-lookup"><span data-stu-id="e6f28-126">The configuration data is corrupt.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="e6f28-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6f28-127">Requirements</span></span>



| <span data-ttu-id="e6f28-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6f28-128">Requirement</span></span> | <span data-ttu-id="e6f28-129">Value</span><span class="sxs-lookup"><span data-stu-id="e6f28-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f28-130">Versión</span><span class="sxs-lookup"><span data-stu-id="e6f28-130">Version</span></span><br/> | <span data-ttu-id="e6f28-131">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e6f28-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e6f28-132">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6f28-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e6f28-133">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e6f28-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e6f28-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e6f28-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="e6f28-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6f28-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e6f28-136">IID</span><span class="sxs-lookup"><span data-stu-id="e6f28-136">IID</span></span><br/>     | <span data-ttu-id="e6f28-137">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e6f28-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e6f28-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6f28-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6f28-139">**MsiQueryProductState**</span><span class="sxs-lookup"><span data-stu-id="e6f28-139">**MsiQueryProductState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




