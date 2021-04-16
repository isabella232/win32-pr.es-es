---
title: Network. getProxySettings (método)
description: El método getProxySettings recupera la configuración del proxy para un protocolo determinado.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- método getProxySettings de Windows Media Player
- método getProxySettings Windows Media Player, clase de red
- Clase de red Windows Media Player, método getProxySettings
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649845"
---
# <a name="networkgetproxysettings-method"></a><span data-ttu-id="a1508-106">Network. getProxySettings (método)</span><span class="sxs-lookup"><span data-stu-id="a1508-106">Network.getProxySettings method</span></span>

<span data-ttu-id="a1508-107">El método **getProxySettings** recupera la configuración del proxy para un protocolo determinado.</span><span class="sxs-lookup"><span data-stu-id="a1508-107">The **getProxySettings** method retrieves the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1508-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1508-108">Syntax</span></span>


```JScript
retVal = Network.getProxySettings(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="a1508-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1508-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1508-110">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a1508-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1508-111">**Cadena** que especifica el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="a1508-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="a1508-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a1508-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1508-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1508-113">Return value</span></span>

<span data-ttu-id="a1508-114">Este método devuelve un **número** (**Long**) que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a1508-114">This method returns a **Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="a1508-115">Value</span><span class="sxs-lookup"><span data-stu-id="a1508-115">Value</span></span> | <span data-ttu-id="a1508-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1508-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a1508-117">0</span><span class="sxs-lookup"><span data-stu-id="a1508-117">0</span></span>     | <span data-ttu-id="a1508-118">No se utiliza un servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="a1508-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="a1508-119">1</span><span class="sxs-lookup"><span data-stu-id="a1508-119">1</span></span>     | <span data-ttu-id="a1508-120">Se está usando la configuración de proxy del explorador actual (solo es válida para HTTP).</span><span class="sxs-lookup"><span data-stu-id="a1508-120">The proxy settings for the current browser are being used (only valid for HTTP).</span></span> |
| <span data-ttu-id="a1508-121">2</span><span class="sxs-lookup"><span data-stu-id="a1508-121">2</span></span>     | <span data-ttu-id="a1508-122">Se usa la configuración de proxy especificada manualmente.</span><span class="sxs-lookup"><span data-stu-id="a1508-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="a1508-123">3</span><span class="sxs-lookup"><span data-stu-id="a1508-123">3</span></span>     | <span data-ttu-id="a1508-124">La configuración de proxy se detecta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a1508-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="a1508-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1508-125">Remarks</span></span>

<span data-ttu-id="a1508-126">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="a1508-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="a1508-127">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="a1508-127">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="a1508-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a1508-128">Examples</span></span>

<span data-ttu-id="a1508-129">En el siguiente ejemplo de JScript se usa *Network*. **getProxySettings** para mostrar un mensaje que proporciona información sobre la configuración del proxy actual del reproductor, en la ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="a1508-129">The following JScript example uses *Network*.**getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in the browser window.</span></span> <span data-ttu-id="a1508-130">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a1508-130">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

```



## <a name="requirements"></a><span data-ttu-id="a1508-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1508-131">Requirements</span></span>



| <span data-ttu-id="a1508-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1508-132">Requirement</span></span> | <span data-ttu-id="a1508-133">Value</span><span class="sxs-lookup"><span data-stu-id="a1508-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1508-134">Versión</span><span class="sxs-lookup"><span data-stu-id="a1508-134">Version</span></span><br/> | <span data-ttu-id="a1508-135">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a1508-135">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a1508-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1508-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="a1508-137"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1508-137"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1508-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1508-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1508-139">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="a1508-139">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





