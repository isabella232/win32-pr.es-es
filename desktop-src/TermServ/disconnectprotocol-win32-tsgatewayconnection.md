---
title: Método DisconnectProtocol de la clase Win32_TSGatewayConnection
description: Desconecta todas las conexiones del protocolo especificado del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 0ca3f478-dfdc-404e-ac17-43b6873b7256
ms.tgt_platform: multiple
keywords:
- Método DisconnectProtocol Servicios de Escritorio remoto
- Método DisconnectProtocol Servicios de Escritorio remoto, clase Win32_TSGatewayConnection
- Win32_TSGatewayConnection de clase Servicios de Escritorio remoto, método DisconnectProtocol
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectProtocol
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a37050cbd622c6fea14b8b4e5dc6a414eaad85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359763"
---
# <a name="disconnectprotocol-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="2e838-106">Método DisconnectProtocol de la \_ clase TSGatewayConnection de Win32</span><span class="sxs-lookup"><span data-stu-id="2e838-106">DisconnectProtocol method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="2e838-107">Desconecta todas las conexiones del protocolo especificado del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="2e838-107">Disconnects all connections of the specified protocol from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e838-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e838-108">Syntax</span></span>


```mof
uint32 DisconnectProtocol(
  [in] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="2e838-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e838-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e838-110">*ProtocolName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e838-110">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e838-111">El nombre de protocolo para una conexión específica.</span><span class="sxs-lookup"><span data-stu-id="2e838-111">The protocol name for a specific connection.</span></span> <span data-ttu-id="2e838-112">Se puede recuperar de la propiedad **ProtocolName** de la clase **\_ TSGatewayConnection de Win32** .</span><span class="sxs-lookup"><span data-stu-id="2e838-112">This can be retrieved from the **ProtocolName** property of the **Win32\_TSGatewayConnection** class.</span></span>

<dt>

<span data-ttu-id="2e838-113">TS</span><span class="sxs-lookup"><span data-stu-id="2e838-113">"TS"</span></span>
</dt> <dd>

<span data-ttu-id="2e838-114">El protocolo para el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2e838-114">The protocol for the RD Gateway server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e838-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e838-115">Return value</span></span>

<span data-ttu-id="2e838-116">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="2e838-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2e838-117">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2e838-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2e838-118">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2e838-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e838-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e838-119">Remarks</span></span>

<span data-ttu-id="2e838-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="2e838-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2e838-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2e838-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2e838-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2e838-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2e838-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2e838-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2e838-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2e838-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e838-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e838-125">Requirements</span></span>



| <span data-ttu-id="2e838-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e838-126">Requirement</span></span> | <span data-ttu-id="2e838-127">Value</span><span class="sxs-lookup"><span data-stu-id="2e838-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e838-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e838-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2e838-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2e838-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2e838-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e838-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2e838-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e838-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2e838-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e838-132">Namespace</span></span><br/>                | <span data-ttu-id="2e838-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2e838-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2e838-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2e838-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e838-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e838-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e838-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e838-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e838-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e838-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2e838-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e838-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e838-139">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="2e838-139">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

