---
description: La \_ clase HWConfig NIC es la clase de tipo de evento para los eventos de configuración de tarjeta de interfaz de red. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: HWConfig_NIC (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: df3897c67ed65eeec5ace49dac1088ca35223a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083236"
---
# <a name="hwconfig_nic-class"></a><span data-ttu-id="115c3-104">\_Clase HWConfig NIC</span><span class="sxs-lookup"><span data-stu-id="115c3-104">HWConfig\_NIC class</span></span>

<span data-ttu-id="115c3-105">La clase **HWConfig \_ NIC** es la clase de tipo de evento para los eventos de configuración de tarjeta de interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="115c3-105">The **HWConfig\_NIC** class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="115c3-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="115c3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="115c3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="115c3-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a><span data-ttu-id="115c3-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="115c3-108">Members</span></span>

<span data-ttu-id="115c3-109">La **clase \_ NIC HWConfig** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="115c3-109">The **HWConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="115c3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="115c3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="115c3-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="115c3-111">Properties</span></span>

<span data-ttu-id="115c3-112">La clase **HWConfig \_ NIC** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="115c3-112">The **HWConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="115c3-113">NICName</span><span class="sxs-lookup"><span data-stu-id="115c3-113">NICName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="115c3-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="115c3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="115c3-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="115c3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="115c3-116">Calificadores: WmiDataId (1), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="115c3-116">Qualifiers: WmiDataId(1), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="115c3-117">Nombre de la tarjeta de interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="115c3-117">Name of the network interface card.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="115c3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="115c3-118">Requirements</span></span>



| <span data-ttu-id="115c3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="115c3-119">Requirement</span></span> | <span data-ttu-id="115c3-120">Value</span><span class="sxs-lookup"><span data-stu-id="115c3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="115c3-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="115c3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="115c3-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="115c3-122">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="115c3-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="115c3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="115c3-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="115c3-124">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="115c3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="115c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="115c3-126">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="115c3-126">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




