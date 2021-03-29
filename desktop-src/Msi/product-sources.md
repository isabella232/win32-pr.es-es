---
description: La propiedad sources enumera todos los orígenes de la instancia del producto.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Propiedad product. sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680663"
---
# <a name="productsources-property"></a><span data-ttu-id="ef2c9-103">Propiedad product. sources</span><span class="sxs-lookup"><span data-stu-id="ef2c9-103">Product.Sources property</span></span>

<span data-ttu-id="ef2c9-104">La propiedad **sources** enumera todos los orígenes de la instancia del producto.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-104">The **Sources** property enumerates all the sources for the product instance.</span></span> <span data-ttu-id="ef2c9-105">Esta propiedad llama a [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) y devuelve la matriz de cadenas y acepta el tipo de origen como argumento.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-105">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns the array of strings, and accepts the source type as argument.</span></span> <span data-ttu-id="ef2c9-106">El tipo de origen puede ser MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-106">The source type can be MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

<span data-ttu-id="ef2c9-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef2c9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef2c9-108">Syntax</span></span>


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a><span data-ttu-id="ef2c9-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ef2c9-109">Property value</span></span>

<span data-ttu-id="ef2c9-110">Tipo de origen que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-110">The type of source to enumerate.</span></span> <span data-ttu-id="ef2c9-111">El valor puede ser *msiInstallSourceTypeNetwork* (1) o *msiInstallSourceTypeURL* (2).</span><span class="sxs-lookup"><span data-stu-id="ef2c9-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef2c9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef2c9-112">Requirements</span></span>



| <span data-ttu-id="ef2c9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef2c9-113">Requirement</span></span> | <span data-ttu-id="ef2c9-114">Value</span><span class="sxs-lookup"><span data-stu-id="ef2c9-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef2c9-115">Versión</span><span class="sxs-lookup"><span data-stu-id="ef2c9-115">Version</span></span><br/> | <span data-ttu-id="ef2c9-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ef2c9-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ef2c9-118">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ef2c9-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="ef2c9-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef2c9-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="ef2c9-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef2c9-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="ef2c9-121">IID</span><span class="sxs-lookup"><span data-stu-id="ef2c9-121">IID</span></span><br/>     | <span data-ttu-id="ef2c9-122">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ef2c9-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="ef2c9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef2c9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef2c9-124">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="ef2c9-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="ef2c9-125">**MsiSourceListEnumSources**</span><span class="sxs-lookup"><span data-stu-id="ef2c9-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="ef2c9-126">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="ef2c9-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




