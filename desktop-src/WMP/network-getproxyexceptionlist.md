---
title: Network. getProxyExceptionList (método)
description: El método getProxyExceptionList recupera la lista de excepciones de proxy.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- método getProxyExceptionList de Windows Media Player
- método getProxyExceptionList Windows Media Player, clase de red
- Clase de red Windows Media Player, método getProxyExceptionList
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ace9bd569c1cc53a8f3d522703aee6154e68a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709139"
---
# <a name="networkgetproxyexceptionlist-method"></a><span data-ttu-id="4be15-106">Network. getProxyExceptionList (método)</span><span class="sxs-lookup"><span data-stu-id="4be15-106">Network.getProxyExceptionList method</span></span>

<span data-ttu-id="4be15-107">El método **getProxyExceptionList** recupera la lista de excepciones de proxy.</span><span class="sxs-lookup"><span data-stu-id="4be15-107">The **getProxyExceptionList** method retrieves the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4be15-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4be15-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyExceptionList(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="4be15-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4be15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4be15-110">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4be15-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4be15-111">**Cadena** que especifica el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="4be15-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="4be15-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="4be15-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4be15-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4be15-113">Return value</span></span>

<span data-ttu-id="4be15-114">Este método devuelve una **cadena** que especifica una lista delimitada por signos de punto y coma de hosts para los que se omite el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="4be15-114">This method returns a **String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="4be15-115">El valor devuelto solo es significativo cuando **getProxySettings** devuelve un valor de dos (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="4be15-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="4be15-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4be15-116">Remarks</span></span>

<span data-ttu-id="4be15-117">Esta es una lista de equipos, dominios y/o direcciones que omitirán el servidor proxy cuando la parte del host de la dirección URL de destino coincida con una entrada de la lista.</span><span class="sxs-lookup"><span data-stu-id="4be15-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="4be15-118">El \* carácter se puede usar como comodín para enumerar entradas.</span><span class="sxs-lookup"><span data-stu-id="4be15-118">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="4be15-119">Por ejemplo, \* . com coincidiría con todos los hosts del dominio com, mientras que 67. \* coincidiría con todos los hosts de la clase 67 en una subred.</span><span class="sxs-lookup"><span data-stu-id="4be15-119">For example, \*.com would match all hosts in the com domain while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="4be15-120">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="4be15-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="4be15-121">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="4be15-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="4be15-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4be15-122">Examples</span></span>

<span data-ttu-id="4be15-123">En el siguiente ejemplo de JScript se usa *Network*. **getProxyExceptionList** para mostrar las listas de servidores proxy omitidos para los protocolos MMS y http.</span><span class="sxs-lookup"><span data-stu-id="4be15-123">The following JScript example uses *Network*.**getProxyExceptionList** to display the lists of bypassed proxies for the MMS and HTTP protocols.</span></span> <span data-ttu-id="4be15-124">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4be15-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

```



## <a name="requirements"></a><span data-ttu-id="4be15-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4be15-125">Requirements</span></span>



| <span data-ttu-id="4be15-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4be15-126">Requirement</span></span> | <span data-ttu-id="4be15-127">Value</span><span class="sxs-lookup"><span data-stu-id="4be15-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4be15-128">Versión</span><span class="sxs-lookup"><span data-stu-id="4be15-128">Version</span></span><br/> | <span data-ttu-id="4be15-129">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="4be15-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4be15-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4be15-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="4be15-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4be15-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4be15-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4be15-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4be15-133">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="4be15-133">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="4be15-134">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="4be15-134">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





