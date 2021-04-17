---
title: RAS_USER_0 estructura (rassapi. h)
description: La \_ \_ estructura de usuario de Ras 0 se usa en las funciones RasAdminUserSetInfo y RasAdminUserGetInfo para especificar información sobre un usuario.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 de la estructura RAS
- PRAS_USER_0 de puntero de estructura RAS
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534102"
---
# <a name="ras_user_0-structure"></a><span data-ttu-id="2ebbc-105">Estructura del usuario de RAS \_ \_ 0</span><span class="sxs-lookup"><span data-stu-id="2ebbc-105">RAS\_USER\_0 structure</span></span>

<span data-ttu-id="2ebbc-106">\[Esta versión de la estructura de **usuario de Ras \_ \_ 0** no es compatible con Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-106">\[This version of the **RAS\_USER\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="2ebbc-107">En su lugar, use el [**\_ usuario ras \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) más reciente definido en mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="2ebbc-107">Use the newer [**RAS\_USER\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="2ebbc-108">La estructura de **usuario de Ras \_ \_ 0** se usa en las funciones [**RasAdminUserSetInfo**](rasadminusersetinfo.md) y [**RasAdminUserGetInfo**](rasadminusergetinfo.md) para especificar información sobre un usuario.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-108">The **RAS\_USER\_0** structure is used in the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) and [**RasAdminUserGetInfo**](rasadminusergetinfo.md) functions to specify information about a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebbc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ebbc-109">Syntax</span></span>


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a><span data-ttu-id="2ebbc-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ebbc-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="2ebbc-111">**bfPrivilege**</span><span class="sxs-lookup"><span data-stu-id="2ebbc-111">**bfPrivilege**</span></span>
</dt> <dd>

<span data-ttu-id="2ebbc-112">Un conjunto de marcadores de bits que especifican los privilegios RAS del usuario.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-112">A set of bit flags that specify the RAS privileges of the user.</span></span> <span data-ttu-id="2ebbc-113">Este miembro puede ser una combinación de la \_ marca RASPRIV DialinPrivilege y una de las marcas de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-113">This member can be a combination of the RASPRIV\_DialinPrivilege flag and one of the call-back flags.</span></span> <span data-ttu-id="2ebbc-114">Use la máscara de CallbackType de RASPRIV \_ para identificar el tipo de privilegio de devolución de llamada que se proporciona al usuario.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-114">Use the RASPRIV\_CallbackType mask to identify the type of call-back privilege provided to the user.</span></span> <span data-ttu-id="2ebbc-115">Se definen las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-115">The following flags are defined.</span></span>



| <span data-ttu-id="2ebbc-116">Value</span><span class="sxs-lookup"><span data-stu-id="2ebbc-116">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="2ebbc-117">Significado</span><span class="sxs-lookup"><span data-stu-id="2ebbc-117">Meaning</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <span data-ttu-id="2ebbc-118"><dt>**RASPRIV \_ Nocallback**</dt></span><span class="sxs-lookup"><span data-stu-id="2ebbc-118"><dt>**RASPRIV\_NoCallback**</dt></span></span> </dl>                             | <span data-ttu-id="2ebbc-119">El usuario no tiene ningún privilegio de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-119">The user has no call-back privilege.</span></span><br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <span data-ttu-id="2ebbc-120"><dt>**RASPRIV \_ AdminSetCallback**</dt></span><span class="sxs-lookup"><span data-stu-id="2ebbc-120"><dt>**RASPRIV\_AdminSetCallback**</dt></span></span> </dl>     | <span data-ttu-id="2ebbc-121">La cuenta de usuario está configurada para que el administrador establezca el número de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-121">The user account is configured to have the administrator set the call-back number.</span></span><br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <span data-ttu-id="2ebbc-122"><dt>**RASPRIV \_ CallerSetCallback**</dt></span><span class="sxs-lookup"><span data-stu-id="2ebbc-122"><dt>**RASPRIV\_CallerSetCallback**</dt></span></span> </dl> | <span data-ttu-id="2ebbc-123">El usuario remoto puede especificar un número de teléfono de devolución de llamada al llamar a.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-123">The remote user can specify a call-back phone number when dialing in.</span></span><br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <span data-ttu-id="2ebbc-124"><dt>**RASPRIV \_ DialinPrivilege**</dt></span><span class="sxs-lookup"><span data-stu-id="2ebbc-124"><dt>**RASPRIV\_DialinPrivilege**</dt></span></span> </dl>         | <span data-ttu-id="2ebbc-125">El usuario tiene permiso para llamar a este servidor.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-125">The user has permission to dial in to this server.</span></span><br/>                                 |



 

<span data-ttu-id="2ebbc-126">Especifique una de las marcas de devolución de llamada en la llamada a la función [**RasAdminUserSetInfo**](rasadminusersetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2ebbc-126">Specify one of the call-back flags in the call to the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2ebbc-127">**szPhoneNumber**</span><span class="sxs-lookup"><span data-stu-id="2ebbc-127">**szPhoneNumber**</span></span>
</dt> <dd>

<span data-ttu-id="2ebbc-128">Una cadena Unicode terminada en null que especifica el número de teléfono de devolución de llamada para el usuario.</span><span class="sxs-lookup"><span data-stu-id="2ebbc-128">A null-terminated Unicode string that specifies the call-back phone number for the user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ebbc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ebbc-129">Requirements</span></span>



| <span data-ttu-id="2ebbc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ebbc-130">Requirement</span></span> | <span data-ttu-id="2ebbc-131">Value</span><span class="sxs-lookup"><span data-stu-id="2ebbc-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebbc-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ebbc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2ebbc-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2ebbc-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2ebbc-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ebbc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2ebbc-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ebbc-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2ebbc-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2ebbc-136">End of client support</span></span><br/>    | <span data-ttu-id="2ebbc-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2ebbc-137">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="2ebbc-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2ebbc-138">End of server support</span></span><br/>    | <span data-ttu-id="2ebbc-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ebbc-139">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="2ebbc-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ebbc-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ebbc-141"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ebbc-141"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ebbc-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ebbc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ebbc-143">Introducción al servicio de acceso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="2ebbc-143">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="2ebbc-144">Estructuras de administración del servidor RAS</span><span class="sxs-lookup"><span data-stu-id="2ebbc-144">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="2ebbc-145">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="2ebbc-145">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="2ebbc-146">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="2ebbc-146">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

 





