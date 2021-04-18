---
title: RAS_SERVER_0 estructura (rassapi. h)
description: '\_ \_ La función RasAdminServerGetInfo utiliza la estructura del servidor RAS 0 para devolver información acerca de los puertos configurados en un servidor RAS.'
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0 de la estructura RAS
- PRAS_SERVER_0 de puntero de estructura RAS
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651408"
---
# <a name="ras_server_0-structure"></a><span data-ttu-id="5a320-105">\_Estructura del servidor RAS \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a320-105">RAS\_SERVER\_0 structure</span></span>

<span data-ttu-id="5a320-106">\[La estructura del **\_ servidor RAS \_ 0** no es compatible con Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="5a320-106">\[The **RAS\_SERVER\_0** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="5a320-107">La función [**RasAdminServerGetInfo**](rasadminservergetinfo.md) utiliza la estructura del **\_ servidor RAS \_ 0** para devolver información acerca de los puertos configurados en un servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="5a320-107">The **RAS\_SERVER\_0** structure is used by the [**RasAdminServerGetInfo**](rasadminservergetinfo.md) function to return information about the ports configured on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a320-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a320-108">Syntax</span></span>


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a><span data-ttu-id="5a320-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a320-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="5a320-110">**TotalPorts**</span><span class="sxs-lookup"><span data-stu-id="5a320-110">**TotalPorts**</span></span>
</dt> <dd>

<span data-ttu-id="5a320-111">Especifica el número total de puertos configurados en el servidor RAS que están disponibles para que los clientes remotos se conecten a.</span><span class="sxs-lookup"><span data-stu-id="5a320-111">Specifies the total number of ports configured on the RAS server that are available for remote clients to connect to.</span></span> <span data-ttu-id="5a320-112">Por ejemplo, si el número total de puertos configurados para el acceso telefónico a un servidor es cuatro, pero uno de los puertos se está usando actualmente para el marcado, **TotalPorts** es tres.</span><span class="sxs-lookup"><span data-stu-id="5a320-112">For example, if the total number of ports configured for dialing in to a server is four, but one of the ports is currently in use for dialing out, **TotalPorts** is three.</span></span>

</dd> <dt>

<span data-ttu-id="5a320-113">**PortsInUse**</span><span class="sxs-lookup"><span data-stu-id="5a320-113">**PortsInUse**</span></span>
</dt> <dd>

<span data-ttu-id="5a320-114">Especifica el número de puertos actualmente en uso por los clientes remotos.</span><span class="sxs-lookup"><span data-stu-id="5a320-114">Specifies the number of ports currently in use by remote clients.</span></span>

</dd> <dt>

<span data-ttu-id="5a320-115">**RasVersion**</span><span class="sxs-lookup"><span data-stu-id="5a320-115">**RasVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5a320-116">Especifica la versión del servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="5a320-116">Specifies the version of the RAS server.</span></span> <span data-ttu-id="5a320-117">Use esta información para realizar una acción específica de la versión.</span><span class="sxs-lookup"><span data-stu-id="5a320-117">Use this information to take version-specific action.</span></span> <span data-ttu-id="5a320-118">Este miembro es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5a320-118">This member is one of the following values.</span></span>



| <span data-ttu-id="5a320-119">Value</span><span class="sxs-lookup"><span data-stu-id="5a320-119">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="5a320-120">Significado</span><span class="sxs-lookup"><span data-stu-id="5a320-120">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <span data-ttu-id="5a320-121"><dt>**RASDOWNLEVEL**</dt></span><span class="sxs-lookup"><span data-stu-id="5a320-121"><dt>**RASDOWNLEVEL**</dt></span></span> </dl>              | <span data-ttu-id="5a320-122">Indica un servidor RAS de LAN Manager versión 1,0.</span><span class="sxs-lookup"><span data-stu-id="5a320-122">Indicates a LAN Manager version 1.0 RAS server.</span></span><br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <span data-ttu-id="5a320-123"><dt>**RASADMIN \_ 35**</dt></span><span class="sxs-lookup"><span data-stu-id="5a320-123"><dt>**RASADMIN\_35**</dt></span></span> </dl>                | <span data-ttu-id="5a320-124">Indica un servidor o cliente RAS de Windows NT Server 3,51 y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="5a320-124">Indicates a Windows NT Server 3.51 and earlier RAS server or client.</span></span><br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <span data-ttu-id="5a320-125"><dt>**RASADMIN \_ actual**</dt></span><span class="sxs-lookup"><span data-stu-id="5a320-125"><dt>**RASADMIN\_CURRENT**</dt></span></span> </dl> | <span data-ttu-id="5a320-126">Indica un servidor o cliente RAS de Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="5a320-126">Indicates a Windows NT 4.0 RAS server or client.</span></span><br/>                     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a320-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a320-127">Requirements</span></span>



| <span data-ttu-id="5a320-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a320-128">Requirement</span></span> | <span data-ttu-id="5a320-129">Value</span><span class="sxs-lookup"><span data-stu-id="5a320-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a320-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a320-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5a320-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5a320-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5a320-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a320-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5a320-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a320-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5a320-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5a320-134">End of client support</span></span><br/>    | <span data-ttu-id="5a320-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5a320-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="5a320-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5a320-136">End of server support</span></span><br/>    | <span data-ttu-id="5a320-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5a320-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="5a320-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a320-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a320-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a320-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a320-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a320-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a320-141">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="5a320-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="5a320-142">Estructuras de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="5a320-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="5a320-143">**RasAdminServerGetInfo**</span><span class="sxs-lookup"><span data-stu-id="5a320-143">**RasAdminServerGetInfo**</span></span>](rasadminservergetinfo.md)
</dt> </dl>

 

 





