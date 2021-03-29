---
title: add timeout
description: Agrega un tiempo de espera global al servicio HTTP.sys.
ms.assetid: c59a64e2-36aa-4428-b727-df21f5632d0d
keywords:
- agregar tiempo de espera HTTP
topic_type:
- apiref
api_name:
- add timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2637cb5db663ea36b15eb382a16b02b166e98f88
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104419786"
---
# <a name="add-timeout"></a><span data-ttu-id="85ae6-104">add timeout</span><span class="sxs-lookup"><span data-stu-id="85ae6-104">add timeout</span></span>

<span data-ttu-id="85ae6-105">Agrega un tiempo de espera global al servicio HTTP.sys.</span><span class="sxs-lookup"><span data-stu-id="85ae6-105">Adds a global timeout to the HTTP.sys service.</span></span>

``` syntax
add timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
            [value=]u-short

 
```

## <a name="parameters"></a><span data-ttu-id="85ae6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85ae6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ae6-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleconnectiontimeout, \| HeaderWaitTimeout}**</span><span class="sxs-lookup"><span data-stu-id="85ae6-107"><span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype=\]{idleconnectiontimeout\|headerwaittimeout}**</span></span>
</dt> <dd>

<span data-ttu-id="85ae6-108">Especifica el tipo de tiempo de espera para la configuración.</span><span class="sxs-lookup"><span data-stu-id="85ae6-108">Specifies the type of timeout for setting.</span></span>

</dd> <dt>

<span data-ttu-id="85ae6-109"><span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>\**\[valor = \] \* \* \* u-Short*</span><span class="sxs-lookup"><span data-stu-id="85ae6-109"><span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>\**\[value=\]\*\*\*u-short*</span></span>
</dt> <dd>

<span data-ttu-id="85ae6-110">Especifica el valor del tiempo de espera (en segundos).</span><span class="sxs-lookup"><span data-stu-id="85ae6-110">Specifies the value of the timeout (in seconds).</span></span> <span data-ttu-id="85ae6-111">Si el valor es hexadecimal, agregue el prefijo 0x.</span><span class="sxs-lookup"><span data-stu-id="85ae6-111">If value is hexadecimal, then add the prefix 0x.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="85ae6-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="85ae6-112">Examples</span></span>

<span data-ttu-id="85ae6-113">**add timeout timeouttype=idleconnectiontimeout value=120**</span><span class="sxs-lookup"><span data-stu-id="85ae6-113">**add timeout timeouttype=idleconnectiontimeout value=120**</span></span>

<span data-ttu-id="85ae6-114">**add timeout timeouttype=headerwaittimeout value=0x40**</span><span class="sxs-lookup"><span data-stu-id="85ae6-114">**add timeout timeouttype=headerwaittimeout value=0x40**</span></span>

 

 




