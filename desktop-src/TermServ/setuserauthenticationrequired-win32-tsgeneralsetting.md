---
title: Método SetUserAuthenticationRequired de la clase Win32_TSGeneralSetting
description: Habilita o deshabilita el requisito de que los usuarios se deben autenticar en el momento de la conexión estableciendo el valor de la propiedad UserAuthenticationRequired.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- Método SetUserAuthenticationRequired Servicios de Escritorio remoto
- Método SetUserAuthenticationRequired Servicios de Escritorio remoto, clase Win32_TSGeneralSetting
- Win32_TSGeneralSetting de clase Servicios de Escritorio remoto, método SetUserAuthenticationRequired
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359824"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="347b4-106">Método SetUserAuthenticationRequired de la \_ clase TSGeneralSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="347b4-106">SetUserAuthenticationRequired method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="347b4-107">Habilita o deshabilita el requisito de que los usuarios se deben autenticar en el momento de la conexión estableciendo el valor de la propiedad **UserAuthenticationRequired** en la clase [**\_ TSGeneralSetting de Win32**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="347b4-107">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property in the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span> <span data-ttu-id="347b4-108">Si **es true**, lo que significa habilitado, **UserAuthenticationRequired** requiere autenticación de usuario en el momento de la conexión para aumentar la protección del servidor frente a ataques de red.</span><span class="sxs-lookup"><span data-stu-id="347b4-108">If **True**, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="347b4-109">Solo los clientes Protocolo de escritorio remoto (RDP) que admiten la versión 6,0 o posterior de RDP pueden conectarse.</span><span class="sxs-lookup"><span data-stu-id="347b4-109">Only Remote Desktop Protocol (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="347b4-110">Para evitar interrupciones para los usuarios remotos, se recomienda que implemente los clientes RDP que admitan la versión de protocolo adecuada antes de habilitar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="347b4-110">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

## <a name="syntax"></a><span data-ttu-id="347b4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="347b4-111">Syntax</span></span>


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a><span data-ttu-id="347b4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="347b4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="347b4-113">*UserAuthenticationRequired* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="347b4-113">*UserAuthenticationRequired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="347b4-114">Indica si se requiere la autenticación del usuario.</span><span class="sxs-lookup"><span data-stu-id="347b4-114">Indicates whether user authentication is required.</span></span>

<dt>

<span data-ttu-id="347b4-115">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="347b4-115">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="347b4-116">Deshabilitar requisito de que el usuario debe estar autenticado</span><span class="sxs-lookup"><span data-stu-id="347b4-116">Disable requirement that user must be authenticated</span></span>

</dd> <dt>

<span data-ttu-id="347b4-117">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="347b4-117">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="347b4-118">Habilita el requisito de que el usuario debe estar autenticado.</span><span class="sxs-lookup"><span data-stu-id="347b4-118">Enables requirement that user must be authenticated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="347b4-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="347b4-119">Return value</span></span>

<span data-ttu-id="347b4-120">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="347b4-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="347b4-121">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="347b4-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="347b4-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="347b4-122">Remarks</span></span>

<span data-ttu-id="347b4-123">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="347b4-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="347b4-124">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="347b4-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="347b4-125">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="347b4-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="347b4-126">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="347b4-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="347b4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="347b4-127">Requirements</span></span>



| <span data-ttu-id="347b4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="347b4-128">Requirement</span></span> | <span data-ttu-id="347b4-129">Value</span><span class="sxs-lookup"><span data-stu-id="347b4-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="347b4-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="347b4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="347b4-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="347b4-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="347b4-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="347b4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="347b4-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="347b4-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="347b4-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="347b4-134">Namespace</span></span><br/>                | <span data-ttu-id="347b4-135">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="347b4-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="347b4-136">MOF</span><span class="sxs-lookup"><span data-stu-id="347b4-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="347b4-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="347b4-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="347b4-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="347b4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="347b4-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="347b4-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="347b4-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="347b4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="347b4-141">**Win32 \_ TSGeneralSetting**</span><span class="sxs-lookup"><span data-stu-id="347b4-141">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

