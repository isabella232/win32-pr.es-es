---
description: El método UseFeature del objeto instalador incrementa el recuento de uso de una característica determinada y devuelve el estado de la instalación de esa característica. Este método se debe usar para indicar que la intención de una aplicación es usar una característica.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Instalador. UseFeature (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653886"
---
# <a name="installerusefeature-method"></a><span data-ttu-id="0b645-104">Instalador. UseFeature (método)</span><span class="sxs-lookup"><span data-stu-id="0b645-104">Installer.UseFeature method</span></span>

<span data-ttu-id="0b645-105">El método **UseFeature** del objeto [**instalador**](installer-object.md) incrementa el recuento de uso de una característica determinada y devuelve el estado de la instalación de esa característica.</span><span class="sxs-lookup"><span data-stu-id="0b645-105">The **UseFeature** method of the [**Installer**](installer-object.md) object increments the usage count for a particular feature and returns the installation state for that feature.</span></span> <span data-ttu-id="0b645-106">Este método se debe usar para indicar que la intención de una aplicación es usar una característica.</span><span class="sxs-lookup"><span data-stu-id="0b645-106">This method should be used to indicate an application's intent to use a feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b645-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b645-107">Syntax</span></span>


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="0b645-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b645-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b645-109">*Producto*</span><span class="sxs-lookup"><span data-stu-id="0b645-109">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="0b645-110">Especifica el código de producto del producto.</span><span class="sxs-lookup"><span data-stu-id="0b645-110">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="0b645-111">*Característica*</span><span class="sxs-lookup"><span data-stu-id="0b645-111">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="0b645-112">Identifica la característica que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="0b645-112">Identifies the feature to be used.</span></span>

</dd> <dt>

<span data-ttu-id="0b645-113">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="0b645-113">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="0b645-114">Este parámetro debe ser *msiInstallModeNoDetection*.</span><span class="sxs-lookup"><span data-stu-id="0b645-114">This parameter must be *msiInstallModeNoDetection*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b645-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b645-115">Return value</span></span>

<span data-ttu-id="0b645-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0b645-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b645-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b645-117">Remarks</span></span>

<span data-ttu-id="0b645-118">El método **UseFeature** solo debe usarse en las características que se sabe que se van a publicar.</span><span class="sxs-lookup"><span data-stu-id="0b645-118">The **UseFeature** method should only be used on features known to be published.</span></span> <span data-ttu-id="0b645-119">La aplicación debe determinar el estado de la característica mediante una llamada a la propiedad [**FeatureState**](installer-featurestate.md) o a la propiedad [**características**](installer-features.md) , o a sus equivalentes de API.</span><span class="sxs-lookup"><span data-stu-id="0b645-119">The application should determine the status of the feature by calling either the [**FeatureState**](installer-featurestate.md) property or [**Features**](installer-features.md) property or their API equivalents.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b645-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b645-120">Requirements</span></span>



| <span data-ttu-id="0b645-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b645-121">Requirement</span></span> | <span data-ttu-id="0b645-122">Value</span><span class="sxs-lookup"><span data-stu-id="0b645-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b645-123">Versión</span><span class="sxs-lookup"><span data-stu-id="0b645-123">Version</span></span><br/> | <span data-ttu-id="0b645-124">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b645-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0b645-125">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0b645-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0b645-126">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0b645-126">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0b645-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b645-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="0b645-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b645-128"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0b645-129">IID</span><span class="sxs-lookup"><span data-stu-id="0b645-129">IID</span></span><br/>     | <span data-ttu-id="0b645-130">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0b645-130">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="0b645-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b645-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b645-132">**MsiUseFeatureEx**</span><span class="sxs-lookup"><span data-stu-id="0b645-132">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




