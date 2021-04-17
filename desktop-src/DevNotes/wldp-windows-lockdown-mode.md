---
description: Describe los modos seguros (modos S) de un dispositivo Windows.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: Enumeración WLDP_WINDOWS_LOCKDOWN_MODE (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661214"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a><span data-ttu-id="fae11-103">WLDP \_ \_ enumeración del modo de bloqueo de Windows \_</span><span class="sxs-lookup"><span data-stu-id="fae11-103">WLDP\_WINDOWS\_LOCKDOWN\_MODE enumeration</span></span>

<span data-ttu-id="fae11-104">Describe los modos seguros (modos S) de un dispositivo Windows.</span><span class="sxs-lookup"><span data-stu-id="fae11-104">Describes the secure modes (S modes) for a Windows device.</span></span> <span data-ttu-id="fae11-105">Se usa principalmente en [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).</span><span class="sxs-lookup"><span data-stu-id="fae11-105">Used primarily in [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fae11-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fae11-106">Syntax</span></span>


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a><span data-ttu-id="fae11-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="fae11-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fae11-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**\_modo de bloqueo de Windows WLDP \_ \_ \_ desbloqueado**</span><span class="sxs-lookup"><span data-stu-id="fae11-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_UNLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="fae11-109">Desbloquear.</span><span class="sxs-lookup"><span data-stu-id="fae11-109">Unlocked.</span></span> <span data-ttu-id="fae11-110">Se usa principalmente para dispositivos Windows sin el modo S.</span><span class="sxs-lookup"><span data-stu-id="fae11-110">Used primarily for Windows devices without the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="fae11-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP \_ \_ prueba de \_ modo de bloqueo de Windows \_**</span><span class="sxs-lookup"><span data-stu-id="fae11-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_TRIAL**</span></span>
</dt> <dd>

<span data-ttu-id="fae11-112">Periodo.</span><span class="sxs-lookup"><span data-stu-id="fae11-112">Trial.</span></span> <span data-ttu-id="fae11-113">Se usa principalmente para un dispositivo de prueba de Windows 10 con el modo S.</span><span class="sxs-lookup"><span data-stu-id="fae11-113">Used primarily for a Windows 10 trial device with the S mode.</span></span> <span data-ttu-id="fae11-114">El modo de prueba es un caso especial para dispositivos Windows 10 con el modo S: se aplican las directivas, pero no hay protección contra reversión para la aplicación de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="fae11-114">Trial mode is a special case for Windows 10 devices with the S mode: policies are enforced, but there is no anti-rollback protection for the enforcement of the policy.</span></span>

</dd> <dt>

<span data-ttu-id="fae11-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP \_ modo de bloqueo de Windows \_ \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="fae11-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_LOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="fae11-116">Cerrado.</span><span class="sxs-lookup"><span data-stu-id="fae11-116">Locked.</span></span> <span data-ttu-id="fae11-117">Se usa principalmente para un dispositivo de Windows 10 con el modo S.</span><span class="sxs-lookup"><span data-stu-id="fae11-117">Used primarily for a Windows 10 device with the S mode.</span></span> <span data-ttu-id="fae11-118">Un dispositivo que está bloqueado aplicará las directivas de Device Guard firmadas que se incluyen con la imagen del sistema operativo Windows 10 con el modo S.</span><span class="sxs-lookup"><span data-stu-id="fae11-118">A device that is locked will enforce the signed Device Guard policies shipped with the Windows 10 OS image with the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="fae11-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP \_ modo de bloqueo de Windows \_ \_ \_ máximo**</span><span class="sxs-lookup"><span data-stu-id="fae11-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="fae11-120">Valor de enumeración máximo.</span><span class="sxs-lookup"><span data-stu-id="fae11-120">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fae11-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fae11-121">Requirements</span></span>



| <span data-ttu-id="fae11-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fae11-122">Requirement</span></span> | <span data-ttu-id="fae11-123">Value</span><span class="sxs-lookup"><span data-stu-id="fae11-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fae11-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fae11-124">Header</span></span><br/> | <dl> <span data-ttu-id="fae11-125"><dt>WLDP. h</dt></span><span class="sxs-lookup"><span data-stu-id="fae11-125"><dt>Wldp.h</dt></span></span> </dl> |



 

 




