---
description: La propiedad State devuelve el estado de instalación de esta instancia del producto.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Propiedad product. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653809"
---
# <a name="productstate-property"></a><span data-ttu-id="2c51b-103">Propiedad product. State</span><span class="sxs-lookup"><span data-stu-id="2c51b-103">Product.State property</span></span>

<span data-ttu-id="2c51b-104">La propiedad **State** devuelve el estado de instalación de esta instancia del producto.</span><span class="sxs-lookup"><span data-stu-id="2c51b-104">The **State** property returns the installation state of this instance of the product.</span></span>

<span data-ttu-id="2c51b-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2c51b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c51b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c51b-106">Syntax</span></span>


```JScript
propVal = Product.State
```



## <a name="property-value"></a><span data-ttu-id="2c51b-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2c51b-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="2c51b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c51b-108">Remarks</span></span>

<span data-ttu-id="2c51b-109">Esta propiedad devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2c51b-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="2c51b-110">Estado de la instalación</span><span class="sxs-lookup"><span data-stu-id="2c51b-110">Installation State</span></span>       | <span data-ttu-id="2c51b-111">Significado</span><span class="sxs-lookup"><span data-stu-id="2c51b-111">Meaning</span></span>                                |
|--------------------------|----------------------------------------|
| <span data-ttu-id="2c51b-112">INSTALLSTATE ( \_ valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2c51b-112">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="2c51b-113">Instancia de producto instalada localmente.</span><span class="sxs-lookup"><span data-stu-id="2c51b-113">Instance of product installed locally.</span></span> |
| <span data-ttu-id="2c51b-114">INSTALLSTATE \_ anunciado</span><span class="sxs-lookup"><span data-stu-id="2c51b-114">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="2c51b-115">Instancia de producto anunciada.</span><span class="sxs-lookup"><span data-stu-id="2c51b-115">Instance of product advertised.</span></span>        |
| <span data-ttu-id="2c51b-116">INSTALLSTATE \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="2c51b-116">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="2c51b-117">Instancia de producto desconocida.</span><span class="sxs-lookup"><span data-stu-id="2c51b-117">Instance of product unknown.</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="2c51b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c51b-118">Requirements</span></span>



| <span data-ttu-id="2c51b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c51b-119">Requirement</span></span> | <span data-ttu-id="2c51b-120">Value</span><span class="sxs-lookup"><span data-stu-id="2c51b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c51b-121">Versión</span><span class="sxs-lookup"><span data-stu-id="2c51b-121">Version</span></span><br/> | <span data-ttu-id="2c51b-122">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c51b-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2c51b-123">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2c51b-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2c51b-124">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2c51b-124">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="2c51b-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c51b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c51b-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c51b-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="2c51b-127">IID</span><span class="sxs-lookup"><span data-stu-id="2c51b-127">IID</span></span><br/>     | <span data-ttu-id="2c51b-128">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2c51b-128">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="2c51b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c51b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c51b-130">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="2c51b-130">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="2c51b-131">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="2c51b-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




