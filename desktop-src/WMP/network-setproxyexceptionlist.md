---
title: Network. setProxyExceptionList (método)
description: El método setProxyExceptionList especifica la lista de excepciones de proxy. | Network. setProxyExceptionList (método)
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- método setProxyExceptionList de Windows Media Player
- método setProxyExceptionList Windows Media Player, clase de red
- Clase de red Windows Media Player, método setProxyExceptionList
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698540"
---
# <a name="networksetproxyexceptionlist-method"></a><span data-ttu-id="1702e-107">Network. setProxyExceptionList (método)</span><span class="sxs-lookup"><span data-stu-id="1702e-107">Network.setProxyExceptionList method</span></span>

<span data-ttu-id="1702e-108">El método **setProxyExceptionList** especifica la lista de excepciones de proxy.</span><span class="sxs-lookup"><span data-stu-id="1702e-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1702e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1702e-109">Syntax</span></span>


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a><span data-ttu-id="1702e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1702e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1702e-111">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1702e-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1702e-112">**Cadena** que especifica el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="1702e-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="1702e-113">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="1702e-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="1702e-114">*lista* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1702e-114">*list* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1702e-115">**Cadena** que especifica una lista delimitada por signos de punto y coma de hosts para los que se omite el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="1702e-115">**String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1702e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1702e-116">Return value</span></span>

<span data-ttu-id="1702e-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1702e-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1702e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1702e-118">Remarks</span></span>

<span data-ttu-id="1702e-119">Esta es una lista de equipos, dominios y/o direcciones que omitirán el servidor proxy cuando la parte del host de la dirección URL de destino coincida con una entrada de la lista.</span><span class="sxs-lookup"><span data-stu-id="1702e-119">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="1702e-120">El \* carácter se puede usar como comodín para enumerar entradas.</span><span class="sxs-lookup"><span data-stu-id="1702e-120">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="1702e-121">Por ejemplo, \* . com coincidiría con todos los hosts del dominio com, mientras \* que 67. coincidiría con todos los hosts de la clase 67 A la subred.</span><span class="sxs-lookup"><span data-stu-id="1702e-121">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="1702e-122">Este método no tiene ningún efecto a menos que **getProxySettings** devuelva un valor de 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="1702e-122">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="1702e-123">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="1702e-123">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="1702e-124">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="1702e-124">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="1702e-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1702e-125">Examples</span></span>

<span data-ttu-id="1702e-126">En el siguiente ejemplo de JScript se usa *Network*. **setProxyExceptionList** para especificar una lista de hosts para los que se omite el servidor proxy cuando se usa el protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="1702e-126">The following JScript example uses *Network*.**setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="1702e-127">La nueva lista se recupera de un elemento de texto HTML con ID = "XLIST".</span><span class="sxs-lookup"><span data-stu-id="1702e-127">The new list is retrieved from an HTML TEXT element with ID = "XLIST".</span></span> <span data-ttu-id="1702e-128">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="1702e-128">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="1702e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1702e-129">Requirements</span></span>



| <span data-ttu-id="1702e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1702e-130">Requirement</span></span> | <span data-ttu-id="1702e-131">Value</span><span class="sxs-lookup"><span data-stu-id="1702e-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1702e-132">Versión</span><span class="sxs-lookup"><span data-stu-id="1702e-132">Version</span></span><br/> | <span data-ttu-id="1702e-133">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1702e-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1702e-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1702e-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="1702e-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1702e-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1702e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="1702e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1702e-137">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="1702e-137">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





