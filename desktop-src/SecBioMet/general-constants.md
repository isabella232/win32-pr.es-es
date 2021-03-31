---
title: Constantes generales (Winbio \_ Types. h)
description: Especifique la longitud máxima del SID, los identificadores, los identificadores, la longitud máxima de la cadena y el tamaño máximo del búfer de muestra.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996389"
---
# <a name="general-constants-winbio_typesh"></a><span data-ttu-id="6c4db-103">Constantes generales (Winbio \_ Types. h)</span><span class="sxs-lookup"><span data-stu-id="6c4db-103">General Constants (Winbio\_types.h)</span></span>

<span data-ttu-id="6c4db-104">En el Plataforma de biometría de Windows se usan las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="6c4db-104">The following constants are used throughout the Windows Biometric Framework.</span></span>



| <span data-ttu-id="6c4db-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="6c4db-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="6c4db-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c4db-106">Description</span></span>                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <span data-ttu-id="6c4db-107"><dt>**\_tamaño máximo de \_ SID \_ de seguridad**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4db-107"><dt>**SECURITY\_MAX\_SID\_SIZE**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="6c4db-108">La longitud máxima de un valor de identificador de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="6c4db-108">The maximum length of a security identifier (SID) value.</span></span> <span data-ttu-id="6c4db-109">Actualmente es 68.</span><span class="sxs-lookup"><span data-stu-id="6c4db-109">Currently this is 68.</span></span><br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <span data-ttu-id="6c4db-110"><dt>**\_identificador de unidad de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4db-110"><dt>**WINBIO\_UNIT\_ID**</dt></span></span> </dl>                                                                                                                | <span data-ttu-id="6c4db-111">Número de identificación de una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="6c4db-111">ID number of a biometric unit.</span></span><br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <span data-ttu-id="6c4db-112"><dt>**\_identificador de sesión de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4db-112"><dt>**WINBIO\_SESSION\_HANDLE**</dt></span></span> </dl>                                                                                           | <span data-ttu-id="6c4db-113">Entero largo sin signo que contiene el identificador de una sesión biométrica abierta.</span><span class="sxs-lookup"><span data-stu-id="6c4db-113">An unsigned long integer that contains the handle for an open biometric session.</span></span><br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <span data-ttu-id="6c4db-114"><dt>**\_identificador del marco de WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4db-114"><dt>**WINBIO\_FRAMEWORK\_HANDLE**</dt></span></span> </dl>                                                                                     | <span data-ttu-id="6c4db-115">Entero largo sin signo que contiene el identificador de una sesión de marco abierta.</span><span class="sxs-lookup"><span data-stu-id="6c4db-115">An unsigned long integer that contains the handle for an open framework session.</span></span><br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <span data-ttu-id="6c4db-116"><dt>**\_UUID WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4db-116"><dt>**WINBIO\_UUID**</dt></span></span> </dl>                                                                                                                          | <span data-ttu-id="6c4db-117">Un GUID.</span><span class="sxs-lookup"><span data-stu-id="6c4db-117">A GUID.</span></span><br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <span data-ttu-id="6c4db-118"><dt>**\_cadena WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4db-118"><dt>**WINBIO\_STRING**</dt></span></span> </dl>                                                                                                                    | <span data-ttu-id="6c4db-119">Matriz de bytes que contiene una cadena Unicode terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="6c4db-119">A byte array that contains a null-terminated Unicode string.</span></span><br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <span data-ttu-id="6c4db-120"><dt>**WINBIO \_ \_ \_ longitud máxima de cadena**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4db-120"><dt>**WINBIO\_MAX\_STRING\_LEN** </dt></span></span> </dl>                                                                                       | <span data-ttu-id="6c4db-121">La longitud máxima de un valor de **\_ cadena de WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="6c4db-121">The maximum length of a **WINBIO\_STRING** value.</span></span> <span data-ttu-id="6c4db-122">Actualmente es 256.</span><span class="sxs-lookup"><span data-stu-id="6c4db-122">Currently this is 256.</span></span><br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <span data-ttu-id="6c4db-123"><dt>**WINBIO \_ \_ \_ \_ Tamaño máximo de búfer de ejemplo**</dt> <dt>0x7FFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="6c4db-123"><dt>**WINBIO\_MAX\_SAMPLE\_BUFFER\_SIZE**</dt> <dt>0x7FFFFFFF</dt></span></span> </dl> | <span data-ttu-id="6c4db-124">Número máximo de bytes en una captura de datos biométricos única.</span><span class="sxs-lookup"><span data-stu-id="6c4db-124">The maximum number of bytes in a single biometric data capture.</span></span><br/>                  |



## <a name="requirements"></a><span data-ttu-id="6c4db-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c4db-125">Requirements</span></span>



| <span data-ttu-id="6c4db-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c4db-126">Requirement</span></span> | <span data-ttu-id="6c4db-127">Value</span><span class="sxs-lookup"><span data-stu-id="6c4db-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c4db-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c4db-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6c4db-129">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c4db-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="6c4db-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c4db-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6c4db-131">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c4db-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6c4db-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c4db-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c4db-133"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c4db-133"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c4db-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c4db-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4db-135">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="6c4db-135">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





