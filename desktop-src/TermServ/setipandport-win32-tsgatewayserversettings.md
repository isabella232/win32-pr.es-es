---
title: Método SetIPAndPort de la clase Win32_TSGatewayServerSettings
description: Establece la dirección IP de escucha y el número de puerto para el transporte especificado.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- Método SetIPAndPort Servicios de Escritorio remoto
- Método SetIPAndPort Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método SetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534072"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="09a4e-106">Método SetIPAndPort de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="09a4e-106">SetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="09a4e-107">Establece la dirección IP de escucha y el número de puerto para el transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="09a4e-107">Sets the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="09a4e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09a4e-108">Syntax</span></span>


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
);
```



## <a name="parameters"></a><span data-ttu-id="09a4e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09a4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09a4e-110">*TransportType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09a4e-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a4e-111">Especifica el tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="09a4e-111">Specifies the transport type.</span></span> <span data-ttu-id="09a4e-112">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="09a4e-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="09a4e-113">0</span><span class="sxs-lookup"><span data-stu-id="09a4e-113">0</span></span>
</dt> <dd>

<span data-ttu-id="09a4e-114">Transporte RPC a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="09a4e-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="09a4e-115">1</span><span class="sxs-lookup"><span data-stu-id="09a4e-115">1</span></span>
</dt> <dd>

<span data-ttu-id="09a4e-116">Transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="09a4e-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="09a4e-117">2</span><span class="sxs-lookup"><span data-stu-id="09a4e-117">2</span></span>
</dt> <dd>

<span data-ttu-id="09a4e-118">Transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="09a4e-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="09a4e-119">*Dirección IP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09a4e-119">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a4e-120">Especifica la dirección IP de escucha, en forma de octeto (por ejemplo, "192.168.1.1").</span><span class="sxs-lookup"><span data-stu-id="09a4e-120">Specifies the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="09a4e-121">*Puerto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="09a4e-121">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a4e-122">Especifica el número de puerto de escucha.</span><span class="sxs-lookup"><span data-stu-id="09a4e-122">Specifies the listening port number.</span></span>

</dd> <dt>

<span data-ttu-id="09a4e-123">*OverrideExisting* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09a4e-123">*OverrideExisting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a4e-124">Indica si se va a invalidar el enlace IP/puerto existente para HTTP.</span><span class="sxs-lookup"><span data-stu-id="09a4e-124">Indicates whether to override the existing IP/Port binding for HTTP.</span></span> <span data-ttu-id="09a4e-125">Este parámetro solo se usa si el parámetro *TransportType* contiene 0 (RPC a través de http) o 1 (http).</span><span class="sxs-lookup"><span data-stu-id="09a4e-125">This parameter is only used if the *TransportType* parameter contains 0 (RPC over HTTP) or 1 (HTTP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09a4e-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09a4e-126">Return value</span></span>

<span data-ttu-id="09a4e-127">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="09a4e-127">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="09a4e-128">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="09a4e-128">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="09a4e-129">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="09a4e-129">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09a4e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09a4e-130">Requirements</span></span>



| <span data-ttu-id="09a4e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="09a4e-131">Requirement</span></span> | <span data-ttu-id="09a4e-132">Value</span><span class="sxs-lookup"><span data-stu-id="09a4e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a4e-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09a4e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="09a4e-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="09a4e-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="09a4e-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09a4e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="09a4e-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09a4e-136">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="09a4e-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="09a4e-137">Namespace</span></span><br/>                | <span data-ttu-id="09a4e-138">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="09a4e-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="09a4e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="09a4e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09a4e-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09a4e-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="09a4e-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09a4e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09a4e-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09a4e-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="09a4e-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="09a4e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a4e-144">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="09a4e-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





