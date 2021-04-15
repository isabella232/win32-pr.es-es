---
title: Método EnableRequestSOH de la clase Win32_TSGatewayServerSettings
description: EnableRequestSOH ya no está disponible.
ms.assetid: 4feb7530-cced-4ead-a1fb-679b81442bb3
ms.tgt_platform: multiple
keywords:
- Método EnableRequestSOH Servicios de Escritorio remoto
- Método EnableRequestSOH Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método EnableRequestSOH
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableRequestSOH
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90ed6a3929b50d13a27ec559aab534f9e06f738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676914"
---
# <a name="enablerequestsoh-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="bce71-106">Método EnableRequestSOH de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="bce71-106">EnableRequestSOH method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="bce71-107">\[El método **EnableRequestSOH** ya no está disponible a partir de Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="bce71-107">\[The **EnableRequestSOH** method is no longer available as of Windows Server 2016.\]</span></span>

<span data-ttu-id="bce71-108">Habilita o deshabilita las solicitudes de un informe de mantenimiento (SoH).</span><span class="sxs-lookup"><span data-stu-id="bce71-108">Enables or disables requests for a Statement of Health (SoH).</span></span>

## <a name="syntax"></a><span data-ttu-id="bce71-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bce71-109">Syntax</span></span>


```mof
uint32 EnableRequestSOH(
  [in] boolean RequestSOH
);
```



## <a name="parameters"></a><span data-ttu-id="bce71-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bce71-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce71-111">*RequestSOH* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bce71-111">*RequestSOH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bce71-112">Especifique **true** para habilitar la característica o **false** para deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="bce71-112">Specify **TRUE** to enable the feature or **FALSE** to disable the feature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce71-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bce71-113">Return value</span></span>

<span data-ttu-id="bce71-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="bce71-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bce71-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bce71-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bce71-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bce71-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bce71-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bce71-117">Remarks</span></span>

<span data-ttu-id="bce71-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="bce71-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bce71-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bce71-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bce71-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bce71-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bce71-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="bce71-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bce71-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bce71-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bce71-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bce71-123">Requirements</span></span>



| <span data-ttu-id="bce71-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bce71-124">Requirement</span></span> | <span data-ttu-id="bce71-125">Value</span><span class="sxs-lookup"><span data-stu-id="bce71-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bce71-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bce71-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bce71-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bce71-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bce71-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bce71-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bce71-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bce71-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bce71-130">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bce71-130">End of server support</span></span><br/>    | <span data-ttu-id="bce71-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bce71-131">Windows Server 2012 R2</span></span><br/>                                                        |
| <span data-ttu-id="bce71-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bce71-132">Namespace</span></span><br/>                | <span data-ttu-id="bce71-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bce71-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bce71-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bce71-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bce71-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bce71-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bce71-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bce71-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bce71-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bce71-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bce71-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="bce71-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce71-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="bce71-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

