---
title: IWMPNetwork setProxyBypassForLocal, método
description: El método setProxyBypassForLocal especifica si el servidor proxy se omite si el servidor de origen está en una red local.
ms.assetid: b308957a-0d7e-45be-8625-db198b276dad
keywords:
- método setProxyBypassForLocal de Windows Media Player
- método setProxyBypassForLocal Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método setProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f869125d43529a039804fe28c0f0dc493f481e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708905"
---
# <a name="iwmpnetworksetproxybypassforlocal-method"></a><span data-ttu-id="b061b-106">IWMPNetwork:: setProxyBypassForLocal (método)</span><span class="sxs-lookup"><span data-stu-id="b061b-106">IWMPNetwork::setProxyBypassForLocal method</span></span>

<span data-ttu-id="b061b-107">El método **setProxyBypassForLocal** especifica si el servidor proxy se omite si el servidor de origen está en una red local.</span><span class="sxs-lookup"><span data-stu-id="b061b-107">The **setProxyBypassForLocal** method specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="b061b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b061b-108">Syntax</span></span>


```CSharp
public void setProxyBypassForLocal(
  System.String bstrProtocol,
  System.Boolean fBypassForLocal
);
```


```VB

Public Sub setProxyBypassForLocal( _
  ByVal bstrProtocol As System.String, _
  ByVal fBypassForLocal As System.Boolean _
)
Implements IWMPNetwork.setProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="b061b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b061b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b061b-110">*bstrProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b061b-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b061b-111">**System. String** que es el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="b061b-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="b061b-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="b061b-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="b061b-113">*fBypassForLocal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b061b-113">*fBypassForLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b061b-114">Valor **System. Boolean** que indica si se omite el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="b061b-114">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b061b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b061b-115">Return value</span></span>

<span data-ttu-id="b061b-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b061b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b061b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b061b-117">Remarks</span></span>

<span data-ttu-id="b061b-118">Este método no tiene ningún efecto a menos que el valor recuperado de **IWMPNetwork. getProxySettings** es 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="b061b-118">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="b061b-119">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="b061b-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="b061b-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b061b-120">Examples</span></span>

<span data-ttu-id="b061b-121">En el ejemplo de código siguiente se usa **setProxyBypassForLocal** para especificar si se omite el servidor proxy de Windows Media Player, cuando se usa el protocolo MMS, si el servidor de origen está en una red local.</span><span class="sxs-lookup"><span data-stu-id="b061b-121">The following code example uses **setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="b061b-122">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="b061b-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Prepare a message, a caption and buttons for the user prompt.
string message = ("Bypass proxy server for local addresses?");
string caption = "Proxy Settings";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.YesNo;

// Test whether the proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    // Prompt the user for a setting. 
    System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

    // Store the return value of the DialogResult in a boolean variable.
    bool proxybypass;
    
    if(result == System.Windows.Forms.DialogResult.Yes)
    {
        proxybypass = true;
    }
    else
    {
        proxybypass = false;
    }

    // Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal("MMS", proxybypass);
}
else
{
    // Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
}
```


```VB

' Prepare a message, a caption and buttons for the user prompt.
Dim message As String = &quot;Bypass proxy server for local addresses?&quot;
Dim caption As String = &quot;Proxy Settings&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.YesNo

&#39; Test whether the proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    &#39; Prompt the user for a setting. 
    Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

    &#39; Store the return value of the DialogResult as a boolean.
    Dim proxybypass As Boolean

    If (result = System.Windows.Forms.DialogResult.Yes) Then

        proxybypass = True

    Else

        proxybypass = False

    End If

    &#39; Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal(&quot;MMS&quot;, proxybypass)

Else

    &#39; Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="b061b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b061b-123">Requirements</span></span>



| <span data-ttu-id="b061b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b061b-124">Requirement</span></span> | <span data-ttu-id="b061b-125">Value</span><span class="sxs-lookup"><span data-stu-id="b061b-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b061b-126">Versión</span><span class="sxs-lookup"><span data-stu-id="b061b-126">Version</span></span><br/>   | <span data-ttu-id="b061b-127">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="b061b-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b061b-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b061b-128">Namespace</span></span><br/> | <span data-ttu-id="b061b-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b061b-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b061b-130">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="b061b-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b061b-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b061b-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b061b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b061b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b061b-133">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b061b-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b061b-134">**IWMPNetwork. getProxyBypassForLocal (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b061b-134">**IWMPNetwork.getProxyBypassForLocal (VB and C#)**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b061b-135">**IWMPNetwork. getProxySettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b061b-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





