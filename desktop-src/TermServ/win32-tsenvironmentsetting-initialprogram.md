---
title: Método InitialProgram de la clase Win32_TSEnvironmentSetting
description: El método InitialProgram establece las propiedades del programa de inicio, como el nombre, el directorio de trabajo y la ruta de acceso del programa que se va a iniciar inmediatamente después del inicio de sesión en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- Método InitialProgram Servicios de Escritorio remoto
- Método InitialProgram Servicios de Escritorio remoto, clase Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting de clase Servicios de Escritorio remoto, método InitialProgram
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685962"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="52d2a-106">Método InitialProgram de la \_ clase TSEnvironmentSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="52d2a-106">InitialProgram method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="52d2a-107">El método **InitialProgram** establece las propiedades del programa de inicio, como el nombre, el directorio de trabajo y la ruta de acceso del programa que se va a iniciar inmediatamente después del inicio de sesión en el servidor de host de sesión de escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="52d2a-107">The **InitialProgram** method sets startup program properties such as the name, working directory, and path of the program to start immediately after logon to the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d2a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52d2a-108">Syntax</span></span>


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a><span data-ttu-id="52d2a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52d2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52d2a-110">*InitialProgramPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52d2a-110">*InitialProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d2a-111">El nombre y la ruta de acceso del programa de inicio.</span><span class="sxs-lookup"><span data-stu-id="52d2a-111">The name and path of the startup program.</span></span>

</dd> <dt>

<span data-ttu-id="52d2a-112">*Inicio* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52d2a-112">*Startin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d2a-113">La ruta de acceso al directorio de trabajo del programa de inicio.</span><span class="sxs-lookup"><span data-stu-id="52d2a-113">The path to the working directory of the startup program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52d2a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52d2a-114">Return value</span></span>

<span data-ttu-id="52d2a-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="52d2a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="52d2a-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="52d2a-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="52d2a-117">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="52d2a-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="52d2a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52d2a-118">Remarks</span></span>

<span data-ttu-id="52d2a-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="52d2a-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="52d2a-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="52d2a-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="52d2a-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="52d2a-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="52d2a-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="52d2a-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="52d2a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52d2a-123">Requirements</span></span>



| <span data-ttu-id="52d2a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="52d2a-124">Requirement</span></span> | <span data-ttu-id="52d2a-125">Value</span><span class="sxs-lookup"><span data-stu-id="52d2a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52d2a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52d2a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52d2a-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52d2a-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52d2a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52d2a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52d2a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52d2a-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52d2a-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="52d2a-130">Namespace</span></span><br/>                | <span data-ttu-id="52d2a-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="52d2a-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="52d2a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="52d2a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52d2a-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52d2a-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="52d2a-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52d2a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52d2a-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52d2a-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d2a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="52d2a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d2a-137">**Win32 \_ TSEnvironmentSetting**</span><span class="sxs-lookup"><span data-stu-id="52d2a-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

