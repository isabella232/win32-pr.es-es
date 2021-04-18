---
title: IWMPNetwork getProxyName, método
description: El método getProxyName devuelve el nombre del servidor proxy que se está usando.
ms.assetid: 69396b01-1da7-450c-b229-0cc4fb832ae9
keywords:
- método getProxyName de Windows Media Player
- método getProxyName Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método getProxyName
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5e05b6552e5e6a922cf02037a0bfc4956bfc28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670423"
---
# <a name="iwmpnetworkgetproxyname-method"></a><span data-ttu-id="dfd12-106">IWMPNetwork:: getProxyName (método)</span><span class="sxs-lookup"><span data-stu-id="dfd12-106">IWMPNetwork::getProxyName method</span></span>

<span data-ttu-id="dfd12-107">El método **getProxyName** devuelve el nombre del servidor proxy que se está usando.</span><span class="sxs-lookup"><span data-stu-id="dfd12-107">The **getProxyName** method returns the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd12-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfd12-108">Syntax</span></span>


```CSharp
public System.String getProxyName(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyName( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyName
```





## <a name="parameters"></a><span data-ttu-id="dfd12-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfd12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfd12-110">*bstrProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dfd12-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfd12-111">**System. String** que es el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="dfd12-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="dfd12-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="dfd12-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfd12-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfd12-113">Return value</span></span>

<span data-ttu-id="dfd12-114">**System. String** que es el nombre del servidor proxy que se está usando.</span><span class="sxs-lookup"><span data-stu-id="dfd12-114">A **System.String** that is the name of the proxy server being used.</span></span> <span data-ttu-id="dfd12-115">El valor solo es significativo cuando **IWMPNetwork. getProxySettings** devuelve un valor de 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="dfd12-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="dfd12-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfd12-116">Remarks</span></span>

<span data-ttu-id="dfd12-117">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="dfd12-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="dfd12-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dfd12-118">Examples</span></span>

<span data-ttu-id="dfd12-119">En el ejemplo de código siguiente se usa **getProxyName** para mostrar los nombres de servidor proxy de Windows Media Player para los protocolos http y MMS.</span><span class="sxs-lookup"><span data-stu-id="dfd12-119">The following code example uses **getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="dfd12-120">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="dfd12-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyNameHTTP = "";
string proxyNameMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyNameHTTP = player.network.getProxyName("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyNameMMS = player.network.getProxyName("MMS");
}

// Store the proxy server names in a string array and display them using a multi-line
// text box. Unavailable proxy server names will display as "undefined".
proxyNames[0] = ("The current HTTP proxy server name is: " + proxyNameHTTP);
proxyNames[1] = ("The current MMS proxy server name is: " + proxyNameMMS);
proxyNameText.Lines = proxyNames;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyNameHTTP As String = &quot;&quot;
Dim proxyNameMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyNameHTTP = player.network.getProxyName(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyNameMMS = player.network.getProxyName(&quot;MMS&quot;)

End If

&#39; Store the proxy server names in a string array and display them using a multi-line
&#39; text box. Unavailable proxy server names will display as &quot;undefined&quot;.
proxyNames(0) = (&quot;The current HTTP proxy server name is: &quot; + proxyNameHTTP)
proxyNames(1) = (&quot;The current MMS proxy server name is: &quot; + proxyNameMMS)
proxyNameText.Lines = proxyNames
```





## <a name="requirements"></a><span data-ttu-id="dfd12-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfd12-121">Requirements</span></span>



| <span data-ttu-id="dfd12-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfd12-122">Requirement</span></span> | <span data-ttu-id="dfd12-123">Value</span><span class="sxs-lookup"><span data-stu-id="dfd12-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd12-124">Versión</span><span class="sxs-lookup"><span data-stu-id="dfd12-124">Version</span></span><br/>   | <span data-ttu-id="dfd12-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="dfd12-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dfd12-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dfd12-126">Namespace</span></span><br/> | <span data-ttu-id="dfd12-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dfd12-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dfd12-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="dfd12-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dfd12-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dfd12-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfd12-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfd12-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd12-131">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dfd12-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dfd12-132">**IWMPNetwork. getProxySettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dfd12-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dfd12-133">**IWMPNetwork. setProxyName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dfd12-133">**IWMPNetwork.setProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)
</dt> </dl>

 

 





