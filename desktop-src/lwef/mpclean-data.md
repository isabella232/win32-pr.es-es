---
title: MPCLEAN_DATA estructura (MpClient. h)
description: Datos de notificación pasados a la función de devolución de llamada Clean.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCLEAN_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801921"
---
# <a name="mpclean_data-structure"></a><span data-ttu-id="95c07-105">\_Estructura de datos MPCLEAN</span><span class="sxs-lookup"><span data-stu-id="95c07-105">MPCLEAN\_DATA structure</span></span>

<span data-ttu-id="95c07-106">Datos de notificación pasados a la función de devolución de llamada Clean.</span><span class="sxs-lookup"><span data-stu-id="95c07-106">Notification data passed to clean callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="95c07-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95c07-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a><span data-ttu-id="95c07-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="95c07-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="95c07-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="95c07-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="95c07-110">Tipo: **\_ ID. de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="95c07-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="95c07-111">Identificador de amenaza para la amenaza de **limpieza de MPNOTIFY \_ \_ \_ Inicio** de MPNOTIFY de la amenaza / **\_ limpia \_ \_ correctamente** / **MPNOTIFY eventos de \_ \_ \_ error de amenaza limpia** .</span><span class="sxs-lookup"><span data-stu-id="95c07-111">Threat identifier for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="95c07-112">El bit superior se establece para identificar las amenazas relacionadas con el antivirus.</span><span class="sxs-lookup"><span data-stu-id="95c07-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="95c07-113">**ThreatAction**</span><span class="sxs-lookup"><span data-stu-id="95c07-113">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="95c07-114">Tipo: **[ **\_ acción MPTHREAT**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="95c07-114">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="95c07-115">Acción de amenaza para la amenaza de limpieza de **MPNOTIFY \_ \_ \_ Inicio** de MPNOTIFY de la amenaza / **\_ limpia \_ \_ correctamente** / **MPNOTIFY eventos de \_ \_ \_ error de amenaza limpia** .</span><span class="sxs-lookup"><span data-stu-id="95c07-115">Threat action for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="95c07-116">Consulte [**la \_ acción MPTHREAT**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="95c07-116">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="95c07-117">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="95c07-117">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="95c07-118">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="95c07-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="95c07-119">Estado adicional o acciones asociadas a la acción realizada.</span><span class="sxs-lookup"><span data-stu-id="95c07-119">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="95c07-120">Se trata de una combinación de marcas de bits de la [**\_ marca MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="95c07-120">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="95c07-121">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="95c07-121">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="95c07-122">Tipo: **PMPRESOURCE \_ info**</span><span class="sxs-lookup"><span data-stu-id="95c07-122">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="95c07-123">Información de recursos para los eventos de **\_ \_ \_** / **\_ \_ \_** / **\_ \_ \_ error** de limpieza de amenaza de limpieza de MPNOTIFY de MPNOTIFY correcta</span><span class="sxs-lookup"><span data-stu-id="95c07-123">Resource information for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="95c07-124">Vea [**\_ información de MPRESOURCE**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="95c07-124">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95c07-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95c07-125">Requirements</span></span>



| <span data-ttu-id="95c07-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="95c07-126">Requirement</span></span> | <span data-ttu-id="95c07-127">Value</span><span class="sxs-lookup"><span data-stu-id="95c07-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95c07-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95c07-128">Minimum supported client</span></span><br/> | <span data-ttu-id="95c07-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="95c07-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="95c07-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95c07-130">Minimum supported server</span></span><br/> | <span data-ttu-id="95c07-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="95c07-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95c07-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95c07-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="95c07-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="95c07-133"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95c07-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="95c07-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c07-135">**información de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="95c07-135">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="95c07-136">**\_marca MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="95c07-136">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="95c07-137">**\_acción MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="95c07-137">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





