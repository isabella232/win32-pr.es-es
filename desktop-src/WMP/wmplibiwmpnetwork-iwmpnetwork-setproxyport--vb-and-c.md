---
title: IWMPNetwork setProxyPort, método
description: El método setProxyPort especifica el puerto del proxy que se va a usar. | IWMPNetwork setProxyPort, método
ms.assetid: df4b33f6-52b5-437f-ade2-0d08ca2878a9
keywords:
- método setProxyPort de Windows Media Player
- método setProxyPort Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método setProxyPort
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d171fa1afc129dd1d13c1d9d12d71c4370cba9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709118"
---
# <a name="iwmpnetworksetproxyport-method"></a><span data-ttu-id="7d8a3-107">IWMPNetwork:: setProxyPort (método)</span><span class="sxs-lookup"><span data-stu-id="7d8a3-107">IWMPNetwork::setProxyPort method</span></span>

<span data-ttu-id="7d8a3-108">El método **setProxyPort** especifica el puerto del proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7d8a3-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8a3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d8a3-109">Syntax</span></span>


```CSharp
public void setProxyPort(
  System.String bstrProtocol,
  System.Int32 lProxyPort
);
```


```VB

Public Sub setProxyPort( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxyPort As System.Int32 _
)
Implements IWMPNetwork.setProxyPort
```





## <a name="parameters"></a><span data-ttu-id="7d8a3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d8a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d8a3-111">*bstrProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d8a3-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d8a3-112">**System. String** que es el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="7d8a3-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="7d8a3-113">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="7d8a3-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d8a3-114">*lProxyPort* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d8a3-114">*lProxyPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d8a3-115">**System. Int32** que es el puerto del proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7d8a3-115">A **System.Int32** that is the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d8a3-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d8a3-116">Return value</span></span>

<span data-ttu-id="7d8a3-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7d8a3-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d8a3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d8a3-118">Remarks</span></span>

<span data-ttu-id="7d8a3-119">Este método no tiene ningún efecto a menos que el valor recuperado de **IWMPNetwork. getProxySettings** es 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="7d8a3-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="7d8a3-120">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="7d8a3-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="7d8a3-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7d8a3-121">Examples</span></span>

<span data-ttu-id="7d8a3-122">En el ejemplo de código siguiente se usa **setProxyPort** para especificar el número de puerto del proxy de Windows Media Player para el protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="7d8a3-122">The following code example uses **setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="7d8a3-123">El número de puerto se recupera de un cuadro de texto cuando se hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="7d8a3-123">The port number is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="7d8a3-124">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="7d8a3-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyPort_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy port number.
        int portnumber = System.Convert.ToInt32(portText.Text);

        // Set the proxy port.
        player.network.setProxyPort("MMS", portnumber);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyPort_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyPort.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy port number.
        Dim portnumber As Integer = System.Convert.ToInt32(portText.Text)

        &#39; Set the proxy port.
        player.network.setProxyPort(&quot;MMS&quot;, portnumber)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="7d8a3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d8a3-125">Requirements</span></span>



| <span data-ttu-id="7d8a3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d8a3-126">Requirement</span></span> | <span data-ttu-id="7d8a3-127">Value</span><span class="sxs-lookup"><span data-stu-id="7d8a3-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8a3-128">Versión</span><span class="sxs-lookup"><span data-stu-id="7d8a3-128">Version</span></span><br/>   | <span data-ttu-id="7d8a3-129">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="7d8a3-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7d8a3-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7d8a3-130">Namespace</span></span><br/> | <span data-ttu-id="7d8a3-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7d8a3-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7d8a3-132">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="7d8a3-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7d8a3-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7d8a3-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d8a3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d8a3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8a3-135">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7d8a3-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7d8a3-136">**IWMPNetwork. getProxyPort (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7d8a3-136">**IWMPNetwork.getProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7d8a3-137">**IWMPNetwork. getProxySettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7d8a3-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





