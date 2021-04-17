---
description: La estructura EXPERTCONFIG contiene los datos de configuración del experto. El experto superpone el miembro RawConfigData con una estructura específica del experto.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Estructura EXPERTCONFIG (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666301"
---
# <a name="expertconfig-structure"></a><span data-ttu-id="4035d-104">Estructura EXPERTCONFIG</span><span class="sxs-lookup"><span data-stu-id="4035d-104">EXPERTCONFIG structure</span></span>

<span data-ttu-id="4035d-105">La estructura **EXPERTCONFIG** contiene los datos de configuración del experto.</span><span class="sxs-lookup"><span data-stu-id="4035d-105">The **EXPERTCONFIG** structure contains the configuration data of the expert.</span></span> <span data-ttu-id="4035d-106">El experto superpone el miembro **RawConfigData** con una estructura específica del experto.</span><span class="sxs-lookup"><span data-stu-id="4035d-106">The expert overlays the **RawConfigData** member with an expert-specific structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4035d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4035d-107">Syntax</span></span>


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a><span data-ttu-id="4035d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4035d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4035d-109">**RawConfigLength**</span><span class="sxs-lookup"><span data-stu-id="4035d-109">**RawConfigLength**</span></span>
</dt> <dd>

<span data-ttu-id="4035d-110">Longitud total de la estructura, incluidos los cuatro bytes usados para el miembro.</span><span class="sxs-lookup"><span data-stu-id="4035d-110">Total length of the structure, including the four bytes used for the member.</span></span> <span data-ttu-id="4035d-111">Monitor de red usa el valor cuando la estructura se guarda en una unidad de disco y se lee de ella.</span><span class="sxs-lookup"><span data-stu-id="4035d-111">Network Monitor uses the value when the structure is saved-to and read-from a disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="4035d-112">**RawConfigData**</span><span class="sxs-lookup"><span data-stu-id="4035d-112">**RawConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="4035d-113">Datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="4035d-113">Configuration data.</span></span> <span data-ttu-id="4035d-114">El experto debe agregar los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="4035d-114">The expert must add the configuration data.</span></span> <span data-ttu-id="4035d-115">Por ejemplo, supongamos que tiene una estructura de datos que tenía el aspecto siguiente.</span><span class="sxs-lookup"><span data-stu-id="4035d-115">For example, suppose that you had a data structure that looked like this.</span></span>

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

<span data-ttu-id="4035d-116">Tenga en cuenta que **RawConfigLength** garantiza que la superposición funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="4035d-116">Note that **RawConfigLength** ensures that the overlay works correctly.</span></span> <span data-ttu-id="4035d-117">Al usar los datos, el código podría tener el aspecto siguiente:</span><span class="sxs-lookup"><span data-stu-id="4035d-117">When you use the data, your code might look like this:</span></span>

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4035d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4035d-118">Requirements</span></span>



| <span data-ttu-id="4035d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4035d-119">Requirement</span></span> | <span data-ttu-id="4035d-120">Value</span><span class="sxs-lookup"><span data-stu-id="4035d-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4035d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4035d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4035d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4035d-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4035d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4035d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4035d-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4035d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4035d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4035d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4035d-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4035d-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




