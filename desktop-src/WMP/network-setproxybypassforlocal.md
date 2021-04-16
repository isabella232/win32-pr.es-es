---
title: Network. setProxyBypassForLocal (método)
description: El método setProxyBypassForLocal especifica un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- método setProxyBypassForLocal de Windows Media Player
- método setProxyBypassForLocal Windows Media Player, clase de red
- Clase de red Windows Media Player, método setProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699744"
---
# <a name="networksetproxybypassforlocal-method"></a><span data-ttu-id="d870e-106">Network. setProxyBypassForLocal (método)</span><span class="sxs-lookup"><span data-stu-id="d870e-106">Network.setProxyBypassForLocal method</span></span>

<span data-ttu-id="d870e-107">El método **setProxyBypassForLocal** especifica un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.</span><span class="sxs-lookup"><span data-stu-id="d870e-107">The **setProxyBypassForLocal** method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="d870e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d870e-108">Syntax</span></span>


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a><span data-ttu-id="d870e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d870e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d870e-110">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d870e-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d870e-111">**Cadena** que especifica el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="d870e-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="d870e-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="d870e-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="d870e-113">*omitir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d870e-113">*bypass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d870e-114">**Valor booleano** que especifica si se omite el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="d870e-114">**Boolean** specifying whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d870e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d870e-115">Return value</span></span>

<span data-ttu-id="d870e-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d870e-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d870e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d870e-117">Remarks</span></span>

<span data-ttu-id="d870e-118">Este método no tiene ningún efecto a menos que **getProxySettings** devuelva un valor de 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="d870e-118">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="d870e-119">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="d870e-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="d870e-120">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="d870e-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="d870e-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d870e-121">Examples</span></span>

<span data-ttu-id="d870e-122">En el siguiente ejemplo de JScript se usa *Network*. **setProxyBypassForLocal** para especificar si se omite el servidor proxy de Windows Media Player, cuando se usa el protocolo MMS, si el servidor de origen está en una red local.</span><span class="sxs-lookup"><span data-stu-id="d870e-122">The following JScript example uses *Network*.**setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="d870e-123">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d870e-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="d870e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d870e-124">Requirements</span></span>



| <span data-ttu-id="d870e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d870e-125">Requirement</span></span> | <span data-ttu-id="d870e-126">Value</span><span class="sxs-lookup"><span data-stu-id="d870e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d870e-127">Versión</span><span class="sxs-lookup"><span data-stu-id="d870e-127">Version</span></span><br/> | <span data-ttu-id="d870e-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d870e-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d870e-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d870e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="d870e-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d870e-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d870e-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d870e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d870e-132">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="d870e-132">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





