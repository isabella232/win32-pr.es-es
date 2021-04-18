---
title: Método CheckStatus de la clase Win32_TSGatewayConnection
description: Comprueba el estado de una conexión de servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) con otro equipo y determina si el equipo de destino está configurado para el equilibrio de carga.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- Método CheckStatus Servicios de Escritorio remoto
- Método CheckStatus Servicios de Escritorio remoto, clase Win32_TSGatewayConnection
- Win32_TSGatewayConnection de clase Servicios de Escritorio remoto, método CheckStatus
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685906"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="86b89-106">Método CheckStatus de la \_ clase TSGatewayConnection de Win32</span><span class="sxs-lookup"><span data-stu-id="86b89-106">CheckStatus method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="86b89-107">Comprueba el estado de una conexión de servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) con otro equipo y determina si el equipo de destino está configurado para el equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="86b89-107">Checks the status of a Remote Desktop Gateway (RD Gateway) server connection to another computer, and determines whether the target computer is configured for load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="86b89-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86b89-108">Syntax</span></span>


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a><span data-ttu-id="86b89-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86b89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86b89-110">*NombreDeServidor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86b89-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86b89-111">Nombre del servidor de puerta de enlace de escritorio remoto de origen desde el que se comprueba la conexión.</span><span class="sxs-lookup"><span data-stu-id="86b89-111">The name of the source RD Gateway server from which the connection is checked.</span></span>

</dd> <dt>

<span data-ttu-id="86b89-112">*EndPointName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="86b89-112">*EndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86b89-113">Nombre del servidor de destino (el punto de conexión) al que se comprueba el acceso desde el servidor de origen.</span><span class="sxs-lookup"><span data-stu-id="86b89-113">The name of the target server (the endpoint) to which access is checked from the source server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86b89-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86b89-114">Return value</span></span>

<span data-ttu-id="86b89-115">Este método devuelve los siguientes valores devueltos posibles.</span><span class="sxs-lookup"><span data-stu-id="86b89-115">This method returns the following possible return values.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="86b89-116">0</span><span class="sxs-lookup"><span data-stu-id="86b89-116">0</span></span>

<span data-ttu-id="86b89-117">El estado de la conexión es correcto.</span><span class="sxs-lookup"><span data-stu-id="86b89-117">The connection status is OK.</span></span> <span data-ttu-id="86b89-118">El punto de conexión es accesible y está configurado para el equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="86b89-118">The endpoint is reachable and is configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="86b89-119">1</span><span class="sxs-lookup"><span data-stu-id="86b89-119">1</span></span>

<span data-ttu-id="86b89-120">Se desconoce el estado de la conexión.</span><span class="sxs-lookup"><span data-stu-id="86b89-120">The connection status is unknown.</span></span> <span data-ttu-id="86b89-121">Lo más probable es que se produzca una excepción.</span><span class="sxs-lookup"><span data-stu-id="86b89-121">Most likely, an exception occurred.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="86b89-122">0x80075c34</span><span class="sxs-lookup"><span data-stu-id="86b89-122">0x80075c34</span></span>

<span data-ttu-id="86b89-123">No se puede tener acceso al punto de conexión o no está configurado para el equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="86b89-123">The endpoint is either not reachable, or it is not configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="86b89-124">0x80075c32</span><span class="sxs-lookup"><span data-stu-id="86b89-124">0x80075c32</span></span>

<span data-ttu-id="86b89-125">Se produjo un error de estado.</span><span class="sxs-lookup"><span data-stu-id="86b89-125">A status error occurred.</span></span> <span data-ttu-id="86b89-126">El extremo es accesible, pero el servicio de equilibrio de carga de RPC/HTTP (RPCHTTPLBS) no se ha iniciado en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="86b89-126">The endpoint is reachable, but the RPC/HTTP Load Balancing Service (RPCHTTPLBS) service is not started on the target computer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86b89-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86b89-127">Remarks</span></span>

<span data-ttu-id="86b89-128">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="86b89-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="86b89-129">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="86b89-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="86b89-130">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="86b89-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="86b89-131">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="86b89-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="86b89-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86b89-132">Requirements</span></span>



| <span data-ttu-id="86b89-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="86b89-133">Requirement</span></span> | <span data-ttu-id="86b89-134">Value</span><span class="sxs-lookup"><span data-stu-id="86b89-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86b89-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86b89-135">Minimum supported client</span></span><br/> | <span data-ttu-id="86b89-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="86b89-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="86b89-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86b89-137">Minimum supported server</span></span><br/> | <span data-ttu-id="86b89-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86b89-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="86b89-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="86b89-139">Namespace</span></span><br/>                | <span data-ttu-id="86b89-140">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="86b89-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="86b89-141">MOF</span><span class="sxs-lookup"><span data-stu-id="86b89-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86b89-142"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86b89-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="86b89-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86b89-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86b89-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86b89-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="86b89-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="86b89-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b89-146">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="86b89-146">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

