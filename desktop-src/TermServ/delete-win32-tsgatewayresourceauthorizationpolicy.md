---
title: Método Delete de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Elimina la Directiva de autorización de recursos de Escritorio remoto actual (RD \ 160; RAP).
ms.assetid: cbabb997-63b8-4a4c-9e16-34f2638fca97
ms.tgt_platform: multiple
keywords:
- Eliminar método Servicios de Escritorio remoto
- Método Delete Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Clase Win32_TSGatewayResourceAuthorizationPolicy Servicios de Escritorio remoto, método Delete
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396a766fb307d1e8a912d614147a2bff2bd924c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422020"
---
# <a name="delete-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="d1254-106">Método Delete de la \_ clase Win32 TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="d1254-106">Delete method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="d1254-107">Elimina la Directiva de autorización de recursos de Escritorio remoto actual (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="d1254-107">Deletes the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1254-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1254-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="d1254-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1254-109">Parameters</span></span>

<span data-ttu-id="d1254-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d1254-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1254-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1254-111">Return value</span></span>

<span data-ttu-id="d1254-112">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="d1254-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d1254-113">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d1254-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d1254-114">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d1254-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d1254-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1254-115">Remarks</span></span>

<span data-ttu-id="d1254-116">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="d1254-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d1254-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d1254-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d1254-118">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d1254-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d1254-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d1254-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d1254-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d1254-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1254-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1254-121">Requirements</span></span>



| <span data-ttu-id="d1254-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1254-122">Requirement</span></span> | <span data-ttu-id="d1254-123">Value</span><span class="sxs-lookup"><span data-stu-id="d1254-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1254-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1254-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d1254-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d1254-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d1254-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1254-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d1254-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1254-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d1254-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d1254-128">Namespace</span></span><br/>                | <span data-ttu-id="d1254-129">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d1254-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d1254-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d1254-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1254-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1254-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1254-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1254-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1254-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1254-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d1254-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1254-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1254-135">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="d1254-135">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

