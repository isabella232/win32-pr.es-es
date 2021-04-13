---
title: Método SetSmartcardAllowed de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad SmartcardAllowed, que habilita o deshabilita la compatibilidad con el uso de una tarjeta inteligente para conectarse al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 9fe1c7a9-2bab-439f-8dc2-421ed876fcf7
ms.tgt_platform: multiple
keywords:
- Método SetSmartcardAllowed Servicios de Escritorio remoto
- Método SetSmartcardAllowed Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetSmartcardAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSmartcardAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022b5461086ae05f198cbce4faaee0e9c36bf77e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422466"
---
# <a name="setsmartcardallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="6a8f0-106">Método SetSmartcardAllowed de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="6a8f0-106">SetSmartcardAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="6a8f0-107">Establece la propiedad **SmartcardAllowed** , que habilita o deshabilita la compatibilidad con el uso de una tarjeta inteligente para conectarse al servidor de puerta de enlace de escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="6a8f0-107">Sets the **SmartcardAllowed** property, which enables or disables support for using a smart card to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a8f0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a8f0-108">Syntax</span></span>


```mof
uint32 SetSmartcardAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="6a8f0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a8f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a8f0-110">*Permitido* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a8f0-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8f0-111">Nuevo valor de **SmartcardAllowed** .</span><span class="sxs-lookup"><span data-stu-id="6a8f0-111">New **SmartcardAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a8f0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a8f0-112">Return value</span></span>

<span data-ttu-id="6a8f0-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="6a8f0-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6a8f0-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6a8f0-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6a8f0-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6a8f0-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a8f0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a8f0-116">Remarks</span></span>

<span data-ttu-id="6a8f0-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="6a8f0-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6a8f0-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6a8f0-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6a8f0-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6a8f0-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6a8f0-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="6a8f0-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6a8f0-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6a8f0-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a8f0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a8f0-122">Requirements</span></span>



| <span data-ttu-id="6a8f0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a8f0-123">Requirement</span></span> | <span data-ttu-id="6a8f0-124">Value</span><span class="sxs-lookup"><span data-stu-id="6a8f0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a8f0-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a8f0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6a8f0-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6a8f0-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6a8f0-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a8f0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6a8f0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a8f0-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6a8f0-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6a8f0-129">Namespace</span></span><br/>                | <span data-ttu-id="6a8f0-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6a8f0-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6a8f0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6a8f0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a8f0-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a8f0-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a8f0-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a8f0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a8f0-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a8f0-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6a8f0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a8f0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a8f0-136">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="6a8f0-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

