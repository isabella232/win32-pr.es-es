---
description: La estructura STATIONQUERY proporciona información acerca de un equipo específico mediante Monitor de red.
ms.assetid: b7202c6b-e2b9-4a6f-8b87-3d11879f1d69
title: Estructura STATIONQUERY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONQUERY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de76c4da7bc27d76c04aeeaa7a46d69134e411ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677633"
---
# <a name="stationquery-structure"></a><span data-ttu-id="f9dbc-103">Estructura STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="f9dbc-103">STATIONQUERY structure</span></span>

<span data-ttu-id="f9dbc-104">La estructura **STATIONQUERY** proporciona información acerca de un equipo específico mediante monitor de red.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-104">The **STATIONQUERY** structure provides information about a specific computer using Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9dbc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9dbc-105">Syntax</span></span>


```C++
typedef struct _STATIONQUERY {
  DWORD Flags;
  BYTE  BCDVerMinor;
  BYTE  BCDVerMajor;
  DWORD LicenseNumber;
  BYTE  MachineName[MACHINE_NAME_LENGTH];
  BYTE  UserName[USER_NAME_LENGTH];
  BYTE  Reserved[32];
  BYTE  AdapterAddress[6];
  WCHAR WMachineName[MACHINE_NAME_LENGTH];
  WCHAR WUserName[USER_NAME_LENGTH];
} STATIONQUERY, *LPSTATIONQUERY;
```



## <a name="members"></a><span data-ttu-id="f9dbc-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9dbc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9dbc-107">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="f9dbc-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="f9dbc-108">Marcas que identifican el estado actual de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-108">Flags that Identify the current state of Network Monitor.</span></span>



| <span data-ttu-id="f9dbc-109">Value</span><span class="sxs-lookup"><span data-stu-id="f9dbc-109">Value</span></span>                                                                                                                                                                                                                | <span data-ttu-id="f9dbc-110">Significado</span><span class="sxs-lookup"><span data-stu-id="f9dbc-110">Meaning</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="STATIONQUERY_FLAGS_LOADED"></span><span id="stationquery_flags_loaded"></span><dl> <span data-ttu-id="f9dbc-111"><dt>**\_marcas STATIONQUERY \_ cargadas**</dt></span><span class="sxs-lookup"><span data-stu-id="f9dbc-111"><dt>**STATIONQUERY\_FLAGS\_LOADED**</dt></span></span> </dl>                   | <span data-ttu-id="f9dbc-112">El controlador está cargado, pero el kernel no lo es.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-112">The driver is loaded, but the kernel is not.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_RUNNING"></span><span id="stationquery_flags_running"></span><dl> <span data-ttu-id="f9dbc-113"><dt>**marcas de STATIONQUERY en \_ \_ ejecución**</dt></span><span class="sxs-lookup"><span data-stu-id="f9dbc-113"><dt>**STATIONQUERY\_FLAGS\_RUNNING**</dt></span></span> </dl>                | <span data-ttu-id="f9dbc-114">Se carga el controlador, pero no se capturan los datos.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-114">The driver is loaded but not capturing data.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_CAPTURING"></span><span id="stationquery_flags_capturing"></span><dl> <span data-ttu-id="f9dbc-115"><dt>**\_captura de marcas de STATIONQUERY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f9dbc-115"><dt>**STATIONQUERY\_FLAGS\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="f9dbc-116">El controlador está ocupado activamente en una captura.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-116">The driver is actively engaged in a capture.</span></span><br/> |
| <span id="STATIONQUERY_FLAGS_TRANSMITTING"></span><span id="stationquery_flags_transmitting"></span><dl> <span data-ttu-id="f9dbc-117"><dt>**STATIONQUERY \_ marcas de la \_ transmisión**</dt></span><span class="sxs-lookup"><span data-stu-id="f9dbc-117"><dt>**STATIONQUERY\_FLAGS\_TRANSMITTING**</dt></span></span> </dl> | <span data-ttu-id="f9dbc-118">Este marcador está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-118">This flag is obsolete.</span></span><br/>                       |



 

</dd> <dt>

<span data-ttu-id="f9dbc-119">**BCDVerMinor**</span><span class="sxs-lookup"><span data-stu-id="f9dbc-119">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="f9dbc-120">Número de versión secundaria de Monitor de red instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-120">Minor version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="f9dbc-121">**BCDVerMajor**</span><span class="sxs-lookup"><span data-stu-id="f9dbc-121">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="f9dbc-122">Número de versión principal de Monitor de red instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-122">Major version number of Network Monitor installed on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="f9dbc-123">**LicenseNumber**</span><span class="sxs-lookup"><span data-stu-id="f9dbc-123">**LicenseNumber**</span></span>
</dt> <dd>

<span data-ttu-id="f9dbc-124">Número de licencia de software.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-124">Software license number.</span></span>

</dd> <dt>

<span data-ttu-id="f9dbc-125">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="f9dbc-125">**MachineName**</span></span>
</dt> <dd>

<span data-ttu-id="f9dbc-126">Nombre del fabricante del equipo, si existe.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-126">Computer manufacturer name, if any.</span></span>

</dd> <dt>

<span data-ttu-id="f9dbc-127">**UserName**</span><span class="sxs-lookup"><span data-stu-id="f9dbc-127">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="f9dbc-128">Nombre de usuario o identificador de sistema.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-128">User name or system identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f9dbc-129">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f9dbc-129">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f9dbc-130">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-130">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="f9dbc-131">**AdapterAddress**</span><span class="sxs-lookup"><span data-stu-id="f9dbc-131">**AdapterAddress**</span></span>
</dt> <dd>

<span data-ttu-id="f9dbc-132">Dirección NIC.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-132">NIC address.</span></span>

</dd> <dt>

<span data-ttu-id="f9dbc-133">**WMachineName**</span><span class="sxs-lookup"><span data-stu-id="f9dbc-133">**WMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="f9dbc-134">Nombre del equipo Unicode.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-134">Unicode computer name.</span></span> <span data-ttu-id="f9dbc-135">Este miembro se aplica a Monitor de red 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-135">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="f9dbc-136">**WUserName**</span><span class="sxs-lookup"><span data-stu-id="f9dbc-136">**WUserName**</span></span>
</dt> <dd>

<span data-ttu-id="f9dbc-137">Nombre de usuario Unicode.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-137">Unicode user name.</span></span> <span data-ttu-id="f9dbc-138">Este miembro se aplica a Monitor de red 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-138">This member applies to Network Monitor 2.0 or later.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9dbc-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9dbc-139">Remarks</span></span>

<span data-ttu-id="f9dbc-140">La estructura [QUERYTABLE](querytable.md) utiliza una matriz de estas estructuras para proporcionar una lista de los equipos que usan actualmente monitor de red para capturar datos.</span><span class="sxs-lookup"><span data-stu-id="f9dbc-140">An array of these structures is used by the [QUERYTABLE](querytable.md) structure to provide a list of the computers that are currently using Network Monitor to capture data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9dbc-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9dbc-141">Requirements</span></span>



| <span data-ttu-id="f9dbc-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9dbc-142">Requirement</span></span> | <span data-ttu-id="f9dbc-143">Value</span><span class="sxs-lookup"><span data-stu-id="f9dbc-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f9dbc-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9dbc-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f9dbc-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f9dbc-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f9dbc-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9dbc-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f9dbc-147">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9dbc-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f9dbc-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9dbc-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9dbc-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9dbc-149"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9dbc-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9dbc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9dbc-151">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="f9dbc-151">QUERYTABLE</span></span>](querytable.md)
</dt> </dl>

 

 




