---
description: Contenga el nombre o una descripción de un perfil de LAN inalámbrica.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: Tipo simple de nameType (LAN_policy) (perfil)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 77ad0b96cc2887e65af8a7ffc1ab71953dee478b
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105681316"
---
# <a name="nametype-simple-type-lan_policy"></a><span data-ttu-id="49ec4-103">Tipo simple de nameType (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="49ec4-103">nameType Simple Type (LAN_policy)</span></span>

<span data-ttu-id="49ec4-104">El tipo simple nameType puede contener el nombre o una descripción de un perfil de LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="49ec4-104">The nameType simple type can contain either the name or a description of a wireless LAN profile.</span></span> <span data-ttu-id="49ec4-105">Este valor de cadena debe tener entre 1 y 255 caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="49ec4-105">This string value must be between 1 and 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="49ec4-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49ec4-106">Requirements</span></span>



| <span data-ttu-id="49ec4-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ec4-107">Requirement</span></span> | <span data-ttu-id="49ec4-108">Value</span><span class="sxs-lookup"><span data-stu-id="49ec4-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="49ec4-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49ec4-109">Minimum supported client</span></span><br/> | <span data-ttu-id="49ec4-110">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="49ec4-110">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="49ec4-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49ec4-111">Minimum supported server</span></span><br/> | <span data-ttu-id="49ec4-112">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="49ec4-112">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="49ec4-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="49ec4-113">Redistributable</span></span><br/>          | <span data-ttu-id="49ec4-114">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="49ec4-114">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




