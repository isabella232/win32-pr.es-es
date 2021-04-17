---
title: Network. getProxyPort (método)
description: El método getProxyPort recupera el puerto del proxy que se está usando.
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- método getProxyPort de Windows Media Player
- método getProxyPort Windows Media Player, clase de red
- Clase de red Windows Media Player, método getProxyPort
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3114b2188c0ccb0f6c260df33461fb117e7851e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708656"
---
# <a name="networkgetproxyport-method"></a><span data-ttu-id="5ee24-106">Network. getProxyPort (método)</span><span class="sxs-lookup"><span data-stu-id="5ee24-106">Network.getProxyPort method</span></span>

<span data-ttu-id="5ee24-107">El método **getProxyPort** recupera el puerto del proxy que se está usando.</span><span class="sxs-lookup"><span data-stu-id="5ee24-107">The **getProxyPort** method retrieves the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee24-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ee24-108">Syntax</span></span>


```JScript
retVal = Network.getProxyPort(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="5ee24-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ee24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ee24-110">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5ee24-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee24-111">**Cadena** que especifica el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="5ee24-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="5ee24-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="5ee24-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ee24-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ee24-113">Return value</span></span>

<span data-ttu-id="5ee24-114">Este método devuelve un **número** (**largo**) que contiene el puerto del proxy que se está usando.</span><span class="sxs-lookup"><span data-stu-id="5ee24-114">This method returns a **Number** (**long**) containing the proxy port being used.</span></span> <span data-ttu-id="5ee24-115">El valor devuelto solo es significativo cuando **getProxySettings** devuelve un valor de dos (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="5ee24-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ee24-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ee24-116">Remarks</span></span>

<span data-ttu-id="5ee24-117">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="5ee24-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="5ee24-118">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="5ee24-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="5ee24-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5ee24-119">Examples</span></span>

<span data-ttu-id="5ee24-120">En el siguiente ejemplo de JScript se usa *Network*. **getProxyPort** para mostrar los números de puerto de proxy de Windows Media Player actuales para los protocolos MMS y http.</span><span class="sxs-lookup"><span data-stu-id="5ee24-120">The following JScript example uses *Network*.**getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="5ee24-121">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5ee24-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

```



## <a name="requirements"></a><span data-ttu-id="5ee24-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ee24-122">Requirements</span></span>



| <span data-ttu-id="5ee24-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ee24-123">Requirement</span></span> | <span data-ttu-id="5ee24-124">Value</span><span class="sxs-lookup"><span data-stu-id="5ee24-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee24-125">Versión</span><span class="sxs-lookup"><span data-stu-id="5ee24-125">Version</span></span><br/> | <span data-ttu-id="5ee24-126">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5ee24-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5ee24-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ee24-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ee24-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ee24-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ee24-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ee24-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee24-130">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="5ee24-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="5ee24-131">**Network. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="5ee24-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





