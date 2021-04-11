---
title: MPENDOFLIFE_DATA estructura (MpClient. h)
description: '\ 0034; Final de la vida \ 0034; datos de notificación.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPENDOFLIFE_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150676"
---
# <a name="mpendoflife_data-structure"></a><span data-ttu-id="04ad7-105">\_Estructura de datos MPENDOFLIFE</span><span class="sxs-lookup"><span data-stu-id="04ad7-105">MPENDOFLIFE\_DATA structure</span></span>

<span data-ttu-id="04ad7-106">Datos de notificación de "fin de la vida".</span><span class="sxs-lookup"><span data-stu-id="04ad7-106">"End of life" notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ad7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04ad7-107">Syntax</span></span>


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a><span data-ttu-id="04ad7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="04ad7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="04ad7-109">**ftSignatureExpiry**</span><span class="sxs-lookup"><span data-stu-id="04ad7-109">**ftSignatureExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="04ad7-110">Tipo: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="04ad7-110">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="04ad7-111">Hora a la que expira la firma.</span><span class="sxs-lookup"><span data-stu-id="04ad7-111">Time when the signature expires.</span></span>

</dd> <dt>

<span data-ttu-id="04ad7-112">**ftPlatformExpiry**</span><span class="sxs-lookup"><span data-stu-id="04ad7-112">**ftPlatformExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="04ad7-113">Tipo: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="04ad7-113">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="04ad7-114">Hora a la que expira la plataforma.</span><span class="sxs-lookup"><span data-stu-id="04ad7-114">Time when the platform expires.</span></span>

</dd> <dt>

<span data-ttu-id="04ad7-115">**fAdminControlled**</span><span class="sxs-lookup"><span data-stu-id="04ad7-115">**fAdminControlled**</span></span>
</dt> <dd>

<span data-ttu-id="04ad7-116">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="04ad7-116">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="04ad7-117">True si el administrador controla la Directiva para mostrar la notificación.</span><span class="sxs-lookup"><span data-stu-id="04ad7-117">True if the administrator controlling the policy for showing the notification.</span></span> <span data-ttu-id="04ad7-118">Si se establece, indica a la interfaz de usuario que no muestre la notificación EOL.</span><span class="sxs-lookup"><span data-stu-id="04ad7-118">If set, this tells the UI to not show the EOL notification.</span></span>

</dd> <dt>

<span data-ttu-id="04ad7-119">**fEndOfLifeImpendingOrPast**</span><span class="sxs-lookup"><span data-stu-id="04ad7-119">**fEndOfLifeImpendingOrPast**</span></span>
</dt> <dd>

<span data-ttu-id="04ad7-120">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="04ad7-120">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="04ad7-121">True si "fin de la vida" está pendiente o pasado.</span><span class="sxs-lookup"><span data-stu-id="04ad7-121">True if "End of Life" is pending or past.</span></span> <span data-ttu-id="04ad7-122">Si es false, la interfaz de usuario y los clientes pueden borrar cualquier estado relacionado con EOL.</span><span class="sxs-lookup"><span data-stu-id="04ad7-122">If false, UI and clients can clear any EOL related states.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04ad7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04ad7-123">Requirements</span></span>



| <span data-ttu-id="04ad7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ad7-124">Requirement</span></span> | <span data-ttu-id="04ad7-125">Value</span><span class="sxs-lookup"><span data-stu-id="04ad7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04ad7-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ad7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="04ad7-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="04ad7-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="04ad7-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="04ad7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="04ad7-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="04ad7-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04ad7-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04ad7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="04ad7-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="04ad7-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





