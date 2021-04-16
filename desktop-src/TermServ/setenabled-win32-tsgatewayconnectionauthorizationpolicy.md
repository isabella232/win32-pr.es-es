---
title: Método SetEnabled de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad habilitada, que habilita o deshabilita la Directiva de autorización de conexión Servicios de Escritorio remoto actual (RD \ 160; CAP).
ms.assetid: f8c0b39e-95d4-46cf-83fb-e91b650fbb4d
ms.tgt_platform: multiple
keywords:
- Método SetEnabled Servicios de Escritorio remoto
- Método SetEnabled Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy Servicios de Escritorio remoto de clase, método SetEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6584e8916db2f8070def3904d0ece6ec0ee5ae34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534077"
---
# <a name="setenabled-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="e488d-106">Método SetEnabled de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="e488d-106">SetEnabled method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="e488d-107">Establece la propiedad **habilitada** , que habilita o deshabilita la Directiva de autorización de conexión servicios de escritorio remoto actual (Cap de RD).</span><span class="sxs-lookup"><span data-stu-id="e488d-107">Sets the **Enabled** property, which enables or disables the current Remote Desktop Services connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="e488d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e488d-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="e488d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e488d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e488d-110">*Habilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e488d-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e488d-111">**True** si se va a habilitar la Cap de Rd, **false** si se va a deshabilitar la Cap de Rd.</span><span class="sxs-lookup"><span data-stu-id="e488d-111">**True** if the RD CAP is to be enabled, **False** if the RD CAP is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e488d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e488d-112">Return value</span></span>

<span data-ttu-id="e488d-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e488d-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e488d-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="e488d-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e488d-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e488d-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e488d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e488d-116">Remarks</span></span>

<span data-ttu-id="e488d-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="e488d-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e488d-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e488d-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e488d-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e488d-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e488d-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="e488d-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e488d-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e488d-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e488d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e488d-122">Requirements</span></span>



| <span data-ttu-id="e488d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e488d-123">Requirement</span></span> | <span data-ttu-id="e488d-124">Value</span><span class="sxs-lookup"><span data-stu-id="e488d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e488d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e488d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e488d-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e488d-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e488d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e488d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e488d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e488d-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e488d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e488d-129">Namespace</span></span><br/>                | <span data-ttu-id="e488d-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e488d-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e488d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e488d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e488d-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e488d-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e488d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e488d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e488d-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e488d-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e488d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e488d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e488d-136">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="e488d-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

