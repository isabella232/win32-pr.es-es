---
description: Define los valores que determinan cómo capturar la credencial de una cuenta de servicio administrada de grupo (gMSA).
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: Enumeración CRED_FETCH (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002472"
---
# <a name="cred_fetch-enumeration"></a><span data-ttu-id="884d6-103">Enumeración de recopilación de CREDENCIALes \_</span><span class="sxs-lookup"><span data-stu-id="884d6-103">CRED\_FETCH enumeration</span></span>

<span data-ttu-id="884d6-104">Define los valores que determinan cómo capturar la credencial de una cuenta de servicio administrada de grupo (gMSA).</span><span class="sxs-lookup"><span data-stu-id="884d6-104">Defines values that determine how to fetch the credential of a Group Managed Service Account (gMSA).</span></span>

## <a name="syntax"></a><span data-ttu-id="884d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="884d6-105">Syntax</span></span>


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a><span data-ttu-id="884d6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="884d6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="884d6-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span><span class="sxs-lookup"><span data-stu-id="884d6-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span></span>
</dt> <dd>

<span data-ttu-id="884d6-108">Significa que el sistema operativo debe intentar primero recuperar la contraseña de la caché local.</span><span class="sxs-lookup"><span data-stu-id="884d6-108">Signifies that the operating system should first attempt to retrieve the password from the local cache.</span></span> <span data-ttu-id="884d6-109">Si es el momento de capturar la contraseña, el sistema operativo debe ponerse en contacto con un controlador de dominio para la contraseña.</span><span class="sxs-lookup"><span data-stu-id="884d6-109">If it is time to fetch the password, then the operating system should contact a domain controller for the password.</span></span> <span data-ttu-id="884d6-110">Si se produce un error, devuelva cualquier contraseña almacenada en caché con el valor de estado correcto.</span><span class="sxs-lookup"><span data-stu-id="884d6-110">If that fails, then return any cached passwords with the status value of success.</span></span>

</dd> <dt>

<span data-ttu-id="884d6-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span><span class="sxs-lookup"><span data-stu-id="884d6-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span></span>
</dt> <dd>

<span data-ttu-id="884d6-112">Devuelve la credencial DPAPI local al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="884d6-112">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="884d6-113">Los [*proveedores de compatibilidad para seguridad*](/windows/desktop/SecGloss/s-gly) (SSP) no suelen requerir el uso de esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="884d6-113">[*Security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs) generally would not require the use of this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="884d6-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span><span class="sxs-lookup"><span data-stu-id="884d6-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span></span>
</dt> <dd>

<span data-ttu-id="884d6-115">Obliga al sistema operativo a intentar leer la contraseña del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="884d6-115">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="884d6-116">Durante el tiempo de sustitución de contraseña, la contraseña puede haber cambiado en el controlador de dominio y en otros hosts miembros, pero el host miembro gMSA reconoce la contraseña como todavía válida.</span><span class="sxs-lookup"><span data-stu-id="884d6-116">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="884d6-117">Esto puede ocurrir debido a problemas de sesgo del reloj entre distintos controladores de dominio.</span><span class="sxs-lookup"><span data-stu-id="884d6-117">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="884d6-118">Cuando se especifica este valor, el sistema operativo determina si puede haber un posible cambio de contraseña debido al sesgo del reloj y, en caso afirmativo, recupera la contraseña.</span><span class="sxs-lookup"><span data-stu-id="884d6-118">When this value is specified, the operating system determines if there could be a possible password change due to clock skew, and if so, retrieves the password.</span></span> <span data-ttu-id="884d6-119">De lo contrario, se devuelve la credencial almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="884d6-119">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="884d6-120">Si no hay ninguna credencial almacenada en caché, el sistema operativo intenta obtener una del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="884d6-120">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="884d6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="884d6-121">Requirements</span></span>



| <span data-ttu-id="884d6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="884d6-122">Requirement</span></span> | <span data-ttu-id="884d6-123">Value</span><span class="sxs-lookup"><span data-stu-id="884d6-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="884d6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="884d6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="884d6-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="884d6-125">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="884d6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="884d6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="884d6-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="884d6-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="884d6-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="884d6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="884d6-129"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="884d6-129"><dt>Secpkg.h</dt></span></span> </dl> |



 

