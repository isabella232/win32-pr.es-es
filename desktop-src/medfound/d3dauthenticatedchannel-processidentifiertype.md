---
description: Especifica el tipo de proceso que se identifica en la estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ .
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: Enumeración D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153656"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a><span data-ttu-id="bd529-103">\_Enumeración de D3DAUTHENTICATEDCHANNEL PROCESSIDENTIFIERTYPE</span><span class="sxs-lookup"><span data-stu-id="bd529-103">D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE enumeration</span></span>

<span data-ttu-id="bd529-104">Especifica el tipo de proceso que se identifica en la estructura de [**\_ \_ salida de D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) .</span><span class="sxs-lookup"><span data-stu-id="bd529-104">Specifies the type of process that is identified in the [**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd529-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd529-105">Syntax</span></span>


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a><span data-ttu-id="bd529-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bd529-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bd529-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="bd529-107"><span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="bd529-108">Tipo de proceso desconocido.</span><span class="sxs-lookup"><span data-stu-id="bd529-108">Unknown process type.</span></span>

</dd> <dt>

<span data-ttu-id="bd529-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE \_ DWM**</span><span class="sxs-lookup"><span data-stu-id="bd529-109"><span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE\_DWM**</span></span>
</dt> <dd>

<span data-ttu-id="bd529-110">Proceso Administrador de ventanas de escritorio (DWM).</span><span class="sxs-lookup"><span data-stu-id="bd529-110">Desktop Window Manager (DWM) process.</span></span>

</dd> <dt>

<span data-ttu-id="bd529-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**identificador de PROCESSIDTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="bd529-111"><span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="bd529-112">Identificador de un proceso.</span><span class="sxs-lookup"><span data-stu-id="bd529-112">Handle to a process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd529-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd529-113">Requirements</span></span>



| <span data-ttu-id="bd529-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd529-114">Requirement</span></span> | <span data-ttu-id="bd529-115">Value</span><span class="sxs-lookup"><span data-stu-id="bd529-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd529-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd529-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bd529-117">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd529-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bd529-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd529-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bd529-119">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd529-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bd529-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd529-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd529-121"><dt>D3d9types. h (incluye d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd529-121"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd529-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd529-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd529-123">Enumeraciones de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="bd529-123">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




