---
title: RAS_PPP_ATCP_RESULT estructura (rassapi. h)
description: La \_ estructura de \_ \_ resultados de PPP de PPP de Ras se utiliza para notificar el resultado de una operación de proyección de protocolo AppleTalk para un puerto.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS_PPP_ATCP_RESULT de la estructura RAS
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996498"
---
# <a name="ras_ppp_atcp_result-structure"></a><span data-ttu-id="ff56f-104">\_Estructura de \_ \_ resultado PPP de protocolo ras</span><span class="sxs-lookup"><span data-stu-id="ff56f-104">RAS\_PPP\_ATCP\_RESULT structure</span></span>

<span data-ttu-id="ff56f-105">\[La estructura de **\_ \_ \_ resultados de PPP de protocolo ras** no es compatible con Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="ff56f-105">\[The **RAS\_PPP\_ATCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="ff56f-106">La estructura de **\_ \_ \_ resultados de PPP de PPP de Ras** se utiliza para notificar el resultado de una operación de proyección de protocolo AppleTalk para un puerto.</span><span class="sxs-lookup"><span data-stu-id="ff56f-106">The **RAS\_PPP\_ATCP\_RESULT** structure is used to report the result of an AppleTalk protocol projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff56f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff56f-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="ff56f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff56f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff56f-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="ff56f-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="ff56f-110">Especifica un valor que indica los resultados de la operación de proyección de AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="ff56f-110">Specifies a value that indicates the results of the AppleTalk projection operation.</span></span> <span data-ttu-id="ff56f-111">Un valor de sin \_ error indica que se ha realizado correctamente, en cuyo caso el miembro **wszAddress** es válido.</span><span class="sxs-lookup"><span data-stu-id="ff56f-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="ff56f-112">Si la operación de proyección no se realiza correctamente, **dwError** es un código de error de Winerror. h o Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="ff56f-112">If the projection operation is not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="ff56f-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="ff56f-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="ff56f-114">Especifica una cadena Unicode terminada en null que especifica la dirección IP asignada al cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="ff56f-114">Specifies a null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff56f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff56f-115">Requirements</span></span>



| <span data-ttu-id="ff56f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff56f-116">Requirement</span></span> | <span data-ttu-id="ff56f-117">Value</span><span class="sxs-lookup"><span data-stu-id="ff56f-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ff56f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff56f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ff56f-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ff56f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ff56f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff56f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ff56f-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ff56f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ff56f-122">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ff56f-122">End of client support</span></span><br/>    | <span data-ttu-id="ff56f-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff56f-123">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="ff56f-124">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="ff56f-124">End of server support</span></span><br/>    | <span data-ttu-id="ff56f-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff56f-125">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="ff56f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff56f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff56f-127"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff56f-127"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff56f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff56f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff56f-129">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="ff56f-129">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="ff56f-130">Estructuras de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="ff56f-130">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="ff56f-131">**\_resultado de \_ proyección \_ PPP de Ras**</span><span class="sxs-lookup"><span data-stu-id="ff56f-131">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





