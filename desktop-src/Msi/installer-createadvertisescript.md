---
description: El método CreateAdvertiseScript del objeto de instalador genera un script de anuncio.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: 'Installer:: CreateAdvertiseScript (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654016"
---
# <a name="installercreateadvertisescript-method"></a><span data-ttu-id="59a53-103">Installer:: CreateAdvertiseScript (método)</span><span class="sxs-lookup"><span data-stu-id="59a53-103">Installer::CreateAdvertiseScript method</span></span>

<span data-ttu-id="59a53-104">El método **CreateAdvertiseScript** del objeto de [**instalador**](installer-object.md) genera un script de anuncio.</span><span class="sxs-lookup"><span data-stu-id="59a53-104">The **CreateAdvertiseScript** method of the [**Installer**](installer-object.md) object generates an advertise script.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59a53-105">Syntax</span></span>


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="59a53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59a53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59a53-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="59a53-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="59a53-108">Ruta de acceso completa al paquete de Windows Installer (. msi) que se va a anunciar.</span><span class="sxs-lookup"><span data-stu-id="59a53-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="59a53-109">*scriptFilePath*</span><span class="sxs-lookup"><span data-stu-id="59a53-109">*scriptFilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="59a53-110">Ruta de acceso completa al archivo de script que se va a crear con la información anunciada.</span><span class="sxs-lookup"><span data-stu-id="59a53-110">The full path to the script file to be created with the advertised information.</span></span>

</dd> <dt>

<span data-ttu-id="59a53-111">*transforma*</span><span class="sxs-lookup"><span data-stu-id="59a53-111">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="59a53-112">Lista de transformaciones que se van a aplicar al producto.</span><span class="sxs-lookup"><span data-stu-id="59a53-112">The list of transforms to apply to the product.</span></span> <span data-ttu-id="59a53-113">Las transformaciones en la lista están delimitadas por signos de punto y coma.</span><span class="sxs-lookup"><span data-stu-id="59a53-113">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="59a53-114">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="59a53-114">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="59a53-115">*language*</span><span class="sxs-lookup"><span data-stu-id="59a53-115">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="59a53-116">Idioma del paquete de instalación que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="59a53-116">The language of the installation package to use.</span></span> <span data-ttu-id="59a53-117">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="59a53-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="59a53-118">*platform*</span><span class="sxs-lookup"><span data-stu-id="59a53-118">*platform*</span></span> 
</dt> <dd>

<span data-ttu-id="59a53-119">Este parámetro especifica la plataforma en la que el instalador debe crear el script.</span><span class="sxs-lookup"><span data-stu-id="59a53-119">This parameter specifies for which platform the installer should create the script.</span></span> <span data-ttu-id="59a53-120">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="59a53-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="59a53-121">Valor</span><span class="sxs-lookup"><span data-stu-id="59a53-121">Value</span></span>                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="59a53-122">Significado</span><span class="sxs-lookup"><span data-stu-id="59a53-122">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <span data-ttu-id="59a53-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="59a53-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="59a53-124">Crea un script para la plataforma actual.</span><span class="sxs-lookup"><span data-stu-id="59a53-124">Creates a script for the current platform.</span></span><br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <span data-ttu-id="59a53-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="59a53-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="59a53-126">Crea un script para la plataforma x86.</span><span class="sxs-lookup"><span data-stu-id="59a53-126">Creates a script for the x86 platform.</span></span><br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <span data-ttu-id="59a53-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="59a53-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="59a53-128">Crea un script para sistemas basados en Itanium.</span><span class="sxs-lookup"><span data-stu-id="59a53-128">Creates a script for Itanium-based systems.</span></span><br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <span data-ttu-id="59a53-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="59a53-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="59a53-130">Crea un script para la plataforma x64.</span><span class="sxs-lookup"><span data-stu-id="59a53-130">Creates a script for the x64 platform.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="59a53-131">*options*</span><span class="sxs-lookup"><span data-stu-id="59a53-131">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="59a53-132">Opciones de anuncios.</span><span class="sxs-lookup"><span data-stu-id="59a53-132">Advertisement options.</span></span> <span data-ttu-id="59a53-133">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="59a53-133">This parameter is optional.</span></span> <span data-ttu-id="59a53-134">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="59a53-134">This parameter can be one of the following values.</span></span> <span data-ttu-id="59a53-135">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="59a53-135">This parameter is optional.</span></span>



| <span data-ttu-id="59a53-136">Value</span><span class="sxs-lookup"><span data-stu-id="59a53-136">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="59a53-137">Significado</span><span class="sxs-lookup"><span data-stu-id="59a53-137">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="59a53-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="59a53-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="59a53-139">Anuncio estándar</span><span class="sxs-lookup"><span data-stu-id="59a53-139">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="59a53-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="59a53-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="59a53-141">Anuncia una nueva instancia del producto.</span><span class="sxs-lookup"><span data-stu-id="59a53-141">Advertises a new instance of the product.</span></span> <span data-ttu-id="59a53-142">Requiere que la primera transformación de la lista de transformación del parámetro *transformaciones* sea la transformación de instancia que cambia el código de producto.</span><span class="sxs-lookup"><span data-stu-id="59a53-142">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="59a53-143">Para obtener más información, consulte [instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="59a53-143">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59a53-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59a53-144">Return value</span></span>

<span data-ttu-id="59a53-145">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="59a53-145">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59a53-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59a53-146">Remarks</span></span>

<span data-ttu-id="59a53-147">El método [**AdvertiseProduct**](installer-advertiseproduct.md) usa la función [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .</span><span class="sxs-lookup"><span data-stu-id="59a53-147">The [**AdvertiseProduct**](installer-advertiseproduct.md) method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="59a53-148">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="59a53-148">Examples</span></span>

<span data-ttu-id="59a53-149">En el siguiente ejemplo se muestra el uso del método **CreateAdvertiseScript** .</span><span class="sxs-lookup"><span data-stu-id="59a53-149">The following example demonstrates the use of the **CreateAdvertiseScript** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
```



## <a name="requirements"></a><span data-ttu-id="59a53-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59a53-150">Requirements</span></span>



| <span data-ttu-id="59a53-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="59a53-151">Requirement</span></span> | <span data-ttu-id="59a53-152">Value</span><span class="sxs-lookup"><span data-stu-id="59a53-152">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a53-153">Versión</span><span class="sxs-lookup"><span data-stu-id="59a53-153">Version</span></span><br/> | <span data-ttu-id="59a53-154">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="59a53-154">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="59a53-155">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="59a53-155">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="59a53-156">Windows Installer 4,5 en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="59a53-156">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="59a53-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="59a53-157">DLL</span></span><br/>     | <dl> <span data-ttu-id="59a53-158"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59a53-158"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="59a53-159">IID</span><span class="sxs-lookup"><span data-stu-id="59a53-159">IID</span></span><br/>     | <span data-ttu-id="59a53-160">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="59a53-160">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="59a53-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="59a53-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a53-162">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="59a53-162">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="59a53-163">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="59a53-163">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




