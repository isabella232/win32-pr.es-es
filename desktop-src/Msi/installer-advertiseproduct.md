---
description: El método AdvertiseProduct del objeto de instalador anuncia un paquete de instalación.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: 'Installer:: AdvertiseProduct (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653643"
---
# <a name="installeradvertiseproduct-method"></a><span data-ttu-id="e84bf-103">Installer:: AdvertiseProduct (método)</span><span class="sxs-lookup"><span data-stu-id="e84bf-103">Installer::AdvertiseProduct method</span></span>

<span data-ttu-id="e84bf-104">El método **AdvertiseProduct** del objeto de [**instalador**](installer-object.md) anuncia un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="e84bf-104">The **AdvertiseProduct** method of the [**Installer**](installer-object.md) object advertises an installation package.</span></span>

## <a name="syntax"></a><span data-ttu-id="e84bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e84bf-105">Syntax</span></span>


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="e84bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e84bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e84bf-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="e84bf-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="e84bf-108">Ruta de acceso completa al paquete de Windows Installer (. msi) que se va a anunciar.</span><span class="sxs-lookup"><span data-stu-id="e84bf-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="e84bf-109">*contextoo*</span><span class="sxs-lookup"><span data-stu-id="e84bf-109">*context*</span></span> 
</dt> <dd>

<span data-ttu-id="e84bf-110">Contexto del anuncio.</span><span class="sxs-lookup"><span data-stu-id="e84bf-110">The context of the advertisement.</span></span> <span data-ttu-id="e84bf-111">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e84bf-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e84bf-112">Valor</span><span class="sxs-lookup"><span data-stu-id="e84bf-112">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="e84bf-113">Significado</span><span class="sxs-lookup"><span data-stu-id="e84bf-113">Meaning</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <span data-ttu-id="e84bf-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e84bf-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e84bf-115">Anuncia la aplicación para una instalación en el [contexto de instalación](installation-context.md)por máquina.</span><span class="sxs-lookup"><span data-stu-id="e84bf-115">Advertises the application for an instalation in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="e84bf-116">Esto hace que el paquete esté disponible para que lo instalen todos los usuarios del equipo.</span><span class="sxs-lookup"><span data-stu-id="e84bf-116">This makes the package available for installation by all users of the computer.</span></span><br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <span data-ttu-id="e84bf-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e84bf-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="e84bf-118">Anuncia la aplicación para una instalación en el [contexto de instalación](installation-context.md)por usuario.</span><span class="sxs-lookup"><span data-stu-id="e84bf-118">Advertises the application for an installation in the per-user [installation context](installation-context.md).</span></span><br/>                                                                                   |



 

</dd> <dt>

<span data-ttu-id="e84bf-119">*transforma*</span><span class="sxs-lookup"><span data-stu-id="e84bf-119">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="e84bf-120">Lista de transformaciones que se van a aplicar al producto.</span><span class="sxs-lookup"><span data-stu-id="e84bf-120">The list of transforms to apply to the product.</span></span> <span data-ttu-id="e84bf-121">Las transformaciones en la lista están delimitadas por signos de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="e84bf-121">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="e84bf-122">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="e84bf-122">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="e84bf-123">*language*</span><span class="sxs-lookup"><span data-stu-id="e84bf-123">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="e84bf-124">Idioma del paquete de instalación que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="e84bf-124">The language of the installation package to use.</span></span> <span data-ttu-id="e84bf-125">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="e84bf-125">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="e84bf-126">*options*</span><span class="sxs-lookup"><span data-stu-id="e84bf-126">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="e84bf-127">Opciones de anuncio.</span><span class="sxs-lookup"><span data-stu-id="e84bf-127">The advertisement options.</span></span> <span data-ttu-id="e84bf-128">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="e84bf-128">This parameter is optional.</span></span> <span data-ttu-id="e84bf-129">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e84bf-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e84bf-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e84bf-130">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="e84bf-131">Significado</span><span class="sxs-lookup"><span data-stu-id="e84bf-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="e84bf-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e84bf-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="e84bf-133">Anuncio estándar</span><span class="sxs-lookup"><span data-stu-id="e84bf-133">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="e84bf-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e84bf-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="e84bf-135">Anuncia una nueva instancia del producto.</span><span class="sxs-lookup"><span data-stu-id="e84bf-135">Advertises a new instance of the product.</span></span> <span data-ttu-id="e84bf-136">Requiere que la primera transformación de la lista de transformación del parámetro *transformaciones* sea la transformación de instancia que cambia el código de producto.</span><span class="sxs-lookup"><span data-stu-id="e84bf-136">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="e84bf-137">Para obtener más información, consulte [instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="e84bf-137">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e84bf-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e84bf-138">Return value</span></span>

<span data-ttu-id="e84bf-139">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e84bf-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e84bf-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e84bf-140">Remarks</span></span>

<span data-ttu-id="e84bf-141">El método **AdvertiseProduct** usa la función [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .</span><span class="sxs-lookup"><span data-stu-id="e84bf-141">The **AdvertiseProduct** method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="e84bf-142">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e84bf-142">Examples</span></span>

<span data-ttu-id="e84bf-143">En el siguiente ejemplo se muestra el uso del método **AdvertiseProduct** .</span><span class="sxs-lookup"><span data-stu-id="e84bf-143">The following example demonstrates the use of the **AdvertiseProduct** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a><span data-ttu-id="e84bf-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e84bf-144">Requirements</span></span>



| <span data-ttu-id="e84bf-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="e84bf-145">Requirement</span></span> | <span data-ttu-id="e84bf-146">Value</span><span class="sxs-lookup"><span data-stu-id="e84bf-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e84bf-147">Versión</span><span class="sxs-lookup"><span data-stu-id="e84bf-147">Version</span></span><br/> | <span data-ttu-id="e84bf-148">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e84bf-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e84bf-149">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e84bf-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e84bf-150">Windows Installer 4,5 en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="e84bf-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="e84bf-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e84bf-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="e84bf-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e84bf-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="e84bf-153">IID</span><span class="sxs-lookup"><span data-stu-id="e84bf-153">IID</span></span><br/>     | <span data-ttu-id="e84bf-154">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e84bf-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="e84bf-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="e84bf-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e84bf-156">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="e84bf-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="e84bf-157">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="e84bf-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




