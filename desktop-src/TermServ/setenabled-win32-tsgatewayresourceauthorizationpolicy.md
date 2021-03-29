---
title: Método SetEnabled de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Habilita o deshabilita la Directiva de autorización de recursos de Escritorio remoto (RD \ 160; RAP) estableciendo la propiedad Enabled.
ms.assetid: ee5830ba-36a1-4f28-a902-be5867439ada
ms.tgt_platform: multiple
keywords:
- Método SetEnabled Servicios de Escritorio remoto
- Método SetEnabled Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy Servicios de Escritorio remoto de clase, método SetEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de7c4e013690a5d5e8ffd6b235a42ea43c445ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492754"
---
# <a name="setenabled-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="3fb35-106">Método SetEnabled de la \_ clase TSGatewayResourceAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="3fb35-106">SetEnabled method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="3fb35-107">Habilita o deshabilita la Directiva de autorización de recursos de Escritorio remoto (RAP de RD) mediante el establecimiento de la propiedad **Enabled** .</span><span class="sxs-lookup"><span data-stu-id="3fb35-107">Enables or disables the Remote Desktop resource authorization policy (RD RAP) by setting the **Enabled** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb35-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fb35-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="3fb35-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fb35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb35-110">*Habilitado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3fb35-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb35-111">Si **es true**, se habilitará la rap de Rd.</span><span class="sxs-lookup"><span data-stu-id="3fb35-111">If **True**, the RD RAP will be enabled.</span></span> <span data-ttu-id="3fb35-112">Si **es false**, se deshabilitará la rap de Rd.</span><span class="sxs-lookup"><span data-stu-id="3fb35-112">If **False**, the RD RAP will be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb35-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fb35-113">Return value</span></span>

<span data-ttu-id="3fb35-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="3fb35-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3fb35-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="3fb35-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3fb35-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3fb35-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3fb35-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fb35-117">Remarks</span></span>

<span data-ttu-id="3fb35-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="3fb35-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3fb35-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3fb35-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3fb35-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3fb35-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3fb35-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="3fb35-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3fb35-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3fb35-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb35-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fb35-123">Requirements</span></span>



| <span data-ttu-id="3fb35-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb35-124">Requirement</span></span> | <span data-ttu-id="3fb35-125">Value</span><span class="sxs-lookup"><span data-stu-id="3fb35-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb35-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fb35-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb35-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3fb35-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3fb35-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fb35-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb35-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fb35-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3fb35-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3fb35-130">Namespace</span></span><br/>                | <span data-ttu-id="3fb35-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3fb35-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3fb35-132">MOF</span><span class="sxs-lookup"><span data-stu-id="3fb35-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fb35-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fb35-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fb35-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3fb35-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fb35-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fb35-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3fb35-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fb35-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb35-137">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="3fb35-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

