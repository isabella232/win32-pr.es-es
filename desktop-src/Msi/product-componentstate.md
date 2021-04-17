---
description: La propiedad ComponentState es el estado de instalación del componente para la instancia de este producto. Esta propiedad llama a MsiQueryComponentState, con ProductCode, UserSid y el contexto del objeto.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Product. ComponentState (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653789"
---
# <a name="productcomponentstate-method"></a><span data-ttu-id="ac37f-103">Product. ComponentState (método)</span><span class="sxs-lookup"><span data-stu-id="ac37f-103">Product.ComponentState method</span></span>

<span data-ttu-id="ac37f-104">La propiedad **ComponentState** es el estado de instalación del componente para la instancia de este producto.</span><span class="sxs-lookup"><span data-stu-id="ac37f-104">The **ComponentState** property is the installation state of the component for the instance of this product.</span></span>

<span data-ttu-id="ac37f-105">Esta propiedad llama a [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), con ProductCode, UserSid y el contexto del objeto.</span><span class="sxs-lookup"><span data-stu-id="ac37f-105">This property calls [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), with the ProductCode, UserSid, and Context of the object.</span></span> <span data-ttu-id="ac37f-106">El GUID del identificador de componente se proporciona como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="ac37f-106">The component Id GUID is provided as a parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac37f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac37f-107">Syntax</span></span>


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a><span data-ttu-id="ac37f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac37f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac37f-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="ac37f-109">*ID*</span></span> 
</dt> <dd>

<span data-ttu-id="ac37f-110">GUID del código de componente del componente tal y como se encuentra en la columna ComponentID de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ac37f-110">Component code GUID of the component as found in the ComponentID column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac37f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac37f-111">Return value</span></span>

<span data-ttu-id="ac37f-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ac37f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac37f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac37f-113">Remarks</span></span>

<span data-ttu-id="ac37f-114">Si la llamada se realiza correctamente, la propiedad contiene el valor como **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="ac37f-114">If the call succeeds, the property contains the value as a **DWORD**.</span></span>



| <span data-ttu-id="ac37f-115">State</span><span class="sxs-lookup"><span data-stu-id="ac37f-115">State</span></span>                | <span data-ttu-id="ac37f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="ac37f-116">Meaning</span></span>                                            |
|----------------------|----------------------------------------------------|
| <span data-ttu-id="ac37f-117">INSTALLSTATE \_ local</span><span class="sxs-lookup"><span data-stu-id="ac37f-117">INSTALLSTATE\_LOCAL</span></span>  | <span data-ttu-id="ac37f-118">El componente se instala localmente.</span><span class="sxs-lookup"><span data-stu-id="ac37f-118">The component is installed locally.</span></span>                |
| <span data-ttu-id="ac37f-119">origen de INSTALLSTATE \_</span><span class="sxs-lookup"><span data-stu-id="ac37f-119">INSTALLSTATE\_SOURCE</span></span> | <span data-ttu-id="ac37f-120">El componente se instala para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="ac37f-120">The component is installed to run from the source.</span></span> |



 

<span data-ttu-id="ac37f-121">Si se produce un error en la llamada, la propiedad contiene un código de error de [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span><span class="sxs-lookup"><span data-stu-id="ac37f-121">If the call fails, the property contains an error code from [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).</span></span>



| <span data-ttu-id="ac37f-122">Error</span><span class="sxs-lookup"><span data-stu-id="ac37f-122">Error</span></span>                     | <span data-ttu-id="ac37f-123">Significado</span><span class="sxs-lookup"><span data-stu-id="ac37f-123">Meaning</span></span>                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac37f-124">ERROR de \_ acceso \_ denegado</span><span class="sxs-lookup"><span data-stu-id="ac37f-124">ERROR\_ACCESS\_DENIED</span></span>     | <span data-ttu-id="ac37f-125">El proceso de llamada debe tener privilegios administrativos para obtener información de un usuario que no sea el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="ac37f-125">The calling process must have administrative privileges to get information for a user other than the current user.</span></span> |
| <span data-ttu-id="ac37f-126">ERROR \_ de \_ Configuración incorrecta</span><span class="sxs-lookup"><span data-stu-id="ac37f-126">ERROR\_BAD\_CONFIGURATION</span></span> | <span data-ttu-id="ac37f-127">Los datos de configuración están dañados.</span><span class="sxs-lookup"><span data-stu-id="ac37f-127">The configuration data is corrupt.</span></span>                                                                                 |
| <span data-ttu-id="ac37f-128">ERROR \_ de \_ parámetro no válido</span><span class="sxs-lookup"><span data-stu-id="ac37f-128">ERROR\_INVALID\_PARAMETER</span></span> | <span data-ttu-id="ac37f-129">Se pasó un parámetro no válido a la función.</span><span class="sxs-lookup"><span data-stu-id="ac37f-129">An invalid parameter was passed to the function.</span></span>                                                                   |
| <span data-ttu-id="ac37f-130">ERROR \_ correcto</span><span class="sxs-lookup"><span data-stu-id="ac37f-130">ERROR\_SUCCESS</span></span>            | <span data-ttu-id="ac37f-131">La función se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac37f-131">The function completed successfully.</span></span>                                                                               |
| <span data-ttu-id="ac37f-132">ERROR \_ de \_ componente desconocido</span><span class="sxs-lookup"><span data-stu-id="ac37f-132">ERROR\_UNKNOWN\_COMPONENT</span></span> | <span data-ttu-id="ac37f-133">El identificador de componente no identifica un componente conocido.</span><span class="sxs-lookup"><span data-stu-id="ac37f-133">The component ID does not identify a known component.</span></span>                                                              |
| <span data-ttu-id="ac37f-134">ERROR \_ desconocido del \_ producto</span><span class="sxs-lookup"><span data-stu-id="ac37f-134">ERROR\_UNKNOWN\_PRODUCT</span></span>   | <span data-ttu-id="ac37f-135">El código de producto no identifica un producto conocido.</span><span class="sxs-lookup"><span data-stu-id="ac37f-135">The product code does not identify a known product.</span></span>                                                                |
| <span data-ttu-id="ac37f-136">ERROR en la \_ función error \_</span><span class="sxs-lookup"><span data-stu-id="ac37f-136">ERROR\_FUNCTION\_FAILED</span></span>   | <span data-ttu-id="ac37f-137">Error interno inesperado.</span><span class="sxs-lookup"><span data-stu-id="ac37f-137">An unexpected internal failure.</span></span>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="ac37f-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac37f-138">Requirements</span></span>



| <span data-ttu-id="ac37f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac37f-139">Requirement</span></span> | <span data-ttu-id="ac37f-140">Value</span><span class="sxs-lookup"><span data-stu-id="ac37f-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac37f-141">Versión</span><span class="sxs-lookup"><span data-stu-id="ac37f-141">Version</span></span><br/> | <span data-ttu-id="ac37f-142">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ac37f-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ac37f-143">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ac37f-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ac37f-144">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ac37f-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="ac37f-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac37f-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="ac37f-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac37f-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="ac37f-147">IID</span><span class="sxs-lookup"><span data-stu-id="ac37f-147">IID</span></span><br/>     | <span data-ttu-id="ac37f-148">IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ac37f-148">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="ac37f-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac37f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac37f-150">**Manuales**</span><span class="sxs-lookup"><span data-stu-id="ac37f-150">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="ac37f-151">**MsiQueryComponentState**</span><span class="sxs-lookup"><span data-stu-id="ac37f-151">**MsiQueryComponentState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[<span data-ttu-id="ac37f-152">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="ac37f-152">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




