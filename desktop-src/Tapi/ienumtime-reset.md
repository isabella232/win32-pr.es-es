---
description: El método Reset se restablece al principio de la secuencia de enumeración.
ms.assetid: a9131da1-051d-493c-939d-07801fda2d49
title: 'IEnumTime:: RESET (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9615fbc07edfb93c2377a7455d94b5fcd8ccd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154568"
---
# <a name="ienumtimereset-method"></a><span data-ttu-id="105b3-103">IEnumTime:: RESET (método)</span><span class="sxs-lookup"><span data-stu-id="105b3-103">IEnumTime::Reset method</span></span>

<span data-ttu-id="105b3-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="105b3-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="105b3-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="105b3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="105b3-106">El método **RESET** se restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="105b3-106">The **Reset** method resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="105b3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="105b3-107">Syntax</span></span>


```C++
HRESULT Reset();
```

## <a name="parameters"></a><span data-ttu-id="105b3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="105b3-108">Parameters</span></span>
<span data-ttu-id="105b3-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="105b3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="105b3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="105b3-110">Return value</span></span>
<span data-ttu-id="105b3-111">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="105b3-111">This method can return one of these values.</span></span>

| <span data-ttu-id="105b3-112">Value</span><span class="sxs-lookup"><span data-stu-id="105b3-112">Value</span></span> | <span data-ttu-id="105b3-113">Significado</span><span class="sxs-lookup"><span data-stu-id="105b3-113">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="105b3-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="105b3-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="105b3-115">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="105b3-115">Method succeeded.</span></span> <br/>         |
