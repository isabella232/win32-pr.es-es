---
description: La estructura EXPERTENUMINFO proporciona información sobre el experto.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Estructura EXPERTENUMINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666300"
---
# <a name="expertenuminfo-structure"></a><span data-ttu-id="dde32-103">Estructura EXPERTENUMINFO</span><span class="sxs-lookup"><span data-stu-id="dde32-103">EXPERTENUMINFO structure</span></span>

<span data-ttu-id="dde32-104">La estructura **EXPERTENUMINFO** proporciona información sobre el experto.</span><span class="sxs-lookup"><span data-stu-id="dde32-104">The **EXPERTENUMINFO** structure provides information about the expert.</span></span> <span data-ttu-id="dde32-105">Monitor de red asigna memoria para la estructura y la pasa al experto cuando llama a la función [**Register Expert**](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="dde32-105">Network Monitor allocates memory for the structure, and passes it to the expert when it calls the [**Register Expert**](register-expert.md) function.</span></span> <span data-ttu-id="dde32-106">Cuando el experto recibe la estructura, debe rellenar toda la información que Monitor de red solicitudes.</span><span class="sxs-lookup"><span data-stu-id="dde32-106">When the expert receives the structure, it must then fill-in all the information that Network Monitor requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde32-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dde32-107">Syntax</span></span>


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a><span data-ttu-id="dde32-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dde32-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dde32-109">**szName**</span><span class="sxs-lookup"><span data-stu-id="dde32-109">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-110">Nombre del experto.</span><span class="sxs-lookup"><span data-stu-id="dde32-110">Name of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="dde32-111">**szVendor**</span><span class="sxs-lookup"><span data-stu-id="dde32-111">**szVendor**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-112">Nombre del proveedor que crea el experto.</span><span class="sxs-lookup"><span data-stu-id="dde32-112">Name of the vendor that creates the expert.</span></span>

</dd> <dt>

<span data-ttu-id="dde32-113">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="dde32-113">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-114">Descripción del experto.</span><span class="sxs-lookup"><span data-stu-id="dde32-114">Description of the expert.</span></span> <span data-ttu-id="dde32-115">El valor del miembro **szDescription** puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="dde32-115">The value of the **szDescription** member may be **NULL**.</span></span> <span data-ttu-id="dde32-116">Si el nombre es demasiado largo, se truncará en la configuración predeterminada del visor.</span><span class="sxs-lookup"><span data-stu-id="dde32-116">If the name is too long, it is truncated in the default viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="dde32-117">**Versión**</span><span class="sxs-lookup"><span data-stu-id="dde32-117">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-118">El valor debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dde32-118">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dde32-119">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="dde32-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-120">Las marcas siguientes describen el experto.</span><span class="sxs-lookup"><span data-stu-id="dde32-120">The following flags describe the expert.</span></span>



| <span data-ttu-id="dde32-121">Value</span><span class="sxs-lookup"><span data-stu-id="dde32-121">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="dde32-122">Significado</span><span class="sxs-lookup"><span data-stu-id="dde32-122">Meaning</span></span>                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <span data-ttu-id="dde32-123"><dt>**\_marca de enumeración experta \_ \_ configurable**</dt></span><span class="sxs-lookup"><span data-stu-id="dde32-123"><dt>**EXPERT\_ENUM\_FLAG\_CONFIGURABLE**</dt></span></span> </dl>                                          | <span data-ttu-id="dde32-124">El experto admite llamadas al método [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="dde32-124">The expert supports calls to the [**Configure**](configure.md) method.</span></span> <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <span data-ttu-id="dde32-125"><dt>**\_visor de marcas de enumeración de expertos \_ \_ \_ privado**</dt></span><span class="sxs-lookup"><span data-stu-id="dde32-125"><dt>**EXPERT\_ENUM\_FLAG\_VIEWER\_PRIVATE**</dt></span></span> </dl>                                   | <span data-ttu-id="dde32-126">El experto requiere un Visor de eventos privado (no compartido).</span><span class="sxs-lookup"><span data-stu-id="dde32-126">The expert requires a private (non-shared) Event Viewer.</span></span> <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <span data-ttu-id="dde32-127"><dt>**\_marca de enumeración de experto \_ \_ sin \_ visor**</dt></span><span class="sxs-lookup"><span data-stu-id="dde32-127"><dt>**EXPERT\_ENUM\_FLAG\_NO\_VIEWER**</dt></span></span> </dl>                                                  | <span data-ttu-id="dde32-128">El experto no envía notificaciones de eventos.</span><span class="sxs-lookup"><span data-stu-id="dde32-128">The expert does not send event notifications.</span></span> <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <span data-ttu-id="dde32-129"><dt>**\_marca de enumeración experta \_ \_ agregarme \_ \_ a \_ RMC \_ en \_ Resumen**</dt></span><span class="sxs-lookup"><span data-stu-id="dde32-129"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_SUMMARY**</dt></span></span> </dl> | <span data-ttu-id="dde32-130">Cuando el foco está en el panel de Resumen, el experto aparece en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="dde32-130">When the focus is in the summary pane, the expert appears on the context menu.</span></span> <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <span data-ttu-id="dde32-131"><dt>**\_marca de enumeración experta \_ \_ agregarme \_ \_ a \_ RMC \_ en \_ detalle**</dt></span><span class="sxs-lookup"><span data-stu-id="dde32-131"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_DETAIL**</dt></span></span> </dl>    | <span data-ttu-id="dde32-132">Cuando el foco está en el panel de detalles, el experto aparece en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="dde32-132">When the focus is in the detail pane, the expert appears on the context menu.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="dde32-133">**hExpert**</span><span class="sxs-lookup"><span data-stu-id="dde32-133">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-134">Identificador del experto.</span><span class="sxs-lookup"><span data-stu-id="dde32-134">Handle to the expert.</span></span> <span data-ttu-id="dde32-135">Cuando se usa la estructura **EXPERTENUMINFO** para registrar un experto, se omite el parámetro.</span><span class="sxs-lookup"><span data-stu-id="dde32-135">When the **EXPERTENUMINFO** structure is used to register an expert, the parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="dde32-136">**szDllName**</span><span class="sxs-lookup"><span data-stu-id="dde32-136">**szDllName**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-137">Miembro privado; No use.</span><span class="sxs-lookup"><span data-stu-id="dde32-137">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="dde32-138">**hModule**</span><span class="sxs-lookup"><span data-stu-id="dde32-138">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-139">Miembro privado; No use.</span><span class="sxs-lookup"><span data-stu-id="dde32-139">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="dde32-140">**pRegisterProc**</span><span class="sxs-lookup"><span data-stu-id="dde32-140">**pRegisterProc**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-141">Miembro privado; No use.</span><span class="sxs-lookup"><span data-stu-id="dde32-141">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="dde32-142">**pConfigProc**</span><span class="sxs-lookup"><span data-stu-id="dde32-142">**pConfigProc**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-143">Miembro privado; No use.</span><span class="sxs-lookup"><span data-stu-id="dde32-143">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="dde32-144">**pRunProc**</span><span class="sxs-lookup"><span data-stu-id="dde32-144">**pRunProc**</span></span>
</dt> <dd>

<span data-ttu-id="dde32-145">Miembro privado; No use.</span><span class="sxs-lookup"><span data-stu-id="dde32-145">Private member; do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dde32-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dde32-146">Requirements</span></span>



| <span data-ttu-id="dde32-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="dde32-147">Requirement</span></span> | <span data-ttu-id="dde32-148">Value</span><span class="sxs-lookup"><span data-stu-id="dde32-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dde32-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dde32-149">Minimum supported client</span></span><br/> | <span data-ttu-id="dde32-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dde32-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dde32-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dde32-151">Minimum supported server</span></span><br/> | <span data-ttu-id="dde32-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dde32-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dde32-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dde32-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="dde32-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dde32-154"><dt>Netmon.h</dt></span></span> </dl> |



 

 




