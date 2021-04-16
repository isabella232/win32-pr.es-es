---
description: La estructura NMCOLUMNINFO define una columna en el panel superior del Visor de eventos.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Estructura NMCOLUMNINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688634"
---
# <a name="nmcolumninfo-structure"></a><span data-ttu-id="4b272-103">Estructura NMCOLUMNINFO</span><span class="sxs-lookup"><span data-stu-id="4b272-103">NMCOLUMNINFO structure</span></span>

<span data-ttu-id="4b272-104">La estructura **NMCOLUMNINFO** define una columna en el panel superior del visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="4b272-104">The **NMCOLUMNINFO** structure defines one column in the top pane of the Event Viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b272-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b272-105">Syntax</span></span>


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a><span data-ttu-id="4b272-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="4b272-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b272-107">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="4b272-107">**szColumnName**</span></span>
</dt> <dd>

<span data-ttu-id="4b272-108">Nombre para mostrar de una columna específica.</span><span class="sxs-lookup"><span data-stu-id="4b272-108">Displayable name of a specific column.</span></span> <span data-ttu-id="4b272-109">Si el nombre es demasiado largo, no estará completamente visible en la configuración de Visor de eventos predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4b272-109">If the name is too long, it will not be completely visible in the default Event Viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4b272-110">**VariantData**</span><span class="sxs-lookup"><span data-stu-id="4b272-110">**VariantData**</span></span>
</dt> <dd>

<span data-ttu-id="4b272-111">Los datos insertados en la columna.</span><span class="sxs-lookup"><span data-stu-id="4b272-111">The data inserted into the column.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b272-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b272-112">Requirements</span></span>



| <span data-ttu-id="4b272-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b272-113">Requirement</span></span> | <span data-ttu-id="4b272-114">Value</span><span class="sxs-lookup"><span data-stu-id="4b272-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4b272-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b272-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4b272-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4b272-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4b272-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b272-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4b272-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b272-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4b272-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b272-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b272-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b272-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




