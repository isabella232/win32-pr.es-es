---
title: Método Disconnect de la clase Win32_TSGatewayConnection
description: Desconecta la conexión del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 8c424e58-aa89-4ec6-acea-5b571d3f4c21
ms.tgt_platform: multiple
keywords:
- Desconectar método Servicios de Escritorio remoto
- Método Disconnect Servicios de Escritorio remoto, clase Win32_TSGatewayConnection
- Servicios de Escritorio remoto de clase Win32_TSGatewayConnection, método Disconnect
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.Disconnect
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53101e5ca3529c5033adc918f1f9ad11a3b45f7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801172"
---
# <a name="disconnect-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="cb27b-106">Método Disconnect de la \_ clase TSGatewayConnection de Win32</span><span class="sxs-lookup"><span data-stu-id="cb27b-106">Disconnect method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="cb27b-107">Desconecta la conexión del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="cb27b-107">Disconnects the connection from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb27b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb27b-108">Syntax</span></span>


```mof
uint32 Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="cb27b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb27b-109">Parameters</span></span>

<span data-ttu-id="cb27b-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cb27b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb27b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb27b-111">Return value</span></span>

<span data-ttu-id="cb27b-112">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cb27b-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="cb27b-113">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="cb27b-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="cb27b-114">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cb27b-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cb27b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb27b-115">Remarks</span></span>

<span data-ttu-id="cb27b-116">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="cb27b-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="cb27b-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cb27b-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cb27b-118">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cb27b-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cb27b-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="cb27b-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cb27b-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cb27b-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb27b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb27b-121">Requirements</span></span>



| <span data-ttu-id="cb27b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb27b-122">Requirement</span></span> | <span data-ttu-id="cb27b-123">Value</span><span class="sxs-lookup"><span data-stu-id="cb27b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb27b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb27b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cb27b-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cb27b-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="cb27b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb27b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cb27b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb27b-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="cb27b-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb27b-128">Namespace</span></span><br/>                | <span data-ttu-id="cb27b-129">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cb27b-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="cb27b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="cb27b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb27b-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb27b-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb27b-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb27b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb27b-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb27b-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cb27b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb27b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb27b-135">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="cb27b-135">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

