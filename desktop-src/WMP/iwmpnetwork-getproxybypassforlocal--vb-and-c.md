---
title: IWMPNetwork getProxyBypassForLocal, método
description: El método getProxyBypassForLocal devuelve un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.
ms.assetid: 150a05f3-6979-4a88-a617-472f07d38807
keywords:
- método getProxyBypassForLocal de Windows Media Player
- método getProxyBypassForLocal Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método getProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b87b1f00432ec91dd4379a9fa5e31664437afe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690366"
---
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a><span data-ttu-id="b8057-106">IWMPNetwork:: getProxyBypassForLocal (método)</span><span class="sxs-lookup"><span data-stu-id="b8057-106">IWMPNetwork::getProxyBypassForLocal method</span></span>

<span data-ttu-id="b8057-107">El método **getProxyBypassForLocal** devuelve un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.</span><span class="sxs-lookup"><span data-stu-id="b8057-107">The **getProxyBypassForLocal** method returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8057-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8057-108">Syntax</span></span>


```CSharp
public System.Boolean getProxyBypassForLocal(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyBypassForLocal( _
  ByVal bstrProtocol As System.String _
) As System.Boolean
Implements IWMPNetwork.getProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="b8057-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8057-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8057-110">*bstrProtocol*</span><span class="sxs-lookup"><span data-stu-id="b8057-110">*bstrProtocol*</span></span> 
</dt> <dd>

<span data-ttu-id="b8057-111">**System. String** que es el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="b8057-111">A **System.String** that is the protocol name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8057-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8057-112">Return value</span></span>

<span data-ttu-id="b8057-113">Valor **System. Boolean** que indica si se omite el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="b8057-113">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span> <span data-ttu-id="b8057-114">El valor solo es significativo cuando **IWMPNetwork. getProxySettings** devuelve un valor de 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="b8057-114">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8057-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8057-115">Remarks</span></span>

<span data-ttu-id="b8057-116">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="b8057-116">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="b8057-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b8057-117">Examples</span></span>

<span data-ttu-id="b8057-118">En el ejemplo de código siguiente se usa **getProxyBypassForLocal** para mostrar si Windows Media Player está establecido para omitir el servidor proxy para las direcciones locales.</span><span class="sxs-lookup"><span data-stu-id="b8057-118">The following code example uses **getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="b8057-119">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="b8057-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```VB
' Boolean values to hold the results of calls to getProxyBypassForLocal. 
Dim proxyBypassForLocalHTTP As Boolean = False
Dim proxyBypassForLocalMMS As Boolean = False

' Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings("HTTP") = 2) Then

    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal("HTTP")

End If

' Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings("MMS") = 2) Then

    proxyBypassForLocalMMS = player.network.getProxyBypassForLocal("MMS")

End If

' Store the proxy bypass for local values in a string array and display them
' using a multi-line text box. Unavailable proxy bypass for local values will display
' as "undefined".
proxyInfo(0) = ("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP.ToString())
proxyInfo(1) = ("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS.ToString())
proxyBypassText.Lines = proxyInfo
```


```CSharp

// Boolean values to hold the results of calls to getProxyBypassForLocal. 
bool proxyBypassForLocalHTTP = false;
bool proxyBypassForLocalMMS = false;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings(&quot;HTTP&quot;) == 2)
{
    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal(&quot;HTTP&quot;);
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings(&quot;MMS&quot;) == 2)
{
   proxyBypassForLocalMMS = player.network.getProxyBypassForLocal(&quot;MMS&quot;);
}

// Store the proxy bypass for local values in a string array and display them
// using a multi-line text box. Unavailable proxy bypass for local values will display
// as &quot;undefined&quot;.
proxyInfo[0] = (&quot;The current HTTP proxy bypass for local value: &quot; + proxyBypassForLocalHTTP.ToString());
proxyInfo[1] = (&quot;The current MMS proxy bypass for local value: &quot; + proxyBypassForLocalMMS.ToString());
proxyBypassText.Lines = proxyInfo;
```





## <a name="requirements"></a><span data-ttu-id="b8057-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8057-120">Requirements</span></span>



| <span data-ttu-id="b8057-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8057-121">Requirement</span></span> | <span data-ttu-id="b8057-122">Value</span><span class="sxs-lookup"><span data-stu-id="b8057-122">Value</span></span> |
|----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8057-123">Versión</span><span class="sxs-lookup"><span data-stu-id="b8057-123">Version</span></span><br/>   | <span data-ttu-id="b8057-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="b8057-124">Windows Media Player 9 Series or later</span></span><br/>                                             |
| <span data-ttu-id="b8057-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8057-125">Namespace</span></span><br/> | <span data-ttu-id="b8057-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b8057-126">**WMPLib**</span></span><br/>                                                                         |
| <span data-ttu-id="b8057-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="b8057-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b8057-128"><dt>Interop.WMPLib.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8057-128"><dt>Interop.WMPLib.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8057-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8057-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8057-130">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b8057-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8057-131">**IWMPNetwork. getProxySettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b8057-131">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8057-132">**IWMPNetwork. setProxyBypassForLocal (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b8057-132">**IWMPNetwork.setProxyBypassForLocal (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





