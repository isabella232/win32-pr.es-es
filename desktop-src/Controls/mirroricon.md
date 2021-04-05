---
title: MirrorIcon función)
description: Invierte los iconos (reflejos) para que se muestren correctamente en un contexto de dispositivo reflejado.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- MirrorIcon (función) controles de Windows
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079001"
---
# <a name="mirroricon-function"></a><span data-ttu-id="09c8e-104">MirrorIcon función)</span><span class="sxs-lookup"><span data-stu-id="09c8e-104">MirrorIcon function</span></span>

<span data-ttu-id="09c8e-105">\[**MirrorIcon** está disponible a través de Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="09c8e-105">\[**MirrorIcon** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="09c8e-106">Podría modificarse o no estar disponible en versiones posteriores.\]</span><span class="sxs-lookup"><span data-stu-id="09c8e-106">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="09c8e-107">Invierte los iconos (reflejos) para que se muestren correctamente en un contexto de dispositivo reflejado.</span><span class="sxs-lookup"><span data-stu-id="09c8e-107">Reverses (mirrors) icons so that they are displayed correctly on a mirrored device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="09c8e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09c8e-108">Syntax</span></span>


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a><span data-ttu-id="09c8e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09c8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09c8e-110">*phIconSmall* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="09c8e-110">*phIconSmall* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09c8e-111">Tipo: \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="09c8e-111">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="09c8e-112">Puntero al identificador de icono que hace referencia a una versión pequeña de un icono.</span><span class="sxs-lookup"><span data-stu-id="09c8e-112">A pointer to the icon handle that references a small version of an icon.</span></span>

</dd> <dt>

<span data-ttu-id="09c8e-113">_phIconLarge \* \[ in, out, Optional\]</span><span class="sxs-lookup"><span data-stu-id="09c8e-113">_phIconLarge\* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="09c8e-114">Tipo: \**[**HICON**](/windows/desktop/WinProg/windows-data-types) \** _</span><span class="sxs-lookup"><span data-stu-id="09c8e-114">Type: \**[**HICON**](/windows/desktop/WinProg/windows-data-types)\** _</span></span>

<span data-ttu-id="09c8e-115">Puntero al identificador de icono que hace referencia a una versión grande de un icono.</span><span class="sxs-lookup"><span data-stu-id="09c8e-115">A pointer to the icon handle that references a large version of an icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09c8e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09c8e-116">Return value</span></span>

<span data-ttu-id="09c8e-117">Tipo: _ *[**bool**](/windows/desktop/WinProg/windows-data-types)*\*</span><span class="sxs-lookup"><span data-stu-id="09c8e-117">Type: _ *[**BOOL**](/windows/desktop/WinProg/windows-data-types)*\*</span></span>

<span data-ttu-id="09c8e-118">**True si es** correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="09c8e-118">**TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="09c8e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09c8e-119">Remarks</span></span>

<span data-ttu-id="09c8e-120">**MirrorIcon** no se exporta por nombre o se declara en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="09c8e-120">**MirrorIcon** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="09c8e-121">Para usarlo, debe utilizar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y el ordinal de solicitud 414 de ComCtl32.dll para obtener un puntero de función.</span><span class="sxs-lookup"><span data-stu-id="09c8e-121">To use it, you must use [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and request ordinal 414 from ComCtl32.dll to obtain a function pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="09c8e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09c8e-122">Requirements</span></span>



| <span data-ttu-id="09c8e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="09c8e-123">Requirement</span></span> | <span data-ttu-id="09c8e-124">Value</span><span class="sxs-lookup"><span data-stu-id="09c8e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09c8e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09c8e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="09c8e-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="09c8e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="09c8e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09c8e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="09c8e-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="09c8e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="09c8e-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09c8e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09c8e-130"><dt>Comctl32.dll (versión 5,81 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="09c8e-130"><dt>Comctl32.dll (version 5.81 or later)</dt></span></span> </dl> |



 

