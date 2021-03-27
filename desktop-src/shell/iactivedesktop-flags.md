---
description: En esta sección se describen las marcas usadas por los métodos de la interfaz IActiveDesktop.
title: Marcas IActiveDesktop (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987487"
---
# <a name="iactivedesktop-flags"></a><span data-ttu-id="f4d24-103">Marcas de IActiveDesktop</span><span class="sxs-lookup"><span data-stu-id="f4d24-103">IActiveDesktop Flags</span></span>

<span data-ttu-id="f4d24-104">En esta sección se describen las marcas usadas por los métodos de la interfaz [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .</span><span class="sxs-lookup"><span data-stu-id="f4d24-104">This section describes the flags used by [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface methods.</span></span>

<dl> <dt>

<span data-ttu-id="f4d24-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**\_aplicar \_ todo en ad**</span><span class="sxs-lookup"><span data-stu-id="f4d24-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD\_APPLY\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-106">Agregación de los valores de \* \* \* \* ad Apply Save \* \* \* \* \_ \_ , \* \* \* \* ad \_ Apply HTMLGEN \* \* \* \* \_ y \* \* \* \* \_ ad \_ Apply Refresh \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="f4d24-106">Aggregate of the \*\*\*\*AD\_APPLY\_SAVE\*\*\*\*, \*\*\*\*AD\_APPLY\_HTMLGEN\*\*\*\*, and \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**\_aplicación de \_ actualización almacenada en búfer \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD\_APPLY\_BUFFERED\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-108">Inicia un temporizador y agrega todas las solicitudes de actualización realizadas con esta marca durante ese intervalo de tiempo en una única actualización.</span><span class="sxs-lookup"><span data-stu-id="f4d24-108">Starts a timer and aggregates all the refresh requests made with this flag during that time interval into a single refresh.</span></span> <span data-ttu-id="f4d24-109">Este intervalo se establece en cinco segundos.</span><span class="sxs-lookup"><span data-stu-id="f4d24-109">This interval is set at five seconds.</span></span> <span data-ttu-id="f4d24-110">Al final del intervalo, o si se solicita una actualización durante el intervalo sin una marca \* \* \* \* AD \_ Apply \_ buffered \_ Refresh \* \* \* \*, se realiza la actualización y se detiene el temporizador.</span><span class="sxs-lookup"><span data-stu-id="f4d24-110">At the end of the interval, or if a refresh is requested during the interval without an \*\*\*\*AD\_APPLY\_BUFFERED\_REFRESH\*\*\*\* flag, the refresh is made and the timer is stopped.</span></span> <span data-ttu-id="f4d24-111">Esta marca debe combinarse con la marca \* \* \* \* AD \_ Apply Refresh \* \* \* \* \_ .</span><span class="sxs-lookup"><span data-stu-id="f4d24-111">This flag must be combined with the \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**\_DYNAMICREFRESH de aplicación de ad \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD\_APPLY\_DYNAMICREFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-113">[Versión 5,0](versions.md).</span><span class="sxs-lookup"><span data-stu-id="f4d24-113">[Version 5.0](versions.md).</span></span> <span data-ttu-id="f4d24-114">Use HTML dinámico para actualizar solo los elementos que han cambiado desde la última actualización, no todo el escritorio.</span><span class="sxs-lookup"><span data-stu-id="f4d24-114">Use dynamic HTML to refresh only those items that have changed since the last refresh, not the entire desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**\_fuerza de aplicación de ad \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD\_APPLY\_FORCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-116">Forzar un cambio de Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="f4d24-116">Force an Active Desktop change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**\_HTMLGEN de aplicación de ad \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD\_APPLY\_HTMLGEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-118">Vuelva a generar el archivo HTML del escritorio.</span><span class="sxs-lookup"><span data-stu-id="f4d24-118">Regenerate the desktop HTML file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**\_actualización de aplicación de ad \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD\_APPLY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-120">Actualice el elemento de escritorio.</span><span class="sxs-lookup"><span data-stu-id="f4d24-120">Refresh the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**\_aplicar \_ guardado de ad**</span><span class="sxs-lookup"><span data-stu-id="f4d24-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD\_APPLY\_SAVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-122">Guarde el elemento de escritorio.</span><span class="sxs-lookup"><span data-stu-id="f4d24-122">Save the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**\_todo Elem \_ todo**</span><span class="sxs-lookup"><span data-stu-id="f4d24-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP\_ELEM\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-124">Agregación de los valores de Elem de COMP \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="f4d24-124">Aggregate of the COMP\_ELEM\_\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP \_ Elem \_ activada**</span><span class="sxs-lookup"><span data-stu-id="f4d24-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP\_ELEM\_CHECKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-126">El elemento se ha comprobado.</span><span class="sxs-lookup"><span data-stu-id="f4d24-126">The item has been checked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ Elem \_ CURITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="f4d24-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP\_ELEM\_CURITEMSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-128">Estado actual del elemento de escritorio.</span><span class="sxs-lookup"><span data-stu-id="f4d24-128">The current state of the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ Elem \_ FRIENDLYNAME**</span><span class="sxs-lookup"><span data-stu-id="f4d24-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP\_ELEM\_FRIENDLYNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-130">Nombre descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="f4d24-130">The friendly name of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ Elem \_ noscroll**</span><span class="sxs-lookup"><span data-stu-id="f4d24-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP\_ELEM\_NOSCROLL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-132">El elemento no es desplazable.</span><span class="sxs-lookup"><span data-stu-id="f4d24-132">The item is not scrollable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMPt \_ Elem \_ original \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="f4d24-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP\_ELEM\_ORIGINAL\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-134">Información de estado del elemento de escritorio original.</span><span class="sxs-lookup"><span data-stu-id="f4d24-134">The original desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**\_OC Elem \_ pos \_ izquierda**</span><span class="sxs-lookup"><span data-stu-id="f4d24-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP\_ELEM\_POS\_LEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-136">Posición horizontal del elemento.</span><span class="sxs-lookup"><span data-stu-id="f4d24-136">The horizontal position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**\_borde de Elem Elem \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP\_ELEM\_POS\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-138">Posición vertical del elemento.</span><span class="sxs-lookup"><span data-stu-id="f4d24-138">The vertical position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ Elem \_ pos \_ ZINDEX**</span><span class="sxs-lookup"><span data-stu-id="f4d24-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP\_ELEM\_POS\_ZINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-140">Índice z del elemento.</span><span class="sxs-lookup"><span data-stu-id="f4d24-140">The z-index of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ Elem \_ restaurada \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="f4d24-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP\_ELEM\_RESTORED\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-142">Información de estado del elemento de escritorio restaurada.</span><span class="sxs-lookup"><span data-stu-id="f4d24-142">The restored desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**\_altura del \_ tamaño de Elem. \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**COMP\_ELEM\_SIZE\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-144">Alto del elemento.</span><span class="sxs-lookup"><span data-stu-id="f4d24-144">The height of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**\_ancho de \_ tamaño de Elem. \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**COMP\_ELEM\_SIZE\_WIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-146">Ancho del elemento.</span><span class="sxs-lookup"><span data-stu-id="f4d24-146">The width of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**\_origen de Elem. \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP\_ELEM\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-148">Origen original del elemento.</span><span class="sxs-lookup"><span data-stu-id="f4d24-148">The original source of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**\_tipo Elem. de comp. \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP\_ELEM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-150">Tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="f4d24-150">The item type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**\_tipo COMP \_ CFHTML**</span><span class="sxs-lookup"><span data-stu-id="f4d24-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**COMP\_TYPE\_CFHTML**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-152">Formato HTML comprimido.</span><span class="sxs-lookup"><span data-stu-id="f4d24-152">Compressed format HTML.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**\_control de tipo COMP \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP\_TYPE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-154">El elemento es un control.</span><span class="sxs-lookup"><span data-stu-id="f4d24-154">The item is a control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**\_tipo COMP \_ HTMLDOC**</span><span class="sxs-lookup"><span data-stu-id="f4d24-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**COMP\_TYPE\_HTMLDOC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-156">El elemento es un documento HTML.</span><span class="sxs-lookup"><span data-stu-id="f4d24-156">The item is an HTML document.</span></span> <span data-ttu-id="f4d24-157">Esta marca solo se debe usar cuando sea absolutamente necesario.</span><span class="sxs-lookup"><span data-stu-id="f4d24-157">This flag should only be used when absolutely necessary.</span></span> <span data-ttu-id="f4d24-158">Hace que un documento HTML se inserte literalmente en el archivo Desktop. htt que se usa para controlar el diseño del escritorio.</span><span class="sxs-lookup"><span data-stu-id="f4d24-158">It causes an HTML document to be inserted verbatim into the Desktop.htt file used to control layout of the desktop.</span></span> <span data-ttu-id="f4d24-159">En la mayoría de los casos, debe usar la marca \* \* \* \* tipo de COMP \_ \_ website \* \* \* \* para agregar elementos al escritorio.</span><span class="sxs-lookup"><span data-stu-id="f4d24-159">For most cases, you should use the \*\*\*\*COMP\_TYPE\_WEBSITE\*\*\*\* flag to add items to the desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**\_tipo COMP \_ máx.**</span><span class="sxs-lookup"><span data-stu-id="f4d24-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**COMP\_TYPE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-161">Valor máximo de una marca de \_ tipo COMP \_ \* .</span><span class="sxs-lookup"><span data-stu-id="f4d24-161">The maximum value of a COMP\_TYPE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**\_imagen del tipo COMP \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**COMP\_TYPE\_PICTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-163">El elemento es una imagen.</span><span class="sxs-lookup"><span data-stu-id="f4d24-163">The item is a picture.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**\_sitio web de tipo COMP \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**COMP\_TYPE\_WEBSITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-165">El elemento es un sitio Web.</span><span class="sxs-lookup"><span data-stu-id="f4d24-165">The item is a website.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**\_parte superior del componente**</span><span class="sxs-lookup"><span data-stu-id="f4d24-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPONENT\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-167">Un valor de orden z que significa que el elemento está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="f4d24-167">A z-order value meaning the item is at the top.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**Centro de WPSTYLE \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE\_CENTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-169">El papel tapiz está centrado.</span><span class="sxs-lookup"><span data-stu-id="f4d24-169">The wallpaper is centered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ máx.**</span><span class="sxs-lookup"><span data-stu-id="f4d24-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-171">Valor máximo de una marca WPSTYLE \_ \* .</span><span class="sxs-lookup"><span data-stu-id="f4d24-171">The maximum value of a WPSTYLE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE \_ Stretch**</span><span class="sxs-lookup"><span data-stu-id="f4d24-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE\_STRETCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-173">El papel tapiz se ajusta para ajustarse a toda la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f4d24-173">The wallpaper is stretched to fit the entire screen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**icono de WPSTYLE \_**</span><span class="sxs-lookup"><span data-stu-id="f4d24-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**WPSTYLE\_TILE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-175">El papel tapiz está en mosaico.</span><span class="sxs-lookup"><span data-stu-id="f4d24-175">The wallpaper is tiled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f4d24-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**\_intervalo WPSTYLE**</span><span class="sxs-lookup"><span data-stu-id="f4d24-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE\_SPAN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f4d24-177">**Windows 8 y versiones posteriores**: el papel tapiz abarca varios monitores.</span><span class="sxs-lookup"><span data-stu-id="f4d24-177">**Windows 8 and later**: The wallpaper spans multiple monitors.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4d24-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4d24-178">Requirements</span></span>



| <span data-ttu-id="f4d24-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4d24-179">Requirement</span></span> | <span data-ttu-id="f4d24-180">Value</span><span class="sxs-lookup"><span data-stu-id="f4d24-180">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f4d24-181">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4d24-181">Header</span></span><br/> | <dl> <span data-ttu-id="f4d24-182"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4d24-182"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
