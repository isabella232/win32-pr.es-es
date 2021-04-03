---
description: Contiene los resultados de la consulta de la base de datos de correcciones de compatibilidad (shim) para un ejecutable coincidente.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: Estructura SDBQUERYRESULT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998206"
---
# <a name="sdbqueryresult-structure"></a><span data-ttu-id="7e67f-103">Estructura SDBQUERYRESULT</span><span class="sxs-lookup"><span data-stu-id="7e67f-103">SDBQUERYRESULT structure</span></span>

<span data-ttu-id="7e67f-104">Contiene los resultados de la consulta de la base de datos de correcciones de compatibilidad (shim) para un ejecutable coincidente.</span><span class="sxs-lookup"><span data-stu-id="7e67f-104">Contains the results from querying the shim database for a matching executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e67f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e67f-105">Syntax</span></span>


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a><span data-ttu-id="7e67f-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e67f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e67f-107">**atrExes**</span><span class="sxs-lookup"><span data-stu-id="7e67f-107">**atrExes**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-108">Los valores **TAGREF** de los archivos ejecutables coincidentes.</span><span class="sxs-lookup"><span data-stu-id="7e67f-108">The **TAGREF** values of the matching executable files.</span></span> <span data-ttu-id="7e67f-109">Tenga en cuenta que los archivos **\_ \_ exe Max de SDB** se definen como 16.</span><span class="sxs-lookup"><span data-stu-id="7e67f-109">Note that **SDB\_MAX\_EXES** is defined as 16.</span></span>

</dd> <dt>

<span data-ttu-id="7e67f-110">**adwExeFlags**</span><span class="sxs-lookup"><span data-stu-id="7e67f-110">**adwExeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-111">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7e67f-111">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7e67f-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Deshabilitar \_ correcciones de compatibilidad** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="7e67f-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ Deshabilitar \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="7e67f-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="7e67f-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ APPHELP \_ Cancel** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="7e67f-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Deshabilitar \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="7e67f-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ Deshabilitar \_ capa** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="7e67f-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Deshabilitar \_ controlador** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="7e67f-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="7e67f-119">**atrLayers**</span><span class="sxs-lookup"><span data-stu-id="7e67f-119">**atrLayers**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-120">Los valores de **TAGREF** de las capas coincidentes.</span><span class="sxs-lookup"><span data-stu-id="7e67f-120">The **TAGREF** values of the matching layers.</span></span> <span data-ttu-id="7e67f-121">Tenga en cuenta que los **\_ \_ niveles máximos de SDB** están definidos como 8.</span><span class="sxs-lookup"><span data-stu-id="7e67f-121">Note that **SDB\_MAX\_LAYERS** is defined as 8.</span></span>

</dd> <dt>

<span data-ttu-id="7e67f-122">**dwLayerFlags**</span><span class="sxs-lookup"><span data-stu-id="7e67f-122">**dwLayerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-123">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7e67f-123">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7e67f-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Deshabilitar \_ correcciones de compatibilidad** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="7e67f-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ Deshabilitar \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="7e67f-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="7e67f-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ APPHELP \_ Cancel** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="7e67f-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Deshabilitar \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="7e67f-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ Deshabilitar \_ capa** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="7e67f-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Deshabilitar \_ controlador** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="7e67f-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="7e67f-131">**trApphelp**</span><span class="sxs-lookup"><span data-stu-id="7e67f-131">**trApphelp**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-132">El valor **TAGREF** del mensaje de apphelp del ejecutable correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7e67f-132">The **TAGREF** value of the apphelp message of the corresponding executable.</span></span>

</dd> <dt>

<span data-ttu-id="7e67f-133">**dwExeCount**</span><span class="sxs-lookup"><span data-stu-id="7e67f-133">**dwExeCount**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-134">Número de elementos de **atrExes**.</span><span class="sxs-lookup"><span data-stu-id="7e67f-134">The number of elements in **atrExes**.</span></span>

</dd> <dt>

<span data-ttu-id="7e67f-135">**dwLayerCount**</span><span class="sxs-lookup"><span data-stu-id="7e67f-135">**dwLayerCount**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-136">Número de elementos de **atrLayers**.</span><span class="sxs-lookup"><span data-stu-id="7e67f-136">The number of elements in **atrLayers**.</span></span>

</dd> <dt>

<span data-ttu-id="7e67f-137">**guidID**</span><span class="sxs-lookup"><span data-stu-id="7e67f-137">**guidID**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-138">GUID del último archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="7e67f-138">The GUID of the last executable file.</span></span>

</dd> <dt>

<span data-ttu-id="7e67f-139">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="7e67f-139">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-140">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7e67f-140">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7e67f-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Deshabilitar \_ correcciones de compatibilidad** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="7e67f-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ Deshabilitar \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="7e67f-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="7e67f-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ APPHELP \_ Cancel** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="7e67f-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Deshabilitar \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="7e67f-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ Deshabilitar \_ capa** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="7e67f-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="7e67f-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Deshabilitar \_ controlador** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="7e67f-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="7e67f-148">**dwCustomSDBMap**</span><span class="sxs-lookup"><span data-stu-id="7e67f-148">**dwCustomSDBMap**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-149">Una asignación de las bases de datos de corrección de compatibilidad (shim) personalizadas.</span><span class="sxs-lookup"><span data-stu-id="7e67f-149">A map of the custom shim databases.</span></span> <span data-ttu-id="7e67f-150">Los bits correspondientes se establecen si **rgGuidDB** es válido.</span><span class="sxs-lookup"><span data-stu-id="7e67f-150">The corresponding bits are set if **rgGuidDB** is valid.</span></span>

</dd> <dt>

<span data-ttu-id="7e67f-151">**rgGuidDB**</span><span class="sxs-lookup"><span data-stu-id="7e67f-151">**rgGuidDB**</span></span>
</dt> <dd>

<span data-ttu-id="7e67f-152">Los GUID de las bases de datos de correcciones de compatibilidad (shim).</span><span class="sxs-lookup"><span data-stu-id="7e67f-152">The GUIDs of the shim databases.</span></span> <span data-ttu-id="7e67f-153">Tenga en cuenta que **SDB \_ Max \_ SDBS** se define como 16.</span><span class="sxs-lookup"><span data-stu-id="7e67f-153">Note that **SDB\_MAX\_SDBS** is defined as 16.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e67f-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e67f-154">Requirements</span></span>



| <span data-ttu-id="7e67f-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e67f-155">Requirement</span></span> | <span data-ttu-id="7e67f-156">Value</span><span class="sxs-lookup"><span data-stu-id="7e67f-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e67f-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e67f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="7e67f-158">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7e67f-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7e67f-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e67f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="7e67f-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e67f-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e67f-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e67f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e67f-162">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="7e67f-162">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> </dl>

 

 




