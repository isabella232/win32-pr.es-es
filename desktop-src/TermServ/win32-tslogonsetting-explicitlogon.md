---
title: Método ExplicitLogon de la clase Win32_TSLogonSetting
description: El método ExplicitLogon establece las credenciales que se usarán para la autenticación.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Método ExplicitLogon Servicios de Escritorio remoto
- Método ExplicitLogon Servicios de Escritorio remoto, clase Win32_TSLogonSetting
- Win32_TSLogonSetting de clase Servicios de Escritorio remoto, método ExplicitLogon
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422463"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="051cb-106">Método ExplicitLogon de la \_ clase TSLogonSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="051cb-106">ExplicitLogon method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="051cb-107">El método **ExplicitLogon** establece las credenciales que se usarán para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="051cb-107">The **ExplicitLogon** method sets the credentials to use for authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="051cb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="051cb-108">Syntax</span></span>


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a><span data-ttu-id="051cb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="051cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="051cb-110">*Nombre de usuario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="051cb-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="051cb-111">La credencial de inicio de sesión del nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="051cb-111">The user name logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="051cb-112">*Dominio* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="051cb-112">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="051cb-113">Credencial de inicio de sesión de dominio.</span><span class="sxs-lookup"><span data-stu-id="051cb-113">The domain logon credential.</span></span>

</dd> <dt>

<span data-ttu-id="051cb-114">*Contraseña* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="051cb-114">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="051cb-115">La credencial de inicio de sesión de contraseña.</span><span class="sxs-lookup"><span data-stu-id="051cb-115">The password logon credential.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="051cb-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="051cb-116">Return value</span></span>

<span data-ttu-id="051cb-117">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="051cb-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="051cb-118">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="051cb-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="051cb-119">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="051cb-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="051cb-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="051cb-120">Remarks</span></span>

<span data-ttu-id="051cb-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="051cb-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="051cb-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="051cb-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="051cb-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="051cb-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="051cb-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="051cb-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="051cb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="051cb-125">Requirements</span></span>



| <span data-ttu-id="051cb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="051cb-126">Requirement</span></span> | <span data-ttu-id="051cb-127">Value</span><span class="sxs-lookup"><span data-stu-id="051cb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="051cb-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="051cb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="051cb-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="051cb-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="051cb-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="051cb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="051cb-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="051cb-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="051cb-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="051cb-132">Namespace</span></span><br/>                | <span data-ttu-id="051cb-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="051cb-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="051cb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="051cb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="051cb-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="051cb-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="051cb-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="051cb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="051cb-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="051cb-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="051cb-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="051cb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="051cb-139">**Win32 \_ TSLogonSetting**</span><span class="sxs-lookup"><span data-stu-id="051cb-139">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

