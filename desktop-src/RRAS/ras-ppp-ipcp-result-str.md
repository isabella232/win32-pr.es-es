---
title: RAS_PPP_IPCP_RESULT estructura (rassapi. h)
description: La \_ estructura de \_ resultados de PPP de PPP de Ras \_ se utiliza para notificar el resultado de una operación de proyección de protocolo de Internet (IP) PPP para un puerto.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS_PPP_IPCP_RESULT de la estructura RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534264"
---
# <a name="ras_ppp_ipcp_result-structure"></a><span data-ttu-id="8c170-104">\_Estructura de resultados de ppp ppp \_ IPCP \_</span><span class="sxs-lookup"><span data-stu-id="8c170-104">RAS\_PPP\_IPCP\_RESULT structure</span></span>

<span data-ttu-id="8c170-105">\[La estructura de **\_ \_ \_ resultados de PPP de Ras** no es compatible con Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="8c170-105">\[The **RAS\_PPP\_IPCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="8c170-106">La estructura de **\_ \_ \_ resultados de PPP de PPP de Ras** se utiliza para notificar el resultado de una operación de proyección de protocolo de Internet (IP) PPP para un puerto.</span><span class="sxs-lookup"><span data-stu-id="8c170-106">The **RAS\_PPP\_IPCP\_RESULT** structure is used to report the result of a PPP Internet Protocol (IP) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c170-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c170-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="8c170-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c170-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8c170-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="8c170-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="8c170-110">Indica los resultados de la operación de proyección IP.</span><span class="sxs-lookup"><span data-stu-id="8c170-110">Indicates the results of the IP projection operation.</span></span> <span data-ttu-id="8c170-111">Un valor de sin \_ error indica que se ha realizado correctamente, en cuyo caso el miembro **wszAddress** es válido.</span><span class="sxs-lookup"><span data-stu-id="8c170-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="8c170-112">Si la operación de proyección no se realiza correctamente, **dwError** es un código de error de Winerror. h o Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="8c170-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="8c170-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="8c170-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8c170-114">Una cadena Unicode terminada en null que especifica la dirección IP asignada al cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="8c170-114">A null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span> <span data-ttu-id="8c170-115">Esta cadena tiene el formato \*\*\*\*.\*\* _b_\* _._ *_c_*_._ \* _d_.</span><span class="sxs-lookup"><span data-stu-id="8c170-115">This string has the form *a\***.**_b_*_._*_c_*_._\*_d_.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c170-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c170-116">Requirements</span></span>



| <span data-ttu-id="8c170-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c170-117">Requirement</span></span> | <span data-ttu-id="8c170-118">Value</span><span class="sxs-lookup"><span data-stu-id="8c170-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8c170-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c170-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8c170-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8c170-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8c170-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c170-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8c170-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8c170-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8c170-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8c170-123">End of client support</span></span><br/>    | <span data-ttu-id="8c170-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c170-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="8c170-125">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8c170-125">End of server support</span></span><br/>    | <span data-ttu-id="8c170-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8c170-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="8c170-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c170-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c170-128"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c170-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c170-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c170-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c170-130">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="8c170-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="8c170-131">Estructuras de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="8c170-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="8c170-132">**\_Puerto ras \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8c170-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="8c170-133">**\_resultado de \_ proyección \_ PPP de Ras**</span><span class="sxs-lookup"><span data-stu-id="8c170-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="8c170-134">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="8c170-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





