---
title: IWMPNetwork setProxyName, método
description: El método setProxyName especifica el nombre del servidor proxy que se va a usar. | IWMPNetwork setProxyName, método
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- método setProxyName de Windows Media Player
- método setProxyName Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método setProxyName
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9759f37dd4c0e171c09afaea4dfde0993c7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650204"
---
# <a name="iwmpnetworksetproxyname-method"></a><span data-ttu-id="ae7d6-107">IWMPNetwork:: setProxyName (método)</span><span class="sxs-lookup"><span data-stu-id="ae7d6-107">IWMPNetwork::setProxyName method</span></span>

<span data-ttu-id="ae7d6-108">El método **setProxyName** especifica el nombre del servidor proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7d6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae7d6-109">Syntax</span></span>


```CSharp
public void setProxyName(
  System.String bstrProtocol,
  System.String bstrProxyName
);
```


```VB

Public Sub setProxyName( _
  ByVal bstrProtocol As System.String, _
  ByVal bstrProxyName As System.String _
)
Implements IWMPNetwork.setProxyName
```





## <a name="parameters"></a><span data-ttu-id="ae7d6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae7d6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae7d6-111">*bstrProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae7d6-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7d6-112">**System. String** que es el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="ae7d6-113">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="ae7d6-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae7d6-114">*bstrProxyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae7d6-114">*bstrProxyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae7d6-115">**System. String** que es el nombre del servidor proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-115">A **System.String** that is the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae7d6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae7d6-116">Return value</span></span>

<span data-ttu-id="ae7d6-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae7d6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae7d6-118">Remarks</span></span>

<span data-ttu-id="ae7d6-119">Este método no tiene ningún efecto a menos que el valor recuperado de **IWMPNetwork. getProxySettings** es 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="ae7d6-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="ae7d6-120">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="ae7d6-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ae7d6-121">Examples</span></span>

<span data-ttu-id="ae7d6-122">En el ejemplo de código siguiente se usa **setProxyName** para especificar el nombre del servidor proxy de Windows Media Player para el protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-122">The following code example uses **setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="ae7d6-123">El nuevo nombre se recupera de un cuadro de texto cuando se hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-123">The new name is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="ae7d6-124">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="ae7d6-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyName_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy name.
        string proxyname = nameText.Text;

        // Set the proxy name.
        player.network.setProxyName("MMS", proxyname);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyName.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy name.
        Dim proxyname As String = nameText.Text

        &#39; Set the proxy name.
        player.network.setProxyName(&quot;MMS&quot;, proxyname)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ae7d6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae7d6-125">Requirements</span></span>



| <span data-ttu-id="ae7d6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae7d6-126">Requirement</span></span> | <span data-ttu-id="ae7d6-127">Value</span><span class="sxs-lookup"><span data-stu-id="ae7d6-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7d6-128">Versión</span><span class="sxs-lookup"><span data-stu-id="ae7d6-128">Version</span></span><br/>   | <span data-ttu-id="ae7d6-129">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="ae7d6-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ae7d6-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae7d6-130">Namespace</span></span><br/> | <span data-ttu-id="ae7d6-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ae7d6-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ae7d6-132">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ae7d6-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ae7d6-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ae7d6-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae7d6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae7d6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae7d6-135">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ae7d6-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ae7d6-136">**IWMPNetwork. getProxyName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ae7d6-136">**IWMPNetwork.getProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ae7d6-137">**IWMPNetwork. getProxySettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ae7d6-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





