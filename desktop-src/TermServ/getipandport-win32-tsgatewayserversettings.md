---
title: Método GetIPAndPort de la clase Win32_TSGatewayServerSettings
description: Obtiene la dirección IP de escucha y el número de puerto para el transporte especificado.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- Método GetIPAndPort Servicios de Escritorio remoto
- Método GetIPAndPort Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método GetIPAndPort
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359690"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="62378-106">Método GetIPAndPort de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="62378-106">GetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="62378-107">Obtiene la dirección IP de escucha y el número de puerto para el transporte especificado.</span><span class="sxs-lookup"><span data-stu-id="62378-107">Obtains the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="62378-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62378-108">Syntax</span></span>


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
);
```



## <a name="parameters"></a><span data-ttu-id="62378-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62378-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62378-110">*TransportType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62378-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62378-111">Especifica el tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="62378-111">Specifies the transport type.</span></span> <span data-ttu-id="62378-112">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="62378-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="62378-113">0</span><span class="sxs-lookup"><span data-stu-id="62378-113">0</span></span>
</dt> <dd>

<span data-ttu-id="62378-114">Transporte RPC a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="62378-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="62378-115">1</span><span class="sxs-lookup"><span data-stu-id="62378-115">1</span></span>
</dt> <dd>

<span data-ttu-id="62378-116">Transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="62378-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="62378-117">2</span><span class="sxs-lookup"><span data-stu-id="62378-117">2</span></span>
</dt> <dd>

<span data-ttu-id="62378-118">Transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="62378-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="62378-119">*Dirección IP* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="62378-119">*IPAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62378-120">Una cadena que recibe la dirección IP de escucha, en forma de octeto (por ejemplo, "192.168.1.1").</span><span class="sxs-lookup"><span data-stu-id="62378-120">A string that receives the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="62378-121">*Puerto* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="62378-121">*Port* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62378-122">Especifica el número de puerto de escucha.</span><span class="sxs-lookup"><span data-stu-id="62378-122">Specifies the listening port number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62378-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62378-123">Return value</span></span>

<span data-ttu-id="62378-124">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="62378-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="62378-125">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="62378-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="62378-126">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="62378-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62378-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62378-127">Requirements</span></span>



| <span data-ttu-id="62378-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="62378-128">Requirement</span></span> | <span data-ttu-id="62378-129">Value</span><span class="sxs-lookup"><span data-stu-id="62378-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62378-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62378-130">Minimum supported client</span></span><br/> | <span data-ttu-id="62378-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="62378-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="62378-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62378-132">Minimum supported server</span></span><br/> | <span data-ttu-id="62378-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62378-133">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="62378-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="62378-134">Namespace</span></span><br/>                | <span data-ttu-id="62378-135">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="62378-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="62378-136">MOF</span><span class="sxs-lookup"><span data-stu-id="62378-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62378-137"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62378-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="62378-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62378-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62378-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62378-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="62378-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="62378-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62378-141">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="62378-141">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





