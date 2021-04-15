---
title: Método EnableTransport de la clase Win32_TSGatewayServerSettings
description: Habilita o deshabilita el transporte especificado.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- Método EnableTransport Servicios de Escritorio remoto
- Método EnableTransport Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método EnableTransport
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a14e7ee94eb02e1358d66b9965ecc2323d5b773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677014"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="9b60d-106">Método EnableTransport de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="9b60d-106">EnableTransport method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="9b60d-107">Habilita o deshabilita el transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="9b60d-107">Enables or disables the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b60d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b60d-108">Syntax</span></span>


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a><span data-ttu-id="9b60d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b60d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b60d-110">*TransportType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b60d-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b60d-111">Especifica el tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="9b60d-111">Specifies the transport type.</span></span> <span data-ttu-id="9b60d-112">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9b60d-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="9b60d-113">0</span><span class="sxs-lookup"><span data-stu-id="9b60d-113">0</span></span>
</dt> <dd>

<span data-ttu-id="9b60d-114">Transporte RPC a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="9b60d-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="9b60d-115">1</span><span class="sxs-lookup"><span data-stu-id="9b60d-115">1</span></span>
</dt> <dd>

<span data-ttu-id="9b60d-116">Transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="9b60d-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="9b60d-117">2</span><span class="sxs-lookup"><span data-stu-id="9b60d-117">2</span></span>
</dt> <dd>

<span data-ttu-id="9b60d-118">Transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="9b60d-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9b60d-119">*Habilitar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9b60d-119">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b60d-120">Especifica si el transporte está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9b60d-120">Specifies if the transport is enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b60d-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b60d-121">Return value</span></span>

<span data-ttu-id="9b60d-122">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="9b60d-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9b60d-123">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="9b60d-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9b60d-124">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9b60d-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b60d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b60d-125">Requirements</span></span>



| <span data-ttu-id="9b60d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b60d-126">Requirement</span></span> | <span data-ttu-id="9b60d-127">Value</span><span class="sxs-lookup"><span data-stu-id="9b60d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b60d-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b60d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9b60d-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9b60d-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9b60d-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b60d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9b60d-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b60d-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="9b60d-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b60d-132">Namespace</span></span><br/>                | <span data-ttu-id="9b60d-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9b60d-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9b60d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9b60d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b60d-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b60d-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b60d-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b60d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b60d-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b60d-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9b60d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b60d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b60d-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="9b60d-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





