---
title: MPCOMPONENT_VERSION estructura (MpClient. h)
description: Versión y tiempo de actualización de un componente individual.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCOMPONENT_VERSION características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996338"
---
# <a name="mpcomponent_version-structure"></a><span data-ttu-id="7956c-105">Estructura de la versión de MPCOMPONENT \_</span><span class="sxs-lookup"><span data-stu-id="7956c-105">MPCOMPONENT\_VERSION structure</span></span>

<span data-ttu-id="7956c-106">Versión y tiempo de actualización de un componente individual.</span><span class="sxs-lookup"><span data-stu-id="7956c-106">Version and update time for an individual component.</span></span>

## <a name="syntax"></a><span data-ttu-id="7956c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7956c-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a><span data-ttu-id="7956c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7956c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7956c-109">**Versión**</span><span class="sxs-lookup"><span data-stu-id="7956c-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="7956c-110">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="7956c-110">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="7956c-111">Campo de versión.</span><span class="sxs-lookup"><span data-stu-id="7956c-111">Version field.</span></span> <span data-ttu-id="7956c-112">Cada **palabra** representa una versión principal, secundaria, de compilación y de revisión.</span><span class="sxs-lookup"><span data-stu-id="7956c-112">Each **WORD** represents major, minor, build, and revision.</span></span>

</dd> <dt>

<span data-ttu-id="7956c-113">**UpdateTime**</span><span class="sxs-lookup"><span data-stu-id="7956c-113">**UpdateTime**</span></span>
</dt> <dd>

<span data-ttu-id="7956c-114">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="7956c-114">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="7956c-115">Hora de la última actualización del componente, en formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="7956c-115">Last update time of the component, in **FILETIME** format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7956c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7956c-116">Requirements</span></span>



| <span data-ttu-id="7956c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7956c-117">Requirement</span></span> | <span data-ttu-id="7956c-118">Value</span><span class="sxs-lookup"><span data-stu-id="7956c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7956c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7956c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7956c-120">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="7956c-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7956c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7956c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7956c-122">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7956c-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7956c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7956c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7956c-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7956c-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





