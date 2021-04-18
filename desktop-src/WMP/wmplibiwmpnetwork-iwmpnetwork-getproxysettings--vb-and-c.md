---
title: IWMPNetwork getProxySettings, método
description: El método getProxySettings devuelve información sobre la configuración de proxy para un protocolo.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- método getProxySettings de Windows Media Player
- método getProxySettings Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método getProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671180"
---
# <a name="iwmpnetworkgetproxysettings-method"></a><span data-ttu-id="41734-106">IWMPNetwork:: getProxySettings (método)</span><span class="sxs-lookup"><span data-stu-id="41734-106">IWMPNetwork::getProxySettings method</span></span>

<span data-ttu-id="41734-107">El método **getProxySettings** devuelve información sobre la configuración de proxy para un protocolo.</span><span class="sxs-lookup"><span data-stu-id="41734-107">The **getProxySettings** method returns information about the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="41734-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41734-108">Syntax</span></span>


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a><span data-ttu-id="41734-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41734-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41734-110">*bstrProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="41734-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41734-111">**System. String** que es el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="41734-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="41734-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="41734-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41734-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41734-113">Return value</span></span>

<span data-ttu-id="41734-114">**System. Int32** que es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="41734-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="41734-115">Value</span><span class="sxs-lookup"><span data-stu-id="41734-115">Value</span></span> | <span data-ttu-id="41734-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="41734-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="41734-117">0</span><span class="sxs-lookup"><span data-stu-id="41734-117">0</span></span>     | <span data-ttu-id="41734-118">No se utiliza un servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="41734-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="41734-119">1</span><span class="sxs-lookup"><span data-stu-id="41734-119">1</span></span>     | <span data-ttu-id="41734-120">Se está usando la configuración de proxy para el explorador actual (solo es válida para HTTP).</span><span class="sxs-lookup"><span data-stu-id="41734-120">The proxy settings for the current browser are being used (valid only for HTTP).</span></span> |
| <span data-ttu-id="41734-121">2</span><span class="sxs-lookup"><span data-stu-id="41734-121">2</span></span>     | <span data-ttu-id="41734-122">Se usa la configuración de proxy especificada manualmente.</span><span class="sxs-lookup"><span data-stu-id="41734-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="41734-123">3</span><span class="sxs-lookup"><span data-stu-id="41734-123">3</span></span>     | <span data-ttu-id="41734-124">La configuración de proxy se detecta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="41734-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="41734-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41734-125">Remarks</span></span>

<span data-ttu-id="41734-126">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="41734-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="41734-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="41734-127">Examples</span></span>

<span data-ttu-id="41734-128">En el ejemplo de código siguiente se usa **getProxySettings** para mostrar un mensaje que proporciona información sobre la configuración de proxy actual del reproductor en una etiqueta.</span><span class="sxs-lookup"><span data-stu-id="41734-128">The following code example uses **getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in a label.</span></span> <span data-ttu-id="41734-129">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="41734-129">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a><span data-ttu-id="41734-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41734-130">Requirements</span></span>



| <span data-ttu-id="41734-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="41734-131">Requirement</span></span> | <span data-ttu-id="41734-132">Value</span><span class="sxs-lookup"><span data-stu-id="41734-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41734-133">Versión</span><span class="sxs-lookup"><span data-stu-id="41734-133">Version</span></span><br/>   | <span data-ttu-id="41734-134">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="41734-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="41734-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="41734-135">Namespace</span></span><br/> | <span data-ttu-id="41734-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="41734-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="41734-137">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="41734-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="41734-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="41734-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41734-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="41734-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41734-140">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="41734-140">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="41734-141">**IWMPNetwork. setProxySettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="41734-141">**IWMPNetwork.setProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





