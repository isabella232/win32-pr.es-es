---
title: Network. getProxyBypassForLocal (método)
description: El método getProxyBypassForLocal recupera un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- método getProxyBypassForLocal de Windows Media Player
- método getProxyBypassForLocal Windows Media Player, clase de red
- Clase de red Windows Media Player, método getProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708806"
---
# <a name="networkgetproxybypassforlocal-method"></a><span data-ttu-id="822f3-106">Network. getProxyBypassForLocal (método)</span><span class="sxs-lookup"><span data-stu-id="822f3-106">Network.getProxyBypassForLocal method</span></span>

<span data-ttu-id="822f3-107">El método **getProxyBypassForLocal** recupera un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.</span><span class="sxs-lookup"><span data-stu-id="822f3-107">The **getProxyBypassForLocal** method retrieves a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="822f3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="822f3-108">Syntax</span></span>


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="822f3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="822f3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="822f3-110">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="822f3-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="822f3-111">**Cadena** que especifica el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="822f3-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="822f3-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="822f3-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="822f3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="822f3-113">Return value</span></span>

<span data-ttu-id="822f3-114">Este método devuelve un **valor booleano** que indica si se omite el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="822f3-114">This method returns a **Boolean** indicating whether the proxy server is bypassed.</span></span> <span data-ttu-id="822f3-115">El valor devuelto solo es significativo cuando **getProxySettings** devuelve un valor de dos (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="822f3-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="822f3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="822f3-116">Remarks</span></span>

<span data-ttu-id="822f3-117">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="822f3-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="822f3-118">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="822f3-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="822f3-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="822f3-119">Examples</span></span>

<span data-ttu-id="822f3-120">En el siguiente ejemplo de JScript se usa *Network*. **getProxyBypassForLocal** para mostrar si Windows Media Player está configurado para omitir el servidor proxy para las direcciones locales.</span><span class="sxs-lookup"><span data-stu-id="822f3-120">The following JScript example uses *Network*.**getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="822f3-121">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="822f3-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a><span data-ttu-id="822f3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="822f3-122">Requirements</span></span>



| <span data-ttu-id="822f3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="822f3-123">Requirement</span></span> | <span data-ttu-id="822f3-124">Value</span><span class="sxs-lookup"><span data-stu-id="822f3-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="822f3-125">Versión</span><span class="sxs-lookup"><span data-stu-id="822f3-125">Version</span></span><br/> | <span data-ttu-id="822f3-126">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="822f3-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="822f3-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="822f3-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="822f3-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="822f3-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="822f3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="822f3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="822f3-130">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="822f3-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="822f3-131">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="822f3-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





