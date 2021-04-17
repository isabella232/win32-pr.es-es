---
title: Network. setProxyName (método)
description: El método setProxyName especifica el nombre del servidor proxy que se va a usar. | Network. setProxyName (método)
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- método setProxyName de Windows Media Player
- método setProxyName Windows Media Player, clase de red
- Clase de red Windows Media Player, método setProxyName
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699813"
---
# <a name="networksetproxyname-method"></a><span data-ttu-id="78de6-107">Network. setProxyName (método)</span><span class="sxs-lookup"><span data-stu-id="78de6-107">Network.setProxyName method</span></span>

<span data-ttu-id="78de6-108">El método **setProxyName** especifica el nombre del servidor proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="78de6-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="78de6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78de6-109">Syntax</span></span>


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="78de6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78de6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78de6-111">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="78de6-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78de6-112">**Cadena** que especifica el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="78de6-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="78de6-113">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="78de6-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="78de6-114">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="78de6-114">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78de6-115">**Cadena** que especifica el nombre del servidor proxy que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="78de6-115">**String** specifying the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78de6-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78de6-116">Return value</span></span>

<span data-ttu-id="78de6-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="78de6-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78de6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78de6-118">Remarks</span></span>

<span data-ttu-id="78de6-119">Este método no tiene ningún efecto a menos que **getProxySettings** devuelva un valor de 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="78de6-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="78de6-120">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="78de6-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="78de6-121">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="78de6-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="78de6-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="78de6-122">Examples</span></span>

<span data-ttu-id="78de6-123">En el siguiente ejemplo de JScript se usa *Network*. **setProxyName** para especificar el nombre del servidor proxy de Windows Media Player para el protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="78de6-123">The following JScript example uses *Network*.**setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="78de6-124">El nuevo nombre se recupera de un elemento de texto HTML con ID = "NAME".</span><span class="sxs-lookup"><span data-stu-id="78de6-124">The new name is retrieved from an HTML TEXT element with ID = "NAME".</span></span> <span data-ttu-id="78de6-125">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="78de6-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="78de6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78de6-126">Requirements</span></span>



| <span data-ttu-id="78de6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="78de6-127">Requirement</span></span> | <span data-ttu-id="78de6-128">Value</span><span class="sxs-lookup"><span data-stu-id="78de6-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="78de6-129">Versión</span><span class="sxs-lookup"><span data-stu-id="78de6-129">Version</span></span><br/> | <span data-ttu-id="78de6-130">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="78de6-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="78de6-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78de6-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="78de6-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78de6-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78de6-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="78de6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78de6-134">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="78de6-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





