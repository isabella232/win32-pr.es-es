---
title: Interfaz IMsTscAdvancedSettings
description: Incluye métodos para recuperar y establecer propiedades que habilitan el almacenamiento en caché de mapas de bits, la compresión y la redirección de la impresora y el portapapeles.
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings, descrito
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4d55df30c940ecc5a5515f13c05a285507499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676759"
---
# <a name="imstscadvancedsettings-interface"></a><span data-ttu-id="0a75e-105">Interfaz IMsTscAdvancedSettings</span><span class="sxs-lookup"><span data-stu-id="0a75e-105">IMsTscAdvancedSettings interface</span></span>

<span data-ttu-id="0a75e-106">Incluye métodos para recuperar y establecer propiedades que habilitan el almacenamiento en caché de mapas de bits, la compresión y la redirección de la impresora y el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="0a75e-106">Includes methods to retrieve and set properties that enable bitmap caching, compression, and printer and clipboard redirection.</span></span> <span data-ttu-id="0a75e-107">También puede especificar nombres de archivos dll de cliente de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="0a75e-107">You can also specify names of virtual channel client DLLs.</span></span>

<span data-ttu-id="0a75e-108">Puede obtener una instancia de esta interfaz mediante la propiedad [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="0a75e-108">You obtain an instance of this interface by using the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="0a75e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0a75e-109">Members</span></span>

<span data-ttu-id="0a75e-110">La interfaz **IMsTscAdvancedSettings** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="0a75e-110">The **IMsTscAdvancedSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0a75e-111">**IMsTscAdvancedSettings** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0a75e-111">**IMsTscAdvancedSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="0a75e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a75e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a75e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a75e-113">Properties</span></span>

<span data-ttu-id="0a75e-114">La interfaz **IMsTscAdvancedSettings** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0a75e-114">The **IMsTscAdvancedSettings** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0a75e-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0a75e-115">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0a75e-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="0a75e-116">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0a75e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a75e-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0a75e-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a75e-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0a75e-119">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-120">Especifica si está habilitado el modo de entrada en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0a75e-120">Specifies whether background input mode is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="0a75e-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a75e-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0a75e-122">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-123">Especifica si está habilitado el almacenamiento en caché de mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="0a75e-123">Specifies whether bitmap caching is enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0a75e-124">El error ortográfico en el nombre de la propiedad se encuentra en la versión de lanzamiento del control.</span><span class="sxs-lookup"><span data-stu-id="0a75e-124">The spelling error in the name of the property is in the released version of the control.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0a75e-125"><a href="imstscadvancedsettings-compress.md"><strong>Comprimir</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a75e-125"><a href="imstscadvancedsettings-compress.md"><strong>Compress</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0a75e-126">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-127">Especifica si está habilitada la compresión.</span><span class="sxs-lookup"><span data-stu-id="0a75e-127">Specifies whether compression is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="0a75e-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a75e-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0a75e-129">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-130">Especifica si está habilitado el modo de pantalla completa controlado por contenedores.</span><span class="sxs-lookup"><span data-stu-id="0a75e-130">Specifies whether the container-handled full-screen mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0a75e-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a75e-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0a75e-132">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-133">Especifica si está habilitada la redirección de la impresora y del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="0a75e-133">Specifies whether printer and clipboard redirection is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="0a75e-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a75e-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-135">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="0a75e-135">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-136">Especifica el nombre del archivo que contiene los datos de icono a los que se tendrá acceso al mostrar el cliente en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0a75e-136">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0a75e-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a75e-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-138">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="0a75e-138">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-139">Especifica el índice del icono dentro del archivo de icono actual.</span><span class="sxs-lookup"><span data-stu-id="0a75e-139">Specifies the index of the icon within the current icon file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="0a75e-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a75e-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-141">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="0a75e-141">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-142">Especifica el nombre del identificador de configuración regional de entrada activo (anteriormente denominado distribución del teclado) que se va a usar para la conexión.</span><span class="sxs-lookup"><span data-stu-id="0a75e-142">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0a75e-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a75e-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-144">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="0a75e-144">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0a75e-145">Especifica los nombres de los archivos dll de cliente de canal virtual que se van a cargar.</span><span class="sxs-lookup"><span data-stu-id="0a75e-145">Specifies the names of virtual channel client DLLs to be loaded.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="0a75e-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a75e-146">Remarks</span></span>

<span data-ttu-id="0a75e-147">Esta interfaz se ha extendido mediante las siguientes interfaces, con cada nueva interfaz que hereda todos los métodos y propiedades de las interfaces anteriores:</span><span class="sxs-lookup"><span data-stu-id="0a75e-147">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="0a75e-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0a75e-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
-   [<span data-ttu-id="0a75e-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0a75e-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
-   [<span data-ttu-id="0a75e-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0a75e-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
-   [<span data-ttu-id="0a75e-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0a75e-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="0a75e-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0a75e-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="0a75e-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0a75e-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="0a75e-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0a75e-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="0a75e-155">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0a75e-155">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a75e-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a75e-156">Requirements</span></span>



| <span data-ttu-id="0a75e-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a75e-157">Requirement</span></span> | <span data-ttu-id="0a75e-158">Value</span><span class="sxs-lookup"><span data-stu-id="0a75e-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a75e-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a75e-159">Minimum supported client</span></span><br/> | <span data-ttu-id="0a75e-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a75e-160">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="0a75e-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a75e-161">Minimum supported server</span></span><br/> | <span data-ttu-id="0a75e-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a75e-162">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="0a75e-163">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0a75e-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a75e-164"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a75e-164"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="0a75e-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a75e-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a75e-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a75e-166"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="0a75e-167">IID</span><span class="sxs-lookup"><span data-stu-id="0a75e-167">IID</span></span><br/>                      | <span data-ttu-id="0a75e-168">IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="0a75e-168">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a75e-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a75e-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a75e-170">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="0a75e-170">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="0a75e-171">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="0a75e-171">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

