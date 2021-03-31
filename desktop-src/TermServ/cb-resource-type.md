---
title: Enumeración CB_RESOURCE_TYPE (Cbclient. h)
description: Especifica el tipo de recurso al que se está conectando la conexión entrante.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- CB_RESOURCE_TYPE enumeración Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801586"
---
# <a name="cb_resource_type-enumeration"></a><span data-ttu-id="9267c-104">\_Enumeración de tipos de recursos CB \_</span><span class="sxs-lookup"><span data-stu-id="9267c-104">CB\_RESOURCE\_TYPE enumeration</span></span>

<span data-ttu-id="9267c-105">Especifica el tipo de recurso al que se está conectando la conexión entrante.</span><span class="sxs-lookup"><span data-stu-id="9267c-105">Specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="9267c-106">Esta enumeración se usa con la estructura de [**\_ \_ información de conexión CB**](cb-connection-info.md) .</span><span class="sxs-lookup"><span data-stu-id="9267c-106">This enumeration is used with the [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9267c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9267c-107">Syntax</span></span>


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="9267c-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="9267c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9267c-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**recurso CB no \_ \_ definido**</span><span class="sxs-lookup"><span data-stu-id="9267c-109"><span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**CB\_RESOURCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="9267c-110">El tipo de recurso no está definido.</span><span class="sxs-lookup"><span data-stu-id="9267c-110">The resource type is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="9267c-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_sesión de recursos CB \_**</span><span class="sxs-lookup"><span data-stu-id="9267c-111"><span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**CB\_RESOURCE\_SESSION**</span></span>
</dt> <dd>

<span data-ttu-id="9267c-112">El recurso es una sesión remota.</span><span class="sxs-lookup"><span data-stu-id="9267c-112">The resource is a remote session.</span></span>

</dd> <dt>

<span data-ttu-id="9267c-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_máquina virtual de recursos CB \_**</span><span class="sxs-lookup"><span data-stu-id="9267c-113"><span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**CB\_RESOURCE\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="9267c-114">El recurso es una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9267c-114">The resource is a virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9267c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9267c-115">Requirements</span></span>



| <span data-ttu-id="9267c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9267c-116">Requirement</span></span> | <span data-ttu-id="9267c-117">Value</span><span class="sxs-lookup"><span data-stu-id="9267c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9267c-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9267c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9267c-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9267c-119">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="9267c-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9267c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9267c-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9267c-121">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="9267c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9267c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9267c-123"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9267c-123"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9267c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9267c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9267c-125">**\_información de conexión de CB \_**</span><span class="sxs-lookup"><span data-stu-id="9267c-125">**CB\_CONNECTION\_INFO**</span></span>](cb-connection-info.md)
</dt> </dl>

 

 





