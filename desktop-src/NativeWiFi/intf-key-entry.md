---
description: Almacena la información clave sobre una interfaz LAN inalámbrica administrada por el servicio de configuración inalámbrica.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: INTF_KEY_ENTRY estructura (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360378"
---
# <a name="intf_key_entry-structure"></a><span data-ttu-id="65405-103">Estructura de entrada de \_ clave de Intf \_</span><span class="sxs-lookup"><span data-stu-id="65405-103">INTF\_KEY\_ENTRY structure</span></span>

<span data-ttu-id="65405-104">\[**Intf \_ La \_ entrada de clave** ya no se admite en Windows Vista y windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="65405-104">\[**INTF\_KEY\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="65405-105">En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar.</span><span class="sxs-lookup"><span data-stu-id="65405-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="65405-106">Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="65405-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="65405-107">La estructura de **\_ \_ entrada de clave de Intf** almacena la información clave sobre una interfaz LAN inalámbrica administrada por el servicio de configuración inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="65405-107">The **INTF\_KEY\_ENTRY** structure stores the key information about a wireless LAN interface managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="65405-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65405-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a><span data-ttu-id="65405-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="65405-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="65405-110">**wszGuid**</span><span class="sxs-lookup"><span data-stu-id="65405-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="65405-111">Puntero al GUID de la interfaz que se representa como una cadena Unicode en el siguiente formato: "{xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".</span><span class="sxs-lookup"><span data-stu-id="65405-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65405-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65405-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65405-113">El archivo de encabezado *wzcsapi. h* no está disponible en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="65405-113">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65405-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65405-114">Requirements</span></span>



| <span data-ttu-id="65405-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="65405-115">Requirement</span></span> | <span data-ttu-id="65405-116">Value</span><span class="sxs-lookup"><span data-stu-id="65405-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65405-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65405-117">Minimum supported client</span></span><br/> | <span data-ttu-id="65405-118">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="65405-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="65405-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65405-119">Minimum supported server</span></span><br/> | <span data-ttu-id="65405-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="65405-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="65405-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="65405-121">End of client support</span></span><br/>    | <span data-ttu-id="65405-122">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="65405-122">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="65405-123">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="65405-123">End of server support</span></span><br/>    | <span data-ttu-id="65405-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65405-124">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="65405-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65405-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="65405-126"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="65405-126"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65405-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="65405-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65405-128">**\_tabla de claves de INTFS \_**</span><span class="sxs-lookup"><span data-stu-id="65405-128">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="65405-129">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="65405-129">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> </dl>

 

 




