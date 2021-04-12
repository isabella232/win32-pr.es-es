---
title: Método Create de la clase Win32_Terminal
description: Crea un terminal con valores predeterminados que se pueden personalizar mediante las propiedades y los métodos de las \_ clases TerminalSetting de Win32.
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create Method Servicios de Escritorio remoto, Win32_Terminal (clase)
- Win32_Terminal Servicios de Escritorio remoto de clase, Create (método)
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489533"
---
# <a name="create-method-of-the-win32_terminal-class"></a><span data-ttu-id="7a33e-106">Método Create de la \_ clase de terminal Win32</span><span class="sxs-lookup"><span data-stu-id="7a33e-106">Create method of the Win32\_Terminal class</span></span>

<span data-ttu-id="7a33e-107">El método **Create** crea un terminal con valores predeterminados que se pueden personalizar mediante las propiedades y los métodos de las clases [**\_ TerminalSetting de Win32**](win32-terminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="7a33e-107">The **Create** method creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span> <span data-ttu-id="7a33e-108">La función devuelve cero si se ejecuta correctamente y un error en el error.</span><span class="sxs-lookup"><span data-stu-id="7a33e-108">The function returns zero on success and an error on failure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a33e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a33e-109">Syntax</span></span>


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="7a33e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a33e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a33e-111">*NewTerminalName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7a33e-111">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a33e-112">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="7a33e-112">Name of the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="7a33e-113">*Transporte* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7a33e-113">*Transport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a33e-114">Transporte para el terminal.</span><span class="sxs-lookup"><span data-stu-id="7a33e-114">Transport for the terminal.</span></span> <span data-ttu-id="7a33e-115">Esta es una propiedad de la [**clase \_ TSGeneralSetting de Win32**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="7a33e-115">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7a33e-116">*TerminalProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7a33e-116">*TerminalProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a33e-117">Protocolo para el terminal.</span><span class="sxs-lookup"><span data-stu-id="7a33e-117">Protocol for the terminal.</span></span> <span data-ttu-id="7a33e-118">Esta es una propiedad de la [**clase \_ TSGeneralSetting de Win32**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="7a33e-118">This is a property of the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a33e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a33e-119">Return value</span></span>

<span data-ttu-id="7a33e-120">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="7a33e-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7a33e-121">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="7a33e-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a33e-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a33e-122">Remarks</span></span>

<span data-ttu-id="7a33e-123">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="7a33e-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7a33e-124">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7a33e-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7a33e-125">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="7a33e-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7a33e-126">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7a33e-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a33e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a33e-127">Requirements</span></span>



| <span data-ttu-id="7a33e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a33e-128">Requirement</span></span> | <span data-ttu-id="7a33e-129">Value</span><span class="sxs-lookup"><span data-stu-id="7a33e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a33e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a33e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7a33e-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a33e-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a33e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a33e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7a33e-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a33e-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a33e-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7a33e-134">Namespace</span></span><br/>                | <span data-ttu-id="7a33e-135">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7a33e-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7a33e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7a33e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a33e-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a33e-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a33e-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a33e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a33e-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a33e-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a33e-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a33e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a33e-141">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="7a33e-141">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

