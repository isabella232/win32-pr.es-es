---
title: Network. setProxySettings (método)
description: El método setProxySettings especifica la configuración de proxy para un protocolo determinado.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- método setProxySettings de Windows Media Player
- método setProxySettings Windows Media Player, clase de red
- Clase de red Windows Media Player, método setProxySettings
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699321"
---
# <a name="networksetproxysettings-method"></a><span data-ttu-id="992bf-106">Network. setProxySettings (método)</span><span class="sxs-lookup"><span data-stu-id="992bf-106">Network.setProxySettings method</span></span>

<span data-ttu-id="992bf-107">El método **setProxySettings** especifica la configuración de proxy para un protocolo determinado.</span><span class="sxs-lookup"><span data-stu-id="992bf-107">The **setProxySettings** method specifies the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="992bf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="992bf-108">Syntax</span></span>


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a><span data-ttu-id="992bf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="992bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="992bf-110">*Protocolo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="992bf-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992bf-111">**Cadena** que especifica el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="992bf-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="992bf-112">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="992bf-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="992bf-113">*configuración* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="992bf-113">*setting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992bf-114">**Número** (**largo**) que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="992bf-114">**Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="992bf-115">Value</span><span class="sxs-lookup"><span data-stu-id="992bf-115">Value</span></span> | <span data-ttu-id="992bf-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="992bf-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="992bf-117">0</span><span class="sxs-lookup"><span data-stu-id="992bf-117">0</span></span>     | <span data-ttu-id="992bf-118">No usar ningún servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="992bf-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="992bf-119">1</span><span class="sxs-lookup"><span data-stu-id="992bf-119">1</span></span>     | <span data-ttu-id="992bf-120">Use la configuración de proxy del explorador actual (solo es válida para HTTP).</span><span class="sxs-lookup"><span data-stu-id="992bf-120">Use the proxy settings of the current browser (only valid for HTTP).</span></span> |
| <span data-ttu-id="992bf-121">2</span><span class="sxs-lookup"><span data-stu-id="992bf-121">2</span></span>     | <span data-ttu-id="992bf-122">Utilice la configuración de proxy especificada manualmente.</span><span class="sxs-lookup"><span data-stu-id="992bf-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="992bf-123">3</span><span class="sxs-lookup"><span data-stu-id="992bf-123">3</span></span>     | <span data-ttu-id="992bf-124">Detectar automáticamente la configuración de proxy.</span><span class="sxs-lookup"><span data-stu-id="992bf-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="992bf-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="992bf-125">Return value</span></span>

<span data-ttu-id="992bf-126">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="992bf-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="992bf-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="992bf-127">Remarks</span></span>

<span data-ttu-id="992bf-128">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="992bf-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="992bf-129">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="992bf-129">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="992bf-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="992bf-130">Examples</span></span>

<span data-ttu-id="992bf-131">En el ejemplo siguiente se usa JScript con un elemento SELECT de HTML **para permitir al usuario especificar la configuración del proxy de Windows Media Player para el protocolo http. El objeto Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="992bf-131">The following example uses JScript with an HTML SELECT **element to allow the user to specify the Windows Media Player proxy setting for the HTTP protocol. The Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="992bf-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="992bf-132">Requirements</span></span>



| <span data-ttu-id="992bf-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="992bf-133">Requirement</span></span> | <span data-ttu-id="992bf-134">Value</span><span class="sxs-lookup"><span data-stu-id="992bf-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="992bf-135">Versión</span><span class="sxs-lookup"><span data-stu-id="992bf-135">Version</span></span><br/> | <span data-ttu-id="992bf-136">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="992bf-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="992bf-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="992bf-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="992bf-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="992bf-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="992bf-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="992bf-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992bf-140">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="992bf-140">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





