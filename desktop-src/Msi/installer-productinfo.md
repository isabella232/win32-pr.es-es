---
description: La propiedad ProductInfo es una propiedad de solo lectura que devuelve el valor del atributo especificado para un producto instalado o publicado.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Propiedad Installer. ProductInfo (Oemupgex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653954"
---
# <a name="installerproductinfo-property"></a><span data-ttu-id="bf89c-103">Installer. ProductInfo (propiedad)</span><span class="sxs-lookup"><span data-stu-id="bf89c-103">Installer.ProductInfo property</span></span>

<span data-ttu-id="bf89c-104">La propiedad **ProductInfo** es una propiedad de solo lectura que devuelve el valor del atributo especificado para un producto instalado o publicado.</span><span class="sxs-lookup"><span data-stu-id="bf89c-104">The **ProductInfo** property is a read-only property that returns the value of the specified attribute for an installed or published product.</span></span>

<span data-ttu-id="bf89c-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bf89c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf89c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf89c-106">Syntax</span></span>


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a><span data-ttu-id="bf89c-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bf89c-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="bf89c-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf89c-108">Remarks</span></span>

<span data-ttu-id="bf89c-109">La propiedad **ProductInfo** ("LocalPackage") no devuelve necesariamente una ruta de acceso al paquete almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="bf89c-109">The **ProductInfo** property ("LocalPackage") does not necessarily return a path to the cached package.</span></span> <span data-ttu-id="bf89c-110">No se deben invocar las instalaciones del modo de mantenimiento desde LocalPackage.</span><span class="sxs-lookup"><span data-stu-id="bf89c-110">Maintenance mode installations should be not be invoked from the LocalPackage.</span></span> <span data-ttu-id="bf89c-111">El paquete en caché solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="bf89c-111">The cached package is for internal uses only.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf89c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf89c-112">Requirements</span></span>



| <span data-ttu-id="bf89c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf89c-113">Requirement</span></span> | <span data-ttu-id="bf89c-114">Value</span><span class="sxs-lookup"><span data-stu-id="bf89c-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf89c-115">Versión</span><span class="sxs-lookup"><span data-stu-id="bf89c-115">Version</span></span><br/> | <span data-ttu-id="bf89c-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf89c-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bf89c-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bf89c-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bf89c-118">Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bf89c-118">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="bf89c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf89c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bf89c-120"><dt>Oemupgex. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf89c-120"><dt>Oemupgex.h</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="bf89c-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf89c-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="bf89c-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf89c-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="bf89c-123">IID</span><span class="sxs-lookup"><span data-stu-id="bf89c-123">IID</span></span><br/>     | <span data-ttu-id="bf89c-124">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bf89c-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="bf89c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf89c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf89c-126">**MsiGetProductInfo**</span><span class="sxs-lookup"><span data-stu-id="bf89c-126">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="bf89c-127">**MsiGetUserInfo**</span><span class="sxs-lookup"><span data-stu-id="bf89c-127">**MsiGetUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[<span data-ttu-id="bf89c-128">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="bf89c-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




