---
title: IWMPNetwork getProxyPort, método
description: El método getProxyPort devuelve el puerto del proxy que se está usando.
ms.assetid: fc94f3a9-458d-410c-98e9-a34be6e08c52
keywords:
- método getProxyPort de Windows Media Player
- método getProxyPort Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método getProxyPort
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46fb388c2740e709e75579c01d216af677a826c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671181"
---
# <a name="iwmpnetworkgetproxyport-method"></a><span data-ttu-id="f395b-106">IWMPNetwork:: getProxyPort (método)</span><span class="sxs-lookup"><span data-stu-id="f395b-106">IWMPNetwork::getProxyPort method</span></span>

<span data-ttu-id="f395b-107">El método **getProxyPort** devuelve el puerto del proxy que se está usando.</span><span class="sxs-lookup"><span data-stu-id="f395b-107">The **getProxyPort** method returns the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="f395b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f395b-108">Syntax</span></span>


```CSharp
public System.Int32 getProxyPort(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyPort( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxyPort
```





## <a name="parameters"></a><span data-ttu-id="f395b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f395b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f395b-110">*bstrProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f395b-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f395b-111">**System. String** que es el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="f395b-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="f395b-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f395b-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f395b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f395b-113">Return value</span></span>

<span data-ttu-id="f395b-114">**System. Int32** que es el puerto del proxy que se está usando.</span><span class="sxs-lookup"><span data-stu-id="f395b-114">A **System.Int32** that is the proxy port being used.</span></span> <span data-ttu-id="f395b-115">El valor solo es significativo cuando **IWMPNetwork. getProxySettings** devuelve un valor de 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="f395b-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="f395b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f395b-116">Remarks</span></span>

<span data-ttu-id="f395b-117">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="f395b-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="f395b-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f395b-118">Examples</span></span>

<span data-ttu-id="f395b-119">En el ejemplo de código siguiente se usa **getProxyPort** para mostrar los números de puerto de proxy de Windows Media Player actuales para los protocolos MMS y http.</span><span class="sxs-lookup"><span data-stu-id="f395b-119">The following code example uses **getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="f395b-120">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="f395b-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Variables to hold the results of calls to getProxyPort. 
int proxyPortHTTP = 0;
int proxyPortMMS = 0;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyPortHTTP = player.network.getProxyPort("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyPortMMS = player.network.getProxyPort("MMS");
}

// Store the proxy port numbers in a string array and display them using a multi-line
// text box. Unavailable proxy port numbers will display as "undefined".
proxyPorts[0] = ("The current HTTP proxy port is: " + proxyPortHTTP.ToString());
proxyPorts[1] = ("The current MMS proxy port is: " + proxyPortMMS.ToString());
proxyPortText.Lines = proxyPorts;
```


```VB

' Variables to hold the results of calls to getProxyPort. 
Dim proxyPortHTTP As Integer = 0
Dim proxyPortMMS As Integer = 0

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyPortHTTP = player.network.getProxyPort(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyPortMMS = player.network.getProxyPort(&quot;MMS&quot;)

End If

&#39; Store the proxy port numbers in a string array and display them using a multi-line
&#39; text box. Unavailable proxy port numbers will display as &quot;undefined&quot;.
proxyPorts(0) = (&quot;The current HTTP proxy port is: &quot; + proxyPortHTTP.ToString())
proxyPorts(1) = (&quot;The current MMS proxy port is: &quot; + proxyPortMMS.ToString())
proxyPortText.Lines = proxyPorts
```





## <a name="requirements"></a><span data-ttu-id="f395b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f395b-121">Requirements</span></span>



| <span data-ttu-id="f395b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f395b-122">Requirement</span></span> | <span data-ttu-id="f395b-123">Value</span><span class="sxs-lookup"><span data-stu-id="f395b-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f395b-124">Versión</span><span class="sxs-lookup"><span data-stu-id="f395b-124">Version</span></span><br/>   | <span data-ttu-id="f395b-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="f395b-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f395b-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f395b-126">Namespace</span></span><br/> | <span data-ttu-id="f395b-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f395b-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f395b-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="f395b-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f395b-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f395b-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f395b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f395b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f395b-131">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f395b-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f395b-132">**IWMPNetwork. getProxySettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f395b-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f395b-133">**IWMPNetwork. setProxyPort (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f395b-133">**IWMPNetwork.setProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)
</dt> </dl>

 

 





