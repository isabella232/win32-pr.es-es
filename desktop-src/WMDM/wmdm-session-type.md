---
title: Enumeración WMDM_SESSION_TYPE
description: El tipo \_ de \_ enumeración de tipo de sesión WMDM define el tipo de sesión.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- Enumeración WMDM_SESSION_TYPE Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698736"
---
# <a name="wmdm_session_type-enumeration"></a><span data-ttu-id="2ca70-104">\_Enumeración de tipo de sesión WMDM \_</span><span class="sxs-lookup"><span data-stu-id="2ca70-104">WMDM\_SESSION\_TYPE enumeration</span></span>

<span data-ttu-id="2ca70-105">El tipo de enumeración de **\_ \_ tipo de sesión WMDM** define el tipo de sesión.</span><span class="sxs-lookup"><span data-stu-id="2ca70-105">The **WMDM\_SESSION\_TYPE** enumeration type defines the session type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca70-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ca70-106">Syntax</span></span>


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="2ca70-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="2ca70-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2ca70-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**sesión de WMDM \_ \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="2ca70-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM\_SESSION\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="2ca70-109">La sesión no está definida.</span><span class="sxs-lookup"><span data-stu-id="2ca70-109">The session is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="2ca70-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**\_ \_ transferencia de sesión \_ de WMDM al \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="2ca70-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM\_SESSION\_TRANSFER\_TO\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="2ca70-111">La sesión se define como la transferencia de datos al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ca70-111">The session is defined as transferring data to the device.</span></span>

</dd> <dt>

<span data-ttu-id="2ca70-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_ \_ transferencia de sesión \_ de WMDM desde el \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="2ca70-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**WMDM\_SESSION\_TRANSFER\_FROM\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="2ca70-113">La sesión se define como la transferencia de datos desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ca70-113">The session is defined as transferring data from the device.</span></span>

</dd> <dt>

<span data-ttu-id="2ca70-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**\_eliminación de sesión de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="2ca70-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM\_SESSION\_DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="2ca70-115">La sesión se define como la eliminación de datos.</span><span class="sxs-lookup"><span data-stu-id="2ca70-115">The session is defined as deleting data.</span></span>

</dd> <dt>

<span data-ttu-id="2ca70-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**sesión de WMDM \_ \_ personalizada**</span><span class="sxs-lookup"><span data-stu-id="2ca70-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM\_SESSION\_CUSTOM**</span></span>
</dt> <dd>

<span data-ttu-id="2ca70-117">La sesión se define como una sesión personalizada.</span><span class="sxs-lookup"><span data-stu-id="2ca70-117">The session is defined as a custom session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ca70-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ca70-118">Requirements</span></span>



| <span data-ttu-id="2ca70-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca70-119">Requirement</span></span> | <span data-ttu-id="2ca70-120">Value</span><span class="sxs-lookup"><span data-stu-id="2ca70-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca70-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ca70-121">Header</span></span><br/> | <dl> <span data-ttu-id="2ca70-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2ca70-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ca70-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ca70-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca70-124">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="2ca70-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





