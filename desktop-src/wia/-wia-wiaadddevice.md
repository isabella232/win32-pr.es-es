---
description: La función WiaAddDevice invoca la interfaz de usuario del Asistente para la instalación de escáneres y cámaras. Es equivalente a ejecutar &\# 0034; rundll32.exe sti \_ci.dll AddDevice&\# 0034; desde el símbolo del sistema.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Función WiaAddDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809962"
---
# <a name="wiaadddevice-function"></a><span data-ttu-id="82b0a-104">WiaAddDevice función)</span><span class="sxs-lookup"><span data-stu-id="82b0a-104">WiaAddDevice function</span></span>

<span data-ttu-id="82b0a-105">La función **WiaAddDevice** invoca la interfaz de usuario del Asistente para la instalación de escáneres y cámaras.</span><span class="sxs-lookup"><span data-stu-id="82b0a-105">The **WiaAddDevice** function invokes the Scanner and Camera Installation Wizard UI.</span></span> <span data-ttu-id="82b0a-106">Es equivalente a ejecutar "rundll32.exe STI \_ci.dll AddDevice" desde el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="82b0a-106">It is equivalent to running "rundll32.exe sti\_ci.dll AddDevice" from the command prompt.</span></span>

## <a name="syntax"></a><span data-ttu-id="82b0a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82b0a-107">Syntax</span></span>


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a><span data-ttu-id="82b0a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82b0a-108">Parameters</span></span>

<span data-ttu-id="82b0a-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="82b0a-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="82b0a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82b0a-110">Return value</span></span>

<span data-ttu-id="82b0a-111">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="82b0a-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82b0a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82b0a-112">Remarks</span></span>

<span data-ttu-id="82b0a-113">Se debe llamar a esta función con credenciales de administrador.</span><span class="sxs-lookup"><span data-stu-id="82b0a-113">This function should be called with administrator credentials.</span></span> <span data-ttu-id="82b0a-114">Al ejecutarse en control de cuentas de usuario (LUA), el proceso debe elevarse.</span><span class="sxs-lookup"><span data-stu-id="82b0a-114">When running under User Account Control (LUA), the process should be elevated.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b0a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82b0a-115">Requirements</span></span>



| <span data-ttu-id="82b0a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="82b0a-116">Requirement</span></span> | <span data-ttu-id="82b0a-117">Value</span><span class="sxs-lookup"><span data-stu-id="82b0a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82b0a-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82b0a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="82b0a-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="82b0a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="82b0a-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82b0a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="82b0a-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="82b0a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="82b0a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82b0a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="82b0a-123"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="82b0a-123"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="82b0a-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82b0a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="82b0a-125"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82b0a-125"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82b0a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="82b0a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b0a-127">**InstallWiaDevice**</span><span class="sxs-lookup"><span data-stu-id="82b0a-127">**InstallWiaDevice**</span></span>](-wia-installwiadevice.md)
</dt> </dl>

 

 




