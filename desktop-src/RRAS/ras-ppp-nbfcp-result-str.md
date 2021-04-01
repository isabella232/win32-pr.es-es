---
title: RAS_PPP_NBFCP_RESULT estructura (rassapi. h)
description: La \_ estructura de resultados NBFCP de PPP de Ras \_ \_ se usa para informar del resultado de una operación de proyección de PPP NetBEUI Framer (NBF) para un puerto.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT de la estructura RAS
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150392"
---
# <a name="ras_ppp_nbfcp_result-structure"></a><span data-ttu-id="04ca0-104">\_Estructura de \_ resultado de NBFCP de PPP de Ras \_</span><span class="sxs-lookup"><span data-stu-id="04ca0-104">RAS\_PPP\_NBFCP\_RESULT structure</span></span>

<span data-ttu-id="04ca0-105">\[La estructura de **\_ \_ \_ resultados NBFCP de PPP de Ras** no es compatible con Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="04ca0-105">\[The **RAS\_PPP\_NBFCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="04ca0-106">La estructura de **\_ \_ \_ resultados NBFCP de PPP de Ras** se usa para informar del resultado de una operación de proyección de PPP NetBEUI Framer (NBF) para un puerto.</span><span class="sxs-lookup"><span data-stu-id="04ca0-106">The **RAS\_PPP\_NBFCP\_RESULT** structure is used to report the result of a PPP NetBEUI Framer (NBF) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ca0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04ca0-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="04ca0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="04ca0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="04ca0-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="04ca0-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="04ca0-110">Indica los resultados de la operación de proyección de NBF.</span><span class="sxs-lookup"><span data-stu-id="04ca0-110">Indicates the results of the NBF projection operation.</span></span> <span data-ttu-id="04ca0-111">Un valor de sin \_ error indica que se ha realizado correctamente, en cuyo caso el miembro **wszWksta** contiene el nombre del equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="04ca0-111">A value of NO\_ERROR indicates success, in which case, the **wszWksta** member contains the name of the remote computer.</span></span> <span data-ttu-id="04ca0-112">Si la operación de proyección no se realiza correctamente, **dwError** es un código de error de Winerror. h o Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="04ca0-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="04ca0-113">**dwNetBiosError**</span><span class="sxs-lookup"><span data-stu-id="04ca0-113">**dwNetBiosError**</span></span>
</dt> <dd>

<span data-ttu-id="04ca0-114">Omitir este miembro en el servidor; solo es relevante en el cliente.</span><span class="sxs-lookup"><span data-stu-id="04ca0-114">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="04ca0-115">**szName**</span><span class="sxs-lookup"><span data-stu-id="04ca0-115">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="04ca0-116">Omitir este miembro en el servidor; solo es relevante en el cliente.</span><span class="sxs-lookup"><span data-stu-id="04ca0-116">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="04ca0-117">**wszWksta**</span><span class="sxs-lookup"><span data-stu-id="04ca0-117">**wszWksta**</span></span>
</dt> <dd>

<span data-ttu-id="04ca0-118">Una cadena Unicode terminada en null que especifica el nombre NetBIOS de la estación de trabajo del cliente RAS.</span><span class="sxs-lookup"><span data-stu-id="04ca0-118">A null-terminated Unicode string that specifies the NetBIOS name of the RAS client workstation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04ca0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04ca0-119">Requirements</span></span>



| <span data-ttu-id="04ca0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ca0-120">Requirement</span></span> | <span data-ttu-id="04ca0-121">Value</span><span class="sxs-lookup"><span data-stu-id="04ca0-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="04ca0-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ca0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="04ca0-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="04ca0-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="04ca0-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ca0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="04ca0-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04ca0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="04ca0-126">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="04ca0-126">End of client support</span></span><br/>    | <span data-ttu-id="04ca0-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="04ca0-127">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="04ca0-128">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="04ca0-128">End of server support</span></span><br/>    | <span data-ttu-id="04ca0-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04ca0-129">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="04ca0-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04ca0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="04ca0-131"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="04ca0-131"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ca0-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="04ca0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ca0-133">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="04ca0-133">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="04ca0-134">Estructuras de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="04ca0-134">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="04ca0-135">**\_Puerto ras \_ 1**</span><span class="sxs-lookup"><span data-stu-id="04ca0-135">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="04ca0-136">**\_resultado de \_ proyección \_ PPP de Ras**</span><span class="sxs-lookup"><span data-stu-id="04ca0-136">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="04ca0-137">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="04ca0-137">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





