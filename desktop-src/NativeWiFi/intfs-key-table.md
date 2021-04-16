---
description: Contiene la tabla de información clave para todas las interfaces LAN inalámbricas administradas por el servicio de configuración inalámbrica.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: INTFS_KEY_TABLE estructura (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666582"
---
# <a name="intfs_key_table-structure"></a><span data-ttu-id="41537-103">Estructura de la tabla de claves de INTFS \_ \_</span><span class="sxs-lookup"><span data-stu-id="41537-103">INTFS\_KEY\_TABLE structure</span></span>

<span data-ttu-id="41537-104">\[**INTFS \_ La \_ tabla de claves** ya no se admite en Windows Vista y windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="41537-104">\[**INTFS\_KEY\_TABLE** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="41537-105">En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar.</span><span class="sxs-lookup"><span data-stu-id="41537-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="41537-106">Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="41537-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="41537-107">La estructura de la **\_ \_ tabla de claves de INTFS** contiene la tabla de información de claves para todas las interfaces de LAN inalámbricas administradas por el servicio de configuración inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="41537-107">The **INTFS\_KEY\_TABLE** structure contains the table of key information for all wireless LAN interfaces managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="41537-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41537-108">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a><span data-ttu-id="41537-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="41537-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="41537-110">**dwNumIntfs**</span><span class="sxs-lookup"><span data-stu-id="41537-110">**dwNumIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="41537-111">Número total de interfaces.</span><span class="sxs-lookup"><span data-stu-id="41537-111">Total number of interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="41537-112">**pIntfs**</span><span class="sxs-lookup"><span data-stu-id="41537-112">**pIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="41537-113">Puntero a la estructura de [**\_ \_ entrada de la clave Intf**](intf-key-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="41537-113">Pointer to the [**INTF\_KEY\_ENTRY**](intf-key-entry.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41537-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41537-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="41537-115">El archivo de encabezado *wzcsapi. h* no está disponible en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="41537-115">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41537-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41537-116">Requirements</span></span>



| <span data-ttu-id="41537-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="41537-117">Requirement</span></span> | <span data-ttu-id="41537-118">Value</span><span class="sxs-lookup"><span data-stu-id="41537-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="41537-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41537-119">Minimum supported client</span></span><br/> | <span data-ttu-id="41537-120">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="41537-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="41537-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41537-121">Minimum supported server</span></span><br/> | <span data-ttu-id="41537-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="41537-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="41537-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="41537-123">End of client support</span></span><br/>    | <span data-ttu-id="41537-124">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="41537-124">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="41537-125">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="41537-125">End of server support</span></span><br/>    | <span data-ttu-id="41537-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="41537-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="41537-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41537-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="41537-128"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="41537-128"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




