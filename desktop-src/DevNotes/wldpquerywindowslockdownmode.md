---
description: Recupera el modo seguro de Windows actual. Windows puede estar en modo bloqueado, modo normal desbloqueado o modo de prueba.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Función WldpQueryWindowsLockdownMode (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275048"
---
# <a name="wldpquerywindowslockdownmode-function"></a><span data-ttu-id="6b537-104">WldpQueryWindowsLockdownMode función)</span><span class="sxs-lookup"><span data-stu-id="6b537-104">WldpQueryWindowsLockdownMode function</span></span>

<span data-ttu-id="6b537-105">Recupera el modo seguro de Windows actual.</span><span class="sxs-lookup"><span data-stu-id="6b537-105">Retrieves the current Windows secure mode.</span></span> <span data-ttu-id="6b537-106">Windows puede estar en modo bloqueado, modo normal desbloqueado o modo de prueba.</span><span class="sxs-lookup"><span data-stu-id="6b537-106">Windows can be in locked mode, unlocked normal mode, or trial mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b537-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b537-107">Syntax</span></span>


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a><span data-ttu-id="6b537-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b537-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b537-109">*lockdownMode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6b537-109">*lockdownMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b537-110">Si se ejecuta correctamente, devuelve un [**\_ modo de \_ bloqueo \_ de Windows PWLDP**](wldp-windows-lockdown-mode.md) que indica el modo seguro para el dispositivo de Windows 10 actual.</span><span class="sxs-lookup"><span data-stu-id="6b537-110">On success, returns a [**PWLDP\_WINDOWS\_LOCKDOWN\_MODE**](wldp-windows-lockdown-mode.md) that indicates the secure mode for the current Windows 10 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b537-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b537-111">Return value</span></span>

<span data-ttu-id="6b537-112">Este método devuelve **S \_ correcto** si es correcto o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6b537-112">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b537-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b537-113">Requirements</span></span>



| <span data-ttu-id="6b537-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b537-114">Requirement</span></span> | <span data-ttu-id="6b537-115">Value</span><span class="sxs-lookup"><span data-stu-id="6b537-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6b537-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b537-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b537-117">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b537-117">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6b537-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b537-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b537-119">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="6b537-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6b537-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b537-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b537-121"><dt>WLDP. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b537-121"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b537-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b537-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b537-123"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b537-123"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




