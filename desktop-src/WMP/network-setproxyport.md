---
title: Network. setProxyPort (método)
description: El método setProxyPort especifica el puerto del proxy que se va a usar. | Network. setProxyPort (método)
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- método setProxyPort de Windows Media Player
- método setProxyPort Windows Media Player, clase de red
- Clase de red Windows Media Player, método setProxyPort
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698496"
---
# <a name="networksetproxyport-method"></a><span data-ttu-id="9b5fa-107">Network. setProxyPort (método)</span><span class="sxs-lookup"><span data-stu-id="9b5fa-107">Network.setProxyPort method</span></span>

<span data-ttu-id="9b5fa-108">El método **setProxyPort** especifica el puerto del proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9b5fa-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b5fa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b5fa-109">Syntax</span></span>


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a><span data-ttu-id="9b5fa-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b5fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b5fa-111">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9b5fa-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b5fa-112">**Cadena** que especifica el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="9b5fa-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="9b5fa-113">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="9b5fa-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b5fa-114">*Puerto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9b5fa-114">*port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b5fa-115">**Número** (**largo**) que especifica el puerto del proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9b5fa-115">**Number** (**long**) specifying the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b5fa-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b5fa-116">Return value</span></span>

<span data-ttu-id="9b5fa-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9b5fa-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b5fa-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b5fa-118">Remarks</span></span>

<span data-ttu-id="9b5fa-119">Este método no tiene ningún efecto a menos que **getProxySettings** devuelva un valor de 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="9b5fa-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="9b5fa-120">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="9b5fa-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="9b5fa-121">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="9b5fa-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="9b5fa-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9b5fa-122">Examples</span></span>

<span data-ttu-id="9b5fa-123">En el siguiente ejemplo de JScript se usa *Network*. **setProxyPort** para especificar el número de puerto del proxy de Windows Media Player para el protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="9b5fa-123">The following JScript example uses *Network*.**setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="9b5fa-124">El número de puerto se recupera de un elemento de entrada HTML con ID = "PORT".</span><span class="sxs-lookup"><span data-stu-id="9b5fa-124">The port number is retrieved from an HTML INPUT element with ID = "PORT".</span></span> <span data-ttu-id="9b5fa-125">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9b5fa-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="9b5fa-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b5fa-126">Requirements</span></span>



| <span data-ttu-id="9b5fa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b5fa-127">Requirement</span></span> | <span data-ttu-id="9b5fa-128">Value</span><span class="sxs-lookup"><span data-stu-id="9b5fa-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5fa-129">Versión</span><span class="sxs-lookup"><span data-stu-id="9b5fa-129">Version</span></span><br/> | <span data-ttu-id="9b5fa-130">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9b5fa-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9b5fa-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b5fa-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="9b5fa-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b5fa-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b5fa-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b5fa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b5fa-134">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="9b5fa-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





