---
title: Método SetDescription de la clase Win32_TSGatewayResourceGroup
description: Establece la propiedad Description del grupo de recursos.
ms.assetid: ab1280c7-ce53-4807-9537-953b597dd636
ms.tgt_platform: multiple
keywords:
- Método SetDescription Servicios de Escritorio remoto
- Método SetDescription Servicios de Escritorio remoto, clase Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup de clase Servicios de Escritorio remoto, método SetDescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d815cc5400a182f2dff3b982643d5e6bfd861002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676965"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourcegroup-class"></a><span data-ttu-id="5688b-106">Método SetDescription de la \_ clase TSGatewayResourceGroup de Win32</span><span class="sxs-lookup"><span data-stu-id="5688b-106">SetDescription method of the Win32\_TSGatewayResourceGroup class</span></span>

<span data-ttu-id="5688b-107">Establece la propiedad **Description** del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5688b-107">Sets the **Description** property for the resource group.</span></span>

## <a name="syntax"></a><span data-ttu-id="5688b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5688b-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="5688b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5688b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5688b-110">*Descripción* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5688b-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5688b-111">Descripción del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5688b-111">Description of the resource group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5688b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5688b-112">Return value</span></span>

<span data-ttu-id="5688b-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5688b-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5688b-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="5688b-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5688b-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5688b-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5688b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5688b-116">Remarks</span></span>

<span data-ttu-id="5688b-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="5688b-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5688b-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5688b-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5688b-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5688b-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5688b-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5688b-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5688b-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5688b-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5688b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5688b-122">Requirements</span></span>



| <span data-ttu-id="5688b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5688b-123">Requirement</span></span> | <span data-ttu-id="5688b-124">Value</span><span class="sxs-lookup"><span data-stu-id="5688b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5688b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5688b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5688b-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5688b-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5688b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5688b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5688b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5688b-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5688b-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5688b-129">Namespace</span></span><br/>                | <span data-ttu-id="5688b-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5688b-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5688b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5688b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5688b-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5688b-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5688b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5688b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5688b-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5688b-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5688b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5688b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5688b-136">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="5688b-136">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

