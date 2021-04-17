---
description: Contiene una lista de identificadores básicos del conjunto de servicios (BSS).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: DOT11_BSSID_LIST estructura (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687762"
---
# <a name="dot11_bssid_list-structure"></a><span data-ttu-id="ff99b-103">\_Estructura de lista BSSID de DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="ff99b-103">DOT11\_BSSID\_LIST structure</span></span>

<span data-ttu-id="ff99b-104">La estructura de **\_ \_ lista BSSID de DOT11** contiene una lista de identificadores básicos del conjunto de servicios (BSS).</span><span class="sxs-lookup"><span data-stu-id="ff99b-104">The **DOT11\_BSSID\_LIST** structure contains a list of basic service set (BSS) identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff99b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff99b-105">Syntax</span></span>


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a><span data-ttu-id="ff99b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff99b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ff99b-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="ff99b-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="ff99b-108">Una estructura de [**\_ \_ encabezado de objeto NDIS**](ndis-object-header.md) que contiene la información de tipo, versión y tamaño de una estructura NDIS.</span><span class="sxs-lookup"><span data-stu-id="ff99b-108">An [**NDIS\_OBJECT\_HEADER**](ndis-object-header.md) structure that contains the type, version, and, size information of an NDIS structure.</span></span> <span data-ttu-id="ff99b-109">En el caso de la mayoría de las estructuras de **\_ \_ listas BSSID de DOT11** , establezca el miembro de **tipo** en el **tipo de \_ objeto NDIS \_ \_ predeterminado**, establezca el miembro de **revisión** en la **revisión de \_ lista BSSID de DOT11 \_ \_ \_ 1** y establezca el miembro de **tamaño** en **sizeof (lista de BSSID de dot11 \_ \_ )**.</span><span class="sxs-lookup"><span data-stu-id="ff99b-109">For most **DOT11\_BSSID\_LIST** structures, set the **Type** member to **NDIS\_OBJECT\_TYPE\_DEFAULT**, set the **Revision** member to **DOT11\_BSSID\_LIST\_REVISION\_1**, and set the **Size** member to **sizeof(DOT11\_BSSID\_LIST)**.</span></span>

</dd> <dt>

<span data-ttu-id="ff99b-110">**uNumOfEntries**</span><span class="sxs-lookup"><span data-stu-id="ff99b-110">**uNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="ff99b-111">Número de entradas en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="ff99b-111">The number of entries in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="ff99b-112">**uTotalNumOfEntries**</span><span class="sxs-lookup"><span data-stu-id="ff99b-112">**uTotalNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="ff99b-113">Número total de entradas admitidas.</span><span class="sxs-lookup"><span data-stu-id="ff99b-113">The total number of entries supported.</span></span>

</dd> <dt>

<span data-ttu-id="ff99b-114">**BSSIDs**</span><span class="sxs-lookup"><span data-stu-id="ff99b-114">**BSSIDs**</span></span>
</dt> <dd>

<span data-ttu-id="ff99b-115">Una lista de identificadores de BSS.</span><span class="sxs-lookup"><span data-stu-id="ff99b-115">A list of BSS identifiers.</span></span> <span data-ttu-id="ff99b-116">Un identificador de BSS se almacena como un tipo de [**\_ \_ dirección Mac de DOT11**](dot11-mac-address-type.md) .</span><span class="sxs-lookup"><span data-stu-id="ff99b-116">A BSS identifier is stored as a [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff99b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff99b-117">Requirements</span></span>



| <span data-ttu-id="ff99b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff99b-118">Requirement</span></span> | <span data-ttu-id="ff99b-119">Value</span><span class="sxs-lookup"><span data-stu-id="ff99b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff99b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff99b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff99b-121">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ff99b-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff99b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff99b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff99b-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff99b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ff99b-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ff99b-124">Redistributable</span></span><br/>          | <span data-ttu-id="ff99b-125">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="ff99b-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="ff99b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff99b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff99b-127"><dt>Windot11. h (incluye Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff99b-127"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff99b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff99b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff99b-129">**\_parámetros de conexión de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="ff99b-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




