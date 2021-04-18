---
title: IWMPNetwork getProxyExceptionList, método
description: El método getProxyExceptionList devuelve la lista de excepciones de proxy.
ms.assetid: 1b209d75-0fa7-420e-831c-160f3826cf3a
keywords:
- método getProxyExceptionList de Windows Media Player
- método getProxyExceptionList Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método getProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402e3b28d5423314b499213c9ddb02bca482d629
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670424"
---
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a><span data-ttu-id="f4e6b-106">IWMPNetwork:: getProxyExceptionList (método)</span><span class="sxs-lookup"><span data-stu-id="f4e6b-106">IWMPNetwork::getProxyExceptionList method</span></span>

<span data-ttu-id="f4e6b-107">El método **getProxyExceptionList** devuelve la lista de excepciones de proxy.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-107">The **getProxyExceptionList** method returns the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e6b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4e6b-108">Syntax</span></span>


```CSharp
public System.String getProxyExceptionList(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyExceptionList( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="f4e6b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4e6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e6b-110">*bstrProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f4e6b-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4e6b-111">**System. String** que es el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="f4e6b-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f4e6b-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e6b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4e6b-113">Return value</span></span>

<span data-ttu-id="f4e6b-114">**System. String** que es una lista de hosts delimitados por punto y coma para los que se omite el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-114">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="f4e6b-115">El valor solo es significativo cuando **IWMPNetwork. getProxySettings** devuelve un valor de 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="f4e6b-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e6b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4e6b-116">Remarks</span></span>

<span data-ttu-id="f4e6b-117">Esta es una lista de equipos, dominios y/o direcciones que omitirán el servidor proxy cuando la parte del host de la dirección URL de destino coincida con una entrada de la lista.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="f4e6b-118">El \* carácter se puede usar como carácter comodín para enumerar entradas.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-118">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="f4e6b-119">Por ejemplo, \* . com coincidiría con todos los hosts del dominio com, mientras \* que 67. coincidiría con todos los hosts de la clase 67 A la subred.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-119">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="f4e6b-120">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="f4e6b-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f4e6b-121">Examples</span></span>

<span data-ttu-id="f4e6b-122">En el ejemplo de código siguiente se usa **getProxyExceptionList** para mostrar si Windows Media Player está establecido para omitir el servidor proxy para las direcciones locales.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-122">The following code example uses **getProxyExceptionList** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="f4e6b-123">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="f4e6b-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyExceptionListHTTP = "";
string proxyExceptionListMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyExceptionListHTTP = player.network.getProxyExceptionList("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyExceptionListMMS = player.network.getProxyExceptionList("MMS");
}

// Store the proxy exception lists in a string array and display them
// using a multi-line text box. Unavailable exception lists will display
// as "undefined".
proxyExList[0] = ("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
proxyExList[1] = ("The current MMS proxy exception list: " + proxyExceptionListMMS);
proxyExceptionListText.Lines = proxyExList;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyExceptionListHTTP As String = &quot;&quot;
Dim proxyExceptionListMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyExceptionListHTTP = player.network.getProxyExceptionList(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyExceptionListMMS = player.network.getProxyExceptionList(&quot;MMS&quot;)

End If

&#39; Store the proxy exception lists in a string array and display them
&#39; using a multi-line text box. Unavailable exception lists will display
&#39; as &quot;undefined&quot;.
proxyExList(0) = (&quot;The current HTTP proxy exception list: &quot; + proxyExceptionListHTTP)
proxyExList(1) = (&quot;The current MMS proxy exception list: &quot; + proxyExceptionListMMS)
proxyExceptionList.Lines = proxyExList
```





## <a name="requirements"></a><span data-ttu-id="f4e6b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4e6b-124">Requirements</span></span>



| <span data-ttu-id="f4e6b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4e6b-125">Requirement</span></span> | <span data-ttu-id="f4e6b-126">Value</span><span class="sxs-lookup"><span data-stu-id="f4e6b-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e6b-127">Versión</span><span class="sxs-lookup"><span data-stu-id="f4e6b-127">Version</span></span><br/>   | <span data-ttu-id="f4e6b-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="f4e6b-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f4e6b-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f4e6b-129">Namespace</span></span><br/> | <span data-ttu-id="f4e6b-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f4e6b-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f4e6b-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="f4e6b-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f4e6b-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e6b-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e6b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4e6b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e6b-134">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f4e6b-134">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4e6b-135">**IWMPNetwork. getProxySettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f4e6b-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4e6b-136">**IWMPNetwork. setProxyExceptionList (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f4e6b-136">**IWMPNetwork.setProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





