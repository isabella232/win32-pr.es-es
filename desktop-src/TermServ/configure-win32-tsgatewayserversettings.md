---
title: Método configure de la clase Win32_TSGatewayServerSettings
description: Configura los valores de IIS y RPC requeridos por el servicio de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 12d7264e-46aa-457f-b89d-547231573db8
ms.tgt_platform: multiple
keywords:
- Configurar método Servicios de Escritorio remoto
- Configurar método Servicios de Escritorio remoto, Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, configure (método)
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.Configure
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1880e1a9811c8aab2660993c6c8ab05061163e1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079039"
---
# <a name="configure-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="0870d-106">Método configure de la \_ clase Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="0870d-106">Configure method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="0870d-107">Configura los valores de IIS y RPC requeridos por el servicio de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="0870d-107">Configures the IIS and RPC settings required by the Remote Desktop Gateway (RD Gateway) service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0870d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0870d-108">Syntax</span></span>


```mof
uint32 Configure();
```



## <a name="parameters"></a><span data-ttu-id="0870d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0870d-109">Parameters</span></span>

<span data-ttu-id="0870d-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0870d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0870d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0870d-111">Return value</span></span>

<span data-ttu-id="0870d-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0870d-112">Type: **uint32**</span></span>

<span data-ttu-id="0870d-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="0870d-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0870d-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="0870d-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0870d-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0870d-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0870d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0870d-116">Remarks</span></span>

<span data-ttu-id="0870d-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="0870d-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0870d-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0870d-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0870d-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0870d-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0870d-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="0870d-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0870d-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0870d-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0870d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0870d-122">Requirements</span></span>



| <span data-ttu-id="0870d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0870d-123">Requirement</span></span> | <span data-ttu-id="0870d-124">Value</span><span class="sxs-lookup"><span data-stu-id="0870d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0870d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0870d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0870d-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0870d-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0870d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0870d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0870d-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0870d-128">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="0870d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0870d-129">Namespace</span></span><br/>                | <span data-ttu-id="0870d-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0870d-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0870d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0870d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0870d-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0870d-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0870d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0870d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0870d-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0870d-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0870d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0870d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0870d-136">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="0870d-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

