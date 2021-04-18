---
description: Contiene información de datos de apphelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: Estructura de APPHELP_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659345"
---
# <a name="apphelp_data-structure"></a><span data-ttu-id="6e976-103">Estructura de datos de APPHELP \_</span><span class="sxs-lookup"><span data-stu-id="6e976-103">APPHELP\_DATA structure</span></span>

<span data-ttu-id="6e976-104">Contiene información de datos de apphelp.</span><span class="sxs-lookup"><span data-stu-id="6e976-104">Contains Apphelp data information.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e976-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e976-105">Syntax</span></span>


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a><span data-ttu-id="6e976-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e976-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6e976-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="6e976-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-108">Este parámetro puede ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="6e976-108">This parameter can be one of more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6e976-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Deshabilitar \_ correcciones de compatibilidad** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="6e976-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="6e976-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ Deshabilitar \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="6e976-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="6e976-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="6e976-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="6e976-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ APPHELP \_ Cancel** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="6e976-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="6e976-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Deshabilitar \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="6e976-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="6e976-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ Deshabilitar \_ capa** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="6e976-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="6e976-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Deshabilitar \_ controlador** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="6e976-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="6e976-116">**dwSeverity**</span><span class="sxs-lookup"><span data-stu-id="6e976-116">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-117">Este parámetro puede ser APPTYPE \_ None (0).</span><span class="sxs-lookup"><span data-stu-id="6e976-117">This parameter can be APPTYPE\_NONE (0).</span></span>

</dd> <dt>

<span data-ttu-id="6e976-118">**dwHTMLHelpID**</span><span class="sxs-lookup"><span data-stu-id="6e976-118">**dwHTMLHelpID**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-119">Identificador de la ayuda HTML.</span><span class="sxs-lookup"><span data-stu-id="6e976-119">The HTML Help identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6e976-120">**szAppName**</span><span class="sxs-lookup"><span data-stu-id="6e976-120">**szAppName**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-121">Nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6e976-121">The application name.</span></span>

</dd> <dt>

<span data-ttu-id="6e976-122">**trExe**</span><span class="sxs-lookup"><span data-stu-id="6e976-122">**trExe**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-123">[**TAGREF**](tagref.md) del archivo ejecutable correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6e976-123">The [**TAGREF**](tagref.md) of the corresponding executable file.</span></span>

</dd> <dt>

<span data-ttu-id="6e976-124">**szURL**</span><span class="sxs-lookup"><span data-stu-id="6e976-124">**szURL**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-125">La dirección URL del vínculo de apphelp en línea.</span><span class="sxs-lookup"><span data-stu-id="6e976-125">The URL for Apphelp online link.</span></span>

</dd> <dt>

<span data-ttu-id="6e976-126">**szLink**</span><span class="sxs-lookup"><span data-stu-id="6e976-126">**szLink**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-127">El texto del vínculo para **szURL**.</span><span class="sxs-lookup"><span data-stu-id="6e976-127">The link text for **szURL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e976-128">**szAppTitle**</span><span class="sxs-lookup"><span data-stu-id="6e976-128">**szAppTitle**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-129">Título del mensaje de apphelp.</span><span class="sxs-lookup"><span data-stu-id="6e976-129">The title for the Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="6e976-130">**szContact**</span><span class="sxs-lookup"><span data-stu-id="6e976-130">**szContact**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-131">Información de contacto del proveedor.</span><span class="sxs-lookup"><span data-stu-id="6e976-131">The vendor contact information.</span></span>

</dd> <dt>

<span data-ttu-id="6e976-132">**szDetails**</span><span class="sxs-lookup"><span data-stu-id="6e976-132">**szDetails**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-133">Mensaje de apphelp detallado.</span><span class="sxs-lookup"><span data-stu-id="6e976-133">The detailed Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="6e976-134">**dwData**</span><span class="sxs-lookup"><span data-stu-id="6e976-134">**dwData**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-135">Datos definidos por el usuario administrados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6e976-135">User-defined data managed by the application.</span></span>

</dd> <dt>

<span data-ttu-id="6e976-136">**bSPEntry**</span><span class="sxs-lookup"><span data-stu-id="6e976-136">**bSPEntry**</span></span>
</dt> <dd>

<span data-ttu-id="6e976-137">Este miembro es **true** si esta entrada está en la base de datos Service Pack y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6e976-137">This member is **TRUE** if this entry is in the service pack database and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e976-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e976-138">Requirements</span></span>



| <span data-ttu-id="6e976-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e976-139">Requirement</span></span> | <span data-ttu-id="6e976-140">Value</span><span class="sxs-lookup"><span data-stu-id="6e976-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6e976-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e976-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6e976-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6e976-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6e976-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e976-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6e976-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e976-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e976-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e976-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e976-146">**SdbReadApphelpDetailsData**</span><span class="sxs-lookup"><span data-stu-id="6e976-146">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




