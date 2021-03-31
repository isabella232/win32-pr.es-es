---
title: Método TimeLimit de la clase Win32_TSSessionSetting
description: Establece el tiempo máximo asignado al tipo de límite de sesión especificado.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- Método TimeLimit Servicios de Escritorio remoto
- Método TimeLimit Servicios de Escritorio remoto, clase Win32_TSSessionSetting
- Win32_TSSessionSetting de clase Servicios de Escritorio remoto, método TimeLimit
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533783"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="f72e1-106">Método TimeLimit de la \_ clase TSSessionSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="f72e1-106">TimeLimit method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="f72e1-107">Establece el tiempo máximo asignado al tipo de límite de sesión especificado.</span><span class="sxs-lookup"><span data-stu-id="f72e1-107">Sets the maximum time allocated to the specified session-limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72e1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f72e1-108">Syntax</span></span>


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a><span data-ttu-id="f72e1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f72e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f72e1-110">*SessionLimitType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f72e1-110">*SessionLimitType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f72e1-111">Especifica el tipo de propiedad de límite de sesión que el método está estableciendo.</span><span class="sxs-lookup"><span data-stu-id="f72e1-111">Specifies the type of session-limit property that the method is setting.</span></span>

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span data-ttu-id="f72e1-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="f72e1-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="f72e1-113">El método está estableciendo la propiedad **ActiveSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="f72e1-113">The method is setting the **ActiveSessionLimit** property.</span></span>

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span data-ttu-id="f72e1-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="f72e1-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="f72e1-115">El método está estableciendo la propiedad **DisconnectedSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="f72e1-115">The method is setting the **DisconnectedSessionLimit** property.</span></span>

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span data-ttu-id="f72e1-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="f72e1-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="f72e1-117">El método está estableciendo la propiedad **IdleSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="f72e1-117">The method is setting the **IdleSessionLimit** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f72e1-118">*ValueLimit* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f72e1-118">*ValueLimit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f72e1-119">Nuevo tiempo máximo, en milisegundos, para la propiedad especificada por el parámetro *SessionLimitType* .</span><span class="sxs-lookup"><span data-stu-id="f72e1-119">The new maximum time, in milliseconds, for the property specified by the *SessionLimitType* parameter.</span></span> <span data-ttu-id="f72e1-120">El valor cero indica que no hay límite de sesión.</span><span class="sxs-lookup"><span data-stu-id="f72e1-120">The value zero indicates that there is no session limit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f72e1-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f72e1-121">Return value</span></span>

<span data-ttu-id="f72e1-122">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="f72e1-122">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f72e1-123">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f72e1-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="f72e1-124">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="f72e1-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="f72e1-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f72e1-125">Remarks</span></span>

<span data-ttu-id="f72e1-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f72e1-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f72e1-127">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f72e1-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f72e1-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f72e1-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f72e1-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f72e1-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f72e1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f72e1-130">Requirements</span></span>



| <span data-ttu-id="f72e1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f72e1-131">Requirement</span></span> | <span data-ttu-id="f72e1-132">Value</span><span class="sxs-lookup"><span data-stu-id="f72e1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f72e1-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f72e1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f72e1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f72e1-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f72e1-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f72e1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f72e1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f72e1-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f72e1-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f72e1-137">Namespace</span></span><br/>                | <span data-ttu-id="f72e1-138">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f72e1-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f72e1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f72e1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f72e1-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f72e1-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f72e1-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f72e1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f72e1-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f72e1-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f72e1-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="f72e1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72e1-144">**Win32 \_ TSSessionSetting**</span><span class="sxs-lookup"><span data-stu-id="f72e1-144">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 

