---
title: Método SetPortNumbers de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Establece los números de puerto que pueden conectarse al recurso a través de Escritorio remoto puerta de enlace de escritorio remoto.
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- Método SetPortNumbers Servicios de Escritorio remoto
- Método SetPortNumbers Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetPortNumbers
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b938435abab23e3ad27cf13dbe65e64b9ec859eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491614"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="6a28f-106">Método SetPortNumbers de la \_ clase TSGatewayResourceAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="6a28f-106">SetPortNumbers method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="6a28f-107">Establece los números de puerto que pueden conectarse al recurso a través de Escritorio remoto puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6a28f-107">Sets the port numbers that are allowed to connect to the resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a28f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a28f-108">Syntax</span></span>


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="6a28f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a28f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a28f-110">*PortNumbers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6a28f-110">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a28f-111">Lista de números de Puerto separados por punto y coma que se permiten para esta Escritorio remoto Directiva de autorización de recursos (RAP de RD).</span><span class="sxs-lookup"><span data-stu-id="6a28f-111">List of semicolon-separated port numbers that are allowed for this Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="6a28f-112">Para permitir cualquier número de puerto, establezca " \* ".</span><span class="sxs-lookup"><span data-stu-id="6a28f-112">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a28f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a28f-113">Remarks</span></span>

<span data-ttu-id="6a28f-114">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6a28f-114">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6a28f-115">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6a28f-115">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6a28f-116">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="6a28f-116">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6a28f-117">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6a28f-117">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a28f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a28f-118">Requirements</span></span>



| <span data-ttu-id="6a28f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a28f-119">Requirement</span></span> | <span data-ttu-id="6a28f-120">Value</span><span class="sxs-lookup"><span data-stu-id="6a28f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a28f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a28f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6a28f-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6a28f-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6a28f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a28f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6a28f-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a28f-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6a28f-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6a28f-125">Namespace</span></span><br/>                | <span data-ttu-id="6a28f-126">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6a28f-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6a28f-127">MOF</span><span class="sxs-lookup"><span data-stu-id="6a28f-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a28f-128"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a28f-128"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a28f-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a28f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a28f-130"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a28f-130"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6a28f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a28f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a28f-132">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="6a28f-132">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

