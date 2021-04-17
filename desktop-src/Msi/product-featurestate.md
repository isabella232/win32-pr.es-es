---
description: La propiedad FeatureState es el estado de instalación de la característica para la instancia de este producto. Esta propiedad llama a MsiQueryFeatureStateEx, con el ProductCode, UserSid y el contexto del objeto. El identificador de la característica se proporciona como un parámetro.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Product. FeatureState (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653537"
---
# <a name="productfeaturestate-method"></a><span data-ttu-id="98c5f-104">Product. FeatureState (método)</span><span class="sxs-lookup"><span data-stu-id="98c5f-104">Product.FeatureState method</span></span>

<span data-ttu-id="98c5f-105">La propiedad **FeatureState** es el estado de instalación de la característica para la instancia de este producto.</span><span class="sxs-lookup"><span data-stu-id="98c5f-105">The **FeatureState** property is the installation state of the feature for the instance of this product.</span></span>

<span data-ttu-id="98c5f-106">Esta propiedad llama a [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), con el *ProductCode*, *UserSid* y el *contexto* del objeto.</span><span class="sxs-lookup"><span data-stu-id="98c5f-106">This property calls [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), with the *ProductCode*, *UserSid* and *Context* of the object.</span></span> <span data-ttu-id="98c5f-107">El identificador de la característica se proporciona como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="98c5f-107">The feature Id is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c5f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98c5f-108">Syntax</span></span>


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a><span data-ttu-id="98c5f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98c5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c5f-110">*FeatureId*</span><span class="sxs-lookup"><span data-stu-id="98c5f-110">*FeatureId*</span></span> 
</dt> <dd>

<span data-ttu-id="98c5f-111">Identificador de característica que aparece en la columna característica de la [tabla de características](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="98c5f-111">Feature Id appearing in the Feature column of the [Feature Table](feature-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c5f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98c5f-112">Return value</span></span>

<span data-ttu-id="98c5f-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="98c5f-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98c5f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98c5f-114">Remarks</span></span>

<span data-ttu-id="98c5f-115">Si la llamada se realiza correctamente, la propiedad contiene el valor como **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="98c5f-115">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="98c5f-116">State</span><span class="sxs-lookup"><span data-stu-id="98c5f-116">State</span></span>                    | <span data-ttu-id="98c5f-117">Significado</span><span class="sxs-lookup"><span data-stu-id="98c5f-117">Meaning</span></span>                                      |
|--------------------------|----------------------------------------------|
| <span data-ttu-id="98c5f-118">INSTALLSTATE \_ anunciado</span><span class="sxs-lookup"><span data-stu-id="98c5f-118">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="98c5f-119">Esta característica se anuncia.</span><span class="sxs-lookup"><span data-stu-id="98c5f-119">This feature is advertised.</span></span>                  |
| <span data-ttu-id="98c5f-120">INSTALLSTATE \_ local</span><span class="sxs-lookup"><span data-stu-id="98c5f-120">INSTALLSTATE\_LOCAL</span></span>      | <span data-ttu-id="98c5f-121">La característica se instala localmente.</span><span class="sxs-lookup"><span data-stu-id="98c5f-121">The feature is installed locally.</span></span>            |
| <span data-ttu-id="98c5f-122">origen de INSTALLSTATE \_</span><span class="sxs-lookup"><span data-stu-id="98c5f-122">INSTALLSTATE\_SOURCE</span></span>     | <span data-ttu-id="98c5f-123">La característica se instala para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="98c5f-123">The feature is installed to run from source.</span></span> |



 

<span data-ttu-id="98c5f-124">Si se produce un error en la llamada, la propiedad contiene un código de error de [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span><span class="sxs-lookup"><span data-stu-id="98c5f-124">If the call fails, the property contains an error code from [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).</span></span>



| <span data-ttu-id="98c5f-125">Error</span><span class="sxs-lookup"><span data-stu-id="98c5f-125">Error</span></span>                     | <span data-ttu-id="98c5f-126">Significado</span><span class="sxs-lookup"><span data-stu-id="98c5f-126">Meaning</span></span>                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c5f-127">ERROR de \_ acceso \_ denegado</span><span class="sxs-lookup"><span data-stu-id="98c5f-127">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="98c5f-128">El proceso de llamada debe tener privilegios administrativos para obtener información de un producto instalado para un usuario que no sea el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="98c5f-128">The calling process must have administrative privileges to get information for a product installed for a user other than the current user.</span></span> |
| <span data-ttu-id="98c5f-129">ERROR \_ de \_ Configuración incorrecta</span><span class="sxs-lookup"><span data-stu-id="98c5f-129">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="98c5f-130">Los datos de configuración están dañados.</span><span class="sxs-lookup"><span data-stu-id="98c5f-130">The configuration data is corrupt.</span></span>                                                                                                         |
| <span data-ttu-id="98c5f-131">ERROR \_ de \_ parámetro no válido</span><span class="sxs-lookup"><span data-stu-id="98c5f-131">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="98c5f-132">Se pasó un parámetro no válido a la función.</span><span class="sxs-lookup"><span data-stu-id="98c5f-132">An invalid parameter was passed to the function.</span></span>                                                                                           |
| <span data-ttu-id="98c5f-133">ERROR \_ correcto</span><span class="sxs-lookup"><span data-stu-id="98c5f-133">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="98c5f-134">La función se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="98c5f-134">The function completed successfully.</span></span>                                                                                                       |
| <span data-ttu-id="98c5f-135">ERROR \_ de \_ característica desconocida</span><span class="sxs-lookup"><span data-stu-id="98c5f-135">ERROR\_UNKNOWN\_FEATURE</span></span>   | <span data-ttu-id="98c5f-136">El identificador de la característica no identifica una característica conocida.</span><span class="sxs-lookup"><span data-stu-id="98c5f-136">The feature ID does not identify a known feature.</span></span>                                                                                          |
| <span data-ttu-id="98c5f-137">ERROR \_ desconocido del \_ producto</span><span class="sxs-lookup"><span data-stu-id="98c5f-137">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="98c5f-138">El código de producto no identifica un producto conocido.</span><span class="sxs-lookup"><span data-stu-id="98c5f-138">The product code does not identify a known product.</span></span>                                                                                        |
| <span data-ttu-id="98c5f-139">ERROR en la \_ función error \_</span><span class="sxs-lookup"><span data-stu-id="98c5f-139">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="98c5f-140">Error interno inesperado.</span><span class="sxs-lookup"><span data-stu-id="98c5f-140">An unexpected internal failure.</span></span>                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="98c5f-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98c5f-141">Requirements</span></span>



| <span data-ttu-id="98c5f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c5f-142">Requirement</span></span> | <span data-ttu-id="98c5f-143">Value</span><span class="sxs-lookup"><span data-stu-id="98c5f-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c5f-144">Versión</span><span class="sxs-lookup"><span data-stu-id="98c5f-144">Version</span></span><br/> | <span data-ttu-id="98c5f-145">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="98c5f-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="98c5f-146">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="98c5f-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="98c5f-147">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="98c5f-147">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="98c5f-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98c5f-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="98c5f-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98c5f-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="98c5f-150">IID</span><span class="sxs-lookup"><span data-stu-id="98c5f-150">IID</span></span><br/>     | <span data-ttu-id="98c5f-151">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="98c5f-151">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="98c5f-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="98c5f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c5f-153">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="98c5f-153">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="98c5f-154">**MsiQueryFeatureStateEx**</span><span class="sxs-lookup"><span data-stu-id="98c5f-154">**MsiQueryFeatureStateEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[<span data-ttu-id="98c5f-155">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="98c5f-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




