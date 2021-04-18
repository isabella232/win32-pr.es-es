---
title: Método MoveUp de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Mueve la Directiva de autorización de conexión Escritorio remoto actual (RD \ 160; CAP) una posición hacia arriba en el orden en que RD \ 160; Se evalúan los extremos.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- MoveUp (método) Servicios de Escritorio remoto
- Método MoveUp Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Clase Win32_TSGatewayConnectionAuthorizationPolicy Servicios de Escritorio remoto, método MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81973261d156328aa1f306c26dd8bd9bdd20511f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492988"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="1e8a5-106">Método MoveUp de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="1e8a5-106">MoveUp method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="1e8a5-107">Mueve la Directiva de autorización de conexión de Escritorio remoto actual una posición hacia arriba en el orden en que se evalúan las Cap de RD.</span><span class="sxs-lookup"><span data-stu-id="1e8a5-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position up in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="1e8a5-108">Este método reduce la propiedad **Order** de la Cap de RD actual e incrementa la propiedad **Order** de la Cap de RD que precedía a la Cap de RD actual.</span><span class="sxs-lookup"><span data-stu-id="1e8a5-108">This method decrements the **Order** property of the current RD CAP and increments the **Order** property of the RD CAP that preceded the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e8a5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e8a5-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="1e8a5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e8a5-110">Parameters</span></span>

<span data-ttu-id="1e8a5-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1e8a5-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e8a5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e8a5-112">Return value</span></span>

<span data-ttu-id="1e8a5-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="1e8a5-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1e8a5-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="1e8a5-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1e8a5-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1e8a5-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1e8a5-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e8a5-116">Remarks</span></span>

<span data-ttu-id="1e8a5-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="1e8a5-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1e8a5-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1e8a5-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1e8a5-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1e8a5-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1e8a5-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="1e8a5-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1e8a5-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1e8a5-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e8a5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e8a5-122">Requirements</span></span>



| <span data-ttu-id="1e8a5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e8a5-123">Requirement</span></span> | <span data-ttu-id="1e8a5-124">Value</span><span class="sxs-lookup"><span data-stu-id="1e8a5-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e8a5-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e8a5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1e8a5-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1e8a5-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1e8a5-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e8a5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1e8a5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e8a5-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1e8a5-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1e8a5-129">Namespace</span></span><br/>                | <span data-ttu-id="1e8a5-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1e8a5-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1e8a5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1e8a5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e8a5-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e8a5-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e8a5-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e8a5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e8a5-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e8a5-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1e8a5-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e8a5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e8a5-136">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="1e8a5-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="1e8a5-137">**Bajar**</span><span class="sxs-lookup"><span data-stu-id="1e8a5-137">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

