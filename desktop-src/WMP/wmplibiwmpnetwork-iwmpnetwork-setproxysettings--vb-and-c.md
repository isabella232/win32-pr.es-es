---
title: IWMPNetwork setProxySettings, método
description: El método setProxySettings especifica la configuración de proxy para un protocolo.
ms.assetid: 6e410812-a06c-4911-8291-1d654fcd281a
keywords:
- método setProxySettings de Windows Media Player
- método setProxySettings Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método setProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7fc36c12335cf97ad7bff34924850155f2fd747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650203"
---
# <a name="iwmpnetworksetproxysettings-method"></a><span data-ttu-id="f5207-106">IWMPNetwork:: setProxySettings (método)</span><span class="sxs-lookup"><span data-stu-id="f5207-106">IWMPNetwork::setProxySettings method</span></span>

<span data-ttu-id="f5207-107">El método **setProxySettings** especifica la configuración de proxy para un protocolo.</span><span class="sxs-lookup"><span data-stu-id="f5207-107">The **setProxySettings** method specifies the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5207-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5207-108">Syntax</span></span>


```CSharp
public void setProxySettings(
  System.String bstrProtocol,
  System.Int32 lProxySetting
);
```


```VB

Public Sub setProxySettings( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxySetting As System.Int32 _
)
Implements IWMPNetwork.setProxySettings
```





## <a name="parameters"></a><span data-ttu-id="f5207-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5207-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5207-110">*bstrProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5207-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5207-111">**System. String** que es el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="f5207-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="f5207-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f5207-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5207-113">*lProxySetting* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5207-113">*lProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5207-114">**System. Int32** que es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f5207-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="f5207-115">Value</span><span class="sxs-lookup"><span data-stu-id="f5207-115">Value</span></span> | <span data-ttu-id="f5207-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5207-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="f5207-117">0</span><span class="sxs-lookup"><span data-stu-id="f5207-117">0</span></span>     | <span data-ttu-id="f5207-118">No usar ningún servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="f5207-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="f5207-119">1</span><span class="sxs-lookup"><span data-stu-id="f5207-119">1</span></span>     | <span data-ttu-id="f5207-120">Use la configuración de proxy del explorador actual (solo es válida para HTTP).</span><span class="sxs-lookup"><span data-stu-id="f5207-120">Use the proxy settings of the current browser (valid only for HTTP).</span></span> |
| <span data-ttu-id="f5207-121">2</span><span class="sxs-lookup"><span data-stu-id="f5207-121">2</span></span>     | <span data-ttu-id="f5207-122">Utilice la configuración de proxy especificada manualmente.</span><span class="sxs-lookup"><span data-stu-id="f5207-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="f5207-123">3</span><span class="sxs-lookup"><span data-stu-id="f5207-123">3</span></span>     | <span data-ttu-id="f5207-124">Detectar automáticamente la configuración de proxy.</span><span class="sxs-lookup"><span data-stu-id="f5207-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5207-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5207-125">Return value</span></span>

<span data-ttu-id="f5207-126">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f5207-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5207-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5207-127">Remarks</span></span>

<span data-ttu-id="f5207-128">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="f5207-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="f5207-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f5207-129">Examples</span></span>

<span data-ttu-id="f5207-130">En el ejemplo de código siguiente se usa un cuadro de lista para permitir al usuario establecer la configuración del proxy de Windows Media Player para el protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5207-130">The following code example uses a list box to allow the user to set the Windows Media Player proxy setting for the HTTP protocol.</span></span> <span data-ttu-id="f5207-131">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="f5207-131">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the proxy settings in order so that their index in the
// list box matches their value.
proxySettings.Items.Add("Do not use a proxy server.  (Value = 0)");                                             
proxySettings.Items.Add("Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)");
proxySettings.Items.Add("Use the manually specified proxy settings.  (Value = 2)");
proxySettings.Items.Add("Auto-detect the proxy settings.  (Value = 3)");                                       

// Change the proxy setting for the HTTP protocol when the user makes a list box selection.
private void proxySettings_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the setting from the ListBox
    int setting = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Change the proxy setting. 
    player.network.setProxySettings("HTTP", setting);
}
```


```VB

' Load the list box with the proxy settings in order so that their index in the
&#39; list box matches their value.
proxySettings.Items.Add(&quot;Do not use a proxy server.  (Value = 0)&quot;)
proxySettings.Items.Add(&quot;Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)&quot;)
proxySettings.Items.Add(&quot;Use the manually specified proxy settings.  (Value = 2)&quot;)
proxySettings.Items.Add(&quot;Auto-detect the proxy settings.  (Value = 3)&quot;)

&#39; Change the proxy setting for the HTTP protocol when the user makes a list box selection.
Public Sub proxySettings_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles proxySettings.SelectedIndexChanged

    &#39; Store the index of the setting from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim setting As Integer = lb.SelectedIndex

    &#39; Change the proxy setting. 
    player.network.setProxySettings(&quot;HTTP&quot;, setting)
    
End Sub
```





## <a name="requirements"></a><span data-ttu-id="f5207-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5207-132">Requirements</span></span>



| <span data-ttu-id="f5207-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5207-133">Requirement</span></span> | <span data-ttu-id="f5207-134">Value</span><span class="sxs-lookup"><span data-stu-id="f5207-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5207-135">Versión</span><span class="sxs-lookup"><span data-stu-id="f5207-135">Version</span></span><br/>   | <span data-ttu-id="f5207-136">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="f5207-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f5207-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f5207-137">Namespace</span></span><br/> | <span data-ttu-id="f5207-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f5207-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f5207-139">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="f5207-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f5207-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f5207-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5207-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5207-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5207-142">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f5207-142">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f5207-143">**IWMPNetwork. getProxySettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="f5207-143">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





