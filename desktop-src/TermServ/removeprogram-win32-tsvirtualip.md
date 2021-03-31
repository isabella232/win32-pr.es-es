---
title: Método RemoveProgram de la clase Win32_TSVirtualIP (Bdaiface. h)
description: Quita un programa de la lista de programas que utilizan la virtualización de IP.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- Método RemoveProgram Servicios de Escritorio remoto
- Método RemoveProgram Servicios de Escritorio remoto, clase Win32_TSVirtualIP
- Win32_TSVirtualIP de clase Servicios de Escritorio remoto, método RemoveProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6241664b6e56c3d387673b6a1cc50e43b413336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803871"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="524a1-106">Método RemoveProgram de la \_ clase TSVirtualIP de Win32</span><span class="sxs-lookup"><span data-stu-id="524a1-106">RemoveProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="524a1-107">Quita un programa de la lista de programas que utilizan la virtualización de IP.</span><span class="sxs-lookup"><span data-stu-id="524a1-107">Removes a program from the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="524a1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="524a1-108">Syntax</span></span>


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="524a1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="524a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="524a1-110">*ProgramPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="524a1-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="524a1-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="524a1-111">Type: **string**</span></span>

<span data-ttu-id="524a1-112">Ruta de acceso y nombre de archivo del programa que se va a quitar de la lista.</span><span class="sxs-lookup"><span data-stu-id="524a1-112">The path and file name of the program to remove from the list.</span></span> <span data-ttu-id="524a1-113">Si no se encuentra el programa, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="524a1-113">If the program is not found, an error is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="524a1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="524a1-114">Return value</span></span>

<span data-ttu-id="524a1-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="524a1-115">Type: **uint32**</span></span>

<span data-ttu-id="524a1-116">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="524a1-116">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="524a1-117">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="524a1-117">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="524a1-118">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="524a1-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="524a1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="524a1-119">Requirements</span></span>



| <span data-ttu-id="524a1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="524a1-120">Requirement</span></span> | <span data-ttu-id="524a1-121">Value</span><span class="sxs-lookup"><span data-stu-id="524a1-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="524a1-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="524a1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="524a1-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="524a1-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="524a1-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="524a1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="524a1-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="524a1-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="524a1-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="524a1-126">Namespace</span></span><br/>                | <span data-ttu-id="524a1-127">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="524a1-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="524a1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="524a1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="524a1-129"><dt>Bdaiface. h</dt></span><span class="sxs-lookup"><span data-stu-id="524a1-129"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="524a1-130">MOF</span><span class="sxs-lookup"><span data-stu-id="524a1-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="524a1-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="524a1-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="524a1-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="524a1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="524a1-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="524a1-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="524a1-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="524a1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="524a1-135">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="524a1-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





