---
title: Network. getProxyName (método)
description: El método getProxyName recupera el nombre del servidor proxy que se está usando.
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- método getProxyName de Windows Media Player
- método getProxyName Windows Media Player, clase de red
- Clase de red Windows Media Player, método getProxyName
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97e51508e9df9aeac85dbc01116e80e710dcb45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708882"
---
# <a name="networkgetproxyname-method"></a><span data-ttu-id="642e1-106">Network. getProxyName (método)</span><span class="sxs-lookup"><span data-stu-id="642e1-106">Network.getProxyName method</span></span>

<span data-ttu-id="642e1-107">El método **getProxyName** recupera el nombre del servidor proxy que se está usando.</span><span class="sxs-lookup"><span data-stu-id="642e1-107">The **getProxyName** method retrieves the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="642e1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="642e1-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyName(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="642e1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="642e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="642e1-110">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="642e1-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="642e1-111">**Cadena** que especifica el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="642e1-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="642e1-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="642e1-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="642e1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="642e1-113">Return value</span></span>

<span data-ttu-id="642e1-114">Este método devuelve una **cadena** que contiene el nombre del servidor proxy que se está usando.</span><span class="sxs-lookup"><span data-stu-id="642e1-114">This method returns a **String** containing the name of the proxy server being used.</span></span> <span data-ttu-id="642e1-115">El valor devuelto solo es significativo cuando **getProxySettings** devuelve un valor de 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="642e1-115">The value returned is meaningful only when **getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="642e1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="642e1-116">Remarks</span></span>

<span data-ttu-id="642e1-117">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="642e1-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="642e1-118">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="642e1-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="642e1-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="642e1-119">Examples</span></span>

<span data-ttu-id="642e1-120">En el siguiente ejemplo de JScript se usa *Network*. **getProxyName** para mostrar los nombres de servidor proxy de Windows Media Player para los protocolos http y MMS.</span><span class="sxs-lookup"><span data-stu-id="642e1-120">The following JScript example uses *Network*.**getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="642e1-121">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="642e1-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

```



## <a name="requirements"></a><span data-ttu-id="642e1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="642e1-122">Requirements</span></span>



| <span data-ttu-id="642e1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="642e1-123">Requirement</span></span> | <span data-ttu-id="642e1-124">Value</span><span class="sxs-lookup"><span data-stu-id="642e1-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="642e1-125">Versión</span><span class="sxs-lookup"><span data-stu-id="642e1-125">Version</span></span><br/> | <span data-ttu-id="642e1-126">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="642e1-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="642e1-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="642e1-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="642e1-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="642e1-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="642e1-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="642e1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="642e1-130">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="642e1-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="642e1-131">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="642e1-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





