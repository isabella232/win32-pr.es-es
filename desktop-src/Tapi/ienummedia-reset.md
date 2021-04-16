---
description: El método Reset se restablece al principio de la secuencia de enumeración.
ms.assetid: 338e0614-8f18-4ee2-8697-66ff3898f813
title: 'IEnumMedia:: RESET (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14624d5a048df2f5bc80205f34f262068c53da74
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689646"
---
# <a name="ienummediareset-method"></a><span data-ttu-id="68a7a-103">IEnumMedia:: RESET (método)</span><span class="sxs-lookup"><span data-stu-id="68a7a-103">IEnumMedia::Reset method</span></span>

<span data-ttu-id="68a7a-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="68a7a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="68a7a-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="68a7a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="68a7a-106">El método **RESET** se restablece al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="68a7a-106">The **Reset** method resets to the beginning of enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a7a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68a7a-107">Syntax</span></span>


```C++
HRESULT Reset();
```

## <a name="parameters"></a><span data-ttu-id="68a7a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68a7a-108">Parameters</span></span>
<span data-ttu-id="68a7a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="68a7a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68a7a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68a7a-110">Return value</span></span>
<span data-ttu-id="68a7a-111">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="68a7a-111">This method can return one of these values.</span></span>

| <span data-ttu-id="68a7a-112">Value</span><span class="sxs-lookup"><span data-stu-id="68a7a-112">Value</span></span> | <span data-ttu-id="68a7a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="68a7a-113">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="68a7a-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="68a7a-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="68a7a-115">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="68a7a-115">Method succeeded.</span></span> <br/>         |
