---
title: Método IsTransportEnabled de la clase Win32_TSGatewayServerSettings
description: Determina si el transporte especificado está habilitado.
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- Método IsTransportEnabled Servicios de Escritorio remoto
- Método IsTransportEnabled Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método IsTransportEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da152499138f6c1aba1ff6477c719aa0e787deee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150214"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="1c630-106">Método IsTransportEnabled de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="1c630-106">IsTransportEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="1c630-107">Determina si el transporte especificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1c630-107">Determines whether the specified transport is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c630-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c630-108">Syntax</span></span>


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="1c630-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c630-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c630-110">*TransportType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c630-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c630-111">Especifica el tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="1c630-111">Specifies the transport type.</span></span> <span data-ttu-id="1c630-112">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1c630-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="1c630-113">0</span><span class="sxs-lookup"><span data-stu-id="1c630-113">0</span></span>
</dt> <dd>

<span data-ttu-id="1c630-114">Transporte RPC a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="1c630-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="1c630-115">1</span><span class="sxs-lookup"><span data-stu-id="1c630-115">1</span></span>
</dt> <dd>

<span data-ttu-id="1c630-116">Transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="1c630-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="1c630-117">2</span><span class="sxs-lookup"><span data-stu-id="1c630-117">2</span></span>
</dt> <dd>

<span data-ttu-id="1c630-118">Transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="1c630-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1c630-119">*Habilitado* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c630-119">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c630-120">Valor **booleano** que indica si el transporte está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1c630-120">A **boolean** value that indicates whether the transport is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c630-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c630-121">Return value</span></span>

<span data-ttu-id="1c630-122">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="1c630-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1c630-123">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="1c630-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1c630-124">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1c630-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c630-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c630-125">Requirements</span></span>



| <span data-ttu-id="1c630-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c630-126">Requirement</span></span> | <span data-ttu-id="1c630-127">Value</span><span class="sxs-lookup"><span data-stu-id="1c630-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c630-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c630-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1c630-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1c630-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1c630-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c630-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1c630-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1c630-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="1c630-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1c630-132">Namespace</span></span><br/>                | <span data-ttu-id="1c630-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1c630-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1c630-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1c630-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c630-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c630-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c630-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c630-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c630-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c630-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1c630-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c630-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c630-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="1c630-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





