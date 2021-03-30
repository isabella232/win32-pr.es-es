---
title: MPCOMPONENT_STATUS estructura (MpClient. h)
description: Información de estado del componente.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCOMPONENT_STATUS características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801916"
---
# <a name="mpcomponent_status-structure"></a><span data-ttu-id="8ebda-105">Estructura de estado de MPCOMPONENT \_</span><span class="sxs-lookup"><span data-stu-id="8ebda-105">MPCOMPONENT\_STATUS structure</span></span>

<span data-ttu-id="8ebda-106">Información de estado del componente.</span><span class="sxs-lookup"><span data-stu-id="8ebda-106">Component status information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ebda-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ebda-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="8ebda-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8ebda-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ebda-109">**fEnable**</span><span class="sxs-lookup"><span data-stu-id="8ebda-109">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="8ebda-110">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="8ebda-110">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="8ebda-111">Estado del componente.</span><span class="sxs-lookup"><span data-stu-id="8ebda-111">Status for the component.</span></span>

</dd> <dt>

<span data-ttu-id="8ebda-112">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8ebda-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="8ebda-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8ebda-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="8ebda-114">Código de éxito o error asociado al estado.</span><span class="sxs-lookup"><span data-stu-id="8ebda-114">Success or failure code associated with the status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ebda-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ebda-115">Requirements</span></span>



| <span data-ttu-id="8ebda-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ebda-116">Requirement</span></span> | <span data-ttu-id="8ebda-117">Value</span><span class="sxs-lookup"><span data-stu-id="8ebda-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebda-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ebda-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8ebda-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ebda-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8ebda-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ebda-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8ebda-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ebda-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ebda-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ebda-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ebda-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ebda-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





