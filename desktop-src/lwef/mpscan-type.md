---
title: Enumeración MPSCAN_TYPE (MpClient. h)
description: Tipo de examen realizado.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE enumeración características de entorno heredado de Windows
- PMPSCAN_TYPE el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb89137dc9cfe5b8a4ff1f44a7a101239aa3a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801250"
---
# <a name="mpscan_type-enumeration"></a><span data-ttu-id="8e6dc-105">\_Enumeración de tipo MPSCAN</span><span class="sxs-lookup"><span data-stu-id="8e6dc-105">MPSCAN\_TYPE enumeration</span></span>

<span data-ttu-id="8e6dc-106">Tipo de examen realizado.</span><span class="sxs-lookup"><span data-stu-id="8e6dc-106">Type of scan performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e6dc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e6dc-107">Syntax</span></span>


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a><span data-ttu-id="8e6dc-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="8e6dc-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8e6dc-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**\_tipo MPSCAN \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="8e6dc-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**MPSCAN\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="8e6dc-110">Exclusivamente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="8e6dc-110">Internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="8e6dc-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN \_ tipo \_ rápido**</span><span class="sxs-lookup"><span data-stu-id="8e6dc-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN\_TYPE\_QUICK**</span></span>
</dt> <dd>

<span data-ttu-id="8e6dc-112">Examina los procesos en ejecución y varios puntos ASEP del sistema en los que normalmente se oculta el malware.</span><span class="sxs-lookup"><span data-stu-id="8e6dc-112">Scans running processes and various ASEP points in the system where malware typically hides.</span></span>

</dd> <dt>

<span data-ttu-id="8e6dc-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**\_tipo MPSCAN \_ completo**</span><span class="sxs-lookup"><span data-stu-id="8e6dc-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN\_TYPE\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="8e6dc-114">Realiza un examen rápido seguido de la exploración de todas las unidades fijas del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e6dc-114">Performs a quick scan followed by scan of all fixed drives of the system.</span></span>

</dd> <dt>

<span data-ttu-id="8e6dc-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**\_recurso de tipo MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="8e6dc-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**MPSCAN\_TYPE\_RESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="8e6dc-116">Examina recursos específicos, como archivos o carpetas.</span><span class="sxs-lookup"><span data-stu-id="8e6dc-116">Scans specific resources, such as files or folders.</span></span>

</dd> <dt>

<span data-ttu-id="8e6dc-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN \_ tipo \_ MAXVALUE**</span><span class="sxs-lookup"><span data-stu-id="8e6dc-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="8e6dc-118">Valor máximo posible.</span><span class="sxs-lookup"><span data-stu-id="8e6dc-118">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e6dc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e6dc-119">Requirements</span></span>



| <span data-ttu-id="8e6dc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e6dc-120">Requirement</span></span> | <span data-ttu-id="8e6dc-121">Value</span><span class="sxs-lookup"><span data-stu-id="8e6dc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e6dc-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e6dc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e6dc-123">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e6dc-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8e6dc-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e6dc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e6dc-125">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e6dc-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e6dc-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e6dc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e6dc-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e6dc-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





