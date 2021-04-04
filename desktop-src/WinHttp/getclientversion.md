---
description: Obtiene la versión del motor de procesamiento WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: getClientVersion función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910849"
---
# <a name="getclientversion-function"></a><span data-ttu-id="ed584-103">getClientVersion función)</span><span class="sxs-lookup"><span data-stu-id="ed584-103">getClientVersion function</span></span>

<span data-ttu-id="ed584-104">Obtiene la versión del motor de procesamiento WPAD.</span><span class="sxs-lookup"><span data-stu-id="ed584-104">Gets the version of the WPAD processing engine.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed584-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed584-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed584-106">*IpAddressList*</span><span class="sxs-lookup"><span data-stu-id="ed584-106">*IpAddressList*</span></span> 
</dt> <dd>

<span data-ttu-id="ed584-107">Cadena delimitada por signos de punto y coma que contiene direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="ed584-107">A semi-colon delimited string containing IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed584-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed584-108">Return value</span></span>

<span data-ttu-id="ed584-109">Una lista de direcciones IP delimitadas por punto y coma ordenadas o una cadena vacía si no se puede ordenar la lista de direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="ed584-109">A list of sorted semi-colon delimited IP addresses or an empty string if unable to sort the IP Address list.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed584-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed584-110">Remarks</span></span>

<span data-ttu-id="ed584-111">Actualmente, esta función devuelve la versión 1,0.</span><span class="sxs-lookup"><span data-stu-id="ed584-111">Currently this function returns version 1.0.</span></span>

<span data-ttu-id="ed584-112">Microsoft ha agregado esta función para permitir que los administradores de ti actualicen sus scripts de WPAD para usar versiones diferentes del motor de procesamiento WPAD sin provocar interrupciones en su implementación existente.</span><span class="sxs-lookup"><span data-stu-id="ed584-112">Microsoft added this function to allow IT administrators to update their WPAD scripts to use different versions of the WPAD processing engine without causing breaks to their existing deployment.</span></span> <span data-ttu-id="ed584-113">Por ejemplo, si Microsoft ha agregado una función a la versión 2,0 del motor WPAD, los administradores pueden comprobar la versión antes de intentar llamar a esa función.</span><span class="sxs-lookup"><span data-stu-id="ed584-113">For example, if Microsoft added a function to the 2.0 version of the WPAD engine, then administrators can check the version before attempting to call that function.</span></span> <span data-ttu-id="ed584-114">Esto permite que su script funcione con las versiones 1,0 y 2,0 del motor WPAD del cliente.</span><span class="sxs-lookup"><span data-stu-id="ed584-114">This allows their script to work with client running versions 1.0 and 2.0 of the WPAD engine.</span></span>

## <a name="examples"></a><span data-ttu-id="ed584-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ed584-115">Examples</span></span>

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a><span data-ttu-id="ed584-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed584-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed584-117">Definiciones de API de aplicación auxiliar de proxy compatible con IPv6</span><span class="sxs-lookup"><span data-stu-id="ed584-117">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[<span data-ttu-id="ed584-118">Extensiones IPv6 para el formato de archivo de configuración automática de navegador</span><span class="sxs-lookup"><span data-stu-id="ed584-118">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



