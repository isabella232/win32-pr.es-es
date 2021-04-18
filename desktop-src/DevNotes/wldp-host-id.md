---
description: Identifica el tipo de host del llamador WLDP.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: Enumeración WLDP_HOST_ID (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538344"
---
# <a name="wldp_host_id-enumeration"></a><span data-ttu-id="91d68-103">\_ \_ Enumeración de ID. de host de WLDP</span><span class="sxs-lookup"><span data-stu-id="91d68-103">WLDP\_HOST\_ID enumeration</span></span>

<span data-ttu-id="91d68-104">Identifica el tipo de host del llamador WLDP.</span><span class="sxs-lookup"><span data-stu-id="91d68-104">Identifies the host type of the WLDP caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d68-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91d68-105">Syntax</span></span>


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a><span data-ttu-id="91d68-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="91d68-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="91d68-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_ identificador de HOST \_ \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="91d68-107"><span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span> **WLDP\_HOST\_ID\_UNKNOWN**</span></span> 
</dt> <dd>

<span data-ttu-id="91d68-108">No se conoce el tipo de host.</span><span class="sxs-lookup"><span data-stu-id="91d68-108">The host type is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="91d68-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_ \_ID. \_ de host global**</span><span class="sxs-lookup"><span data-stu-id="91d68-109"><span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span> **WLDP\_HOST\_ID\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="91d68-110">El tipo de host es una directiva global.</span><span class="sxs-lookup"><span data-stu-id="91d68-110">The host type is global policy.</span></span>

</dd> <dt>

<span data-ttu-id="91d68-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**identificador de host de WLDP \_ \_ \_ VBA**</span><span class="sxs-lookup"><span data-stu-id="91d68-111"><span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP\_HOST\_ID\_VBA**</span></span>
</dt> <dd>

<span data-ttu-id="91d68-112">El tipo de host es VBScript.</span><span class="sxs-lookup"><span data-stu-id="91d68-112">The host type is VBScript.</span></span>

</dd> <dt>

<span data-ttu-id="91d68-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_ \_ \_ WSH ID de host**</span><span class="sxs-lookup"><span data-stu-id="91d68-113"><span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span> **WLDP\_HOST\_ID\_WSH**</span></span>
</dt> <dd>

<span data-ttu-id="91d68-114">El tipo de host es Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="91d68-114">The host type is Windows Script Host.</span></span>

</dd> <dt>

<span data-ttu-id="91d68-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ \_ \_ POWERSHELL de ID. de host**</span><span class="sxs-lookup"><span data-stu-id="91d68-115"><span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span> **WLDP\_HOST\_ID\_POWERSHELL**</span></span>
</dt> <dd>

<span data-ttu-id="91d68-116">El tipo de host es Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91d68-116">The host type is Windows Powershell.</span></span>

</dd> <dt>

<span data-ttu-id="91d68-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ \_ID. \_ de host IE**</span><span class="sxs-lookup"><span data-stu-id="91d68-117"><span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span> **WLDP\_HOST\_ID\_IE**</span></span>
</dt> <dd>

<span data-ttu-id="91d68-118">El tipo de host es Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="91d68-118">The host type is Internet Explorer.</span></span>

</dd> <dt>

<span data-ttu-id="91d68-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ \_ \_ MSI de ID. de host**</span><span class="sxs-lookup"><span data-stu-id="91d68-119"><span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span> **WLDP\_HOST\_ID\_MSI**</span></span>
</dt> <dd>

<span data-ttu-id="91d68-120">El tipo de host es el Microsoft Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="91d68-120">The host type is the Microsoft Windows Installer.</span></span>

</dd> <dt>

<span data-ttu-id="91d68-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ \_ID. \_ de host máximo**</span><span class="sxs-lookup"><span data-stu-id="91d68-121"><span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span> **WLDP\_HOST\_ID\_MAX**</span></span> 
</dt> <dd>

<span data-ttu-id="91d68-122">Valor de enumeración máximo.</span><span class="sxs-lookup"><span data-stu-id="91d68-122">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91d68-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91d68-123">Requirements</span></span>



| <span data-ttu-id="91d68-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="91d68-124">Requirement</span></span> | <span data-ttu-id="91d68-125">Value</span><span class="sxs-lookup"><span data-stu-id="91d68-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="91d68-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91d68-126">Minimum supported client</span></span><br/> | <span data-ttu-id="91d68-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="91d68-127">Windows 8 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91d68-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91d68-128">Minimum supported server</span></span><br/> | <span data-ttu-id="91d68-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="91d68-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="91d68-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91d68-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d68-131"><dt>WLDP. h</dt></span><span class="sxs-lookup"><span data-stu-id="91d68-131"><dt>Wldp.h</dt></span></span> </dl> |



 

 




