---
title: Método SetDescription de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Establece la propiedad Description para la Escritorio remoto Directiva de autorización de recursos (RD \ 160; RAP).
ms.assetid: 5a0f4c4b-50a4-4bd2-960f-8af7f4686d07
ms.tgt_platform: multiple
keywords:
- Método SetDescription Servicios de Escritorio remoto
- Método SetDescription Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetDescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dfdbcf67096dacc694061b5ff7e704c788bd2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422265"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="46752-106">Método SetDescription de la \_ clase TSGatewayResourceAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="46752-106">SetDescription method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="46752-107">Establece la propiedad **Description** de la Directiva de autorización de recursos de escritorio remoto (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="46752-107">Sets the **Description** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="46752-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46752-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="46752-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46752-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46752-110">*Descripción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="46752-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46752-111">Descripción de la RAP de RD.</span><span class="sxs-lookup"><span data-stu-id="46752-111">Description of the RD RAP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46752-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46752-112">Return value</span></span>

<span data-ttu-id="46752-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="46752-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="46752-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="46752-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="46752-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="46752-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="46752-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46752-116">Remarks</span></span>

<span data-ttu-id="46752-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="46752-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="46752-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="46752-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="46752-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="46752-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="46752-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="46752-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="46752-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="46752-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="46752-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46752-122">Requirements</span></span>



| <span data-ttu-id="46752-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="46752-123">Requirement</span></span> | <span data-ttu-id="46752-124">Value</span><span class="sxs-lookup"><span data-stu-id="46752-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46752-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46752-125">Minimum supported client</span></span><br/> | <span data-ttu-id="46752-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="46752-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="46752-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46752-127">Minimum supported server</span></span><br/> | <span data-ttu-id="46752-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46752-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="46752-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46752-129">Namespace</span></span><br/>                | <span data-ttu-id="46752-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="46752-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="46752-131">MOF</span><span class="sxs-lookup"><span data-stu-id="46752-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46752-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46752-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="46752-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46752-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46752-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46752-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="46752-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="46752-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46752-136">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="46752-136">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

