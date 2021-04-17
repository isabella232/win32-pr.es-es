---
description: Contiene los parámetros de configuración de EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: EAPOL_INTF_PARAMS estructura (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667663"
---
# <a name="eapol_intf_params-structure"></a><span data-ttu-id="8890f-103">Estructura de los parámetros de Intf de EAPOL \_ \_</span><span class="sxs-lookup"><span data-stu-id="8890f-103">EAPOL\_INTF\_PARAMS structure</span></span>

<span data-ttu-id="8890f-104">\[**EAPOL \_ Los \_ parámetros de Intf** ya no se admiten a partir de Windows Vista y windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8890f-104">\[**EAPOL\_INTF\_PARAMS** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="8890f-105">En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar.</span><span class="sxs-lookup"><span data-stu-id="8890f-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="8890f-106">Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="8890f-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="8890f-107">Contiene los parámetros de configuración de EAPOL.</span><span class="sxs-lookup"><span data-stu-id="8890f-107">Contains EAPOL configuration parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="8890f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8890f-108">Syntax</span></span>


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a><span data-ttu-id="8890f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8890f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8890f-110">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="8890f-110">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8890f-111">Versión del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="8890f-111">Version of the caller.</span></span> <span data-ttu-id="8890f-112">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="8890f-112">Default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="8890f-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="8890f-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="8890f-114">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="8890f-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="8890f-115">**dwEapFlags**</span><span class="sxs-lookup"><span data-stu-id="8890f-115">**dwEapFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8890f-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8890f-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8890f-117">**dwEapType**</span><span class="sxs-lookup"><span data-stu-id="8890f-117">**dwEapType**</span></span>
</dt> <dd>

<span data-ttu-id="8890f-118">Tipo de extensión EAP que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="8890f-118">The EAP extension type to be used.</span></span> <span data-ttu-id="8890f-119">Establézcalo en 0x00000013 para EAP-TLS y 0x00000026 para PEAP.</span><span class="sxs-lookup"><span data-stu-id="8890f-119">Set to 0x00000013 for EAP-TLS and 0x00000026 for PEAP.</span></span>

</dd> <dt>

<span data-ttu-id="8890f-120">**dwSizeOfSSID**</span><span class="sxs-lookup"><span data-stu-id="8890f-120">**dwSizeOfSSID**</span></span>
</dt> <dd>

<span data-ttu-id="8890f-121">Tamaño del identificador de red.</span><span class="sxs-lookup"><span data-stu-id="8890f-121">Size of network identifier.</span></span>

</dd> <dt>

<span data-ttu-id="8890f-122">**bSSID**</span><span class="sxs-lookup"><span data-stu-id="8890f-122">**bSSID**</span></span>
</dt> <dd>

<span data-ttu-id="8890f-123">Identificador de red.</span><span class="sxs-lookup"><span data-stu-id="8890f-123">Network identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8890f-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8890f-124">Remarks</span></span>

<span data-ttu-id="8890f-125">El archivo de encabezado wzcsapi. h no está disponible en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8890f-125">The header file wzcsapi.h is not available in the Windows SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="8890f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8890f-126">Requirements</span></span>



| <span data-ttu-id="8890f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8890f-127">Requirement</span></span> | <span data-ttu-id="8890f-128">Value</span><span class="sxs-lookup"><span data-stu-id="8890f-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8890f-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8890f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8890f-130">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8890f-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8890f-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8890f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8890f-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8890f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8890f-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8890f-133">End of client support</span></span><br/>    | <span data-ttu-id="8890f-134">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="8890f-134">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="8890f-135">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8890f-135">End of server support</span></span><br/>    | <span data-ttu-id="8890f-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8890f-136">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="8890f-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8890f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="8890f-138"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8890f-138"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




