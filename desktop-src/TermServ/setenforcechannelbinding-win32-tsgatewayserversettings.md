---
title: Método SetEnforceChannelBinding de la clase Win32_TSGatewayServerSettings
description: Establece la propiedad EnforceChannelBinding.
ms.assetid: 8bd64fe7-bad5-44e6-a309-10802d9a8bd4
ms.tgt_platform: multiple
keywords:
- Método SetEnforceChannelBinding Servicios de Escritorio remoto
- Método SetEnforceChannelBinding Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método SetEnforceChannelBinding
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetEnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b236341f0fdac31f80f7e7d77aa12a4b22eb9731
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534413"
---
# <a name="setenforcechannelbinding-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="48c65-106">Método SetEnforceChannelBinding de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="48c65-106">SetEnforceChannelBinding method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="48c65-107">Establece la propiedad **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="48c65-107">Sets the **EnforceChannelBinding** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="48c65-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48c65-108">Syntax</span></span>


```mof
uint32 SetEnforceChannelBinding(
  [in] boolean EnforceChannelBinding
);
```



## <a name="parameters"></a><span data-ttu-id="48c65-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48c65-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48c65-110">*EnforceChannelBinding* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="48c65-110">*EnforceChannelBinding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c65-111">Especifica el nuevo valor de la propiedad **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="48c65-111">Specifies the new **EnforceChannelBinding** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48c65-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48c65-112">Return value</span></span>

<span data-ttu-id="48c65-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="48c65-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="48c65-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="48c65-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="48c65-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="48c65-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48c65-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48c65-116">Requirements</span></span>



| <span data-ttu-id="48c65-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="48c65-117">Requirement</span></span> | <span data-ttu-id="48c65-118">Value</span><span class="sxs-lookup"><span data-stu-id="48c65-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48c65-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48c65-119">Minimum supported client</span></span><br/> | <span data-ttu-id="48c65-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="48c65-120">None supported</span></span><br/>                                                                |
| <span data-ttu-id="48c65-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48c65-121">Minimum supported server</span></span><br/> | <span data-ttu-id="48c65-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48c65-122">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="48c65-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="48c65-123">Namespace</span></span><br/>                | <span data-ttu-id="48c65-124">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="48c65-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="48c65-125">MOF</span><span class="sxs-lookup"><span data-stu-id="48c65-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48c65-126"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48c65-126"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="48c65-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48c65-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48c65-128"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48c65-128"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="48c65-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="48c65-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c65-130">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="48c65-130">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





