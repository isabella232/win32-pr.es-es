---
title: Método AddProgram de la clase Win32_TSVirtualIP (Bdaiface. h)
description: Agrega un programa a la lista de programas que utilizan la virtualización de IP.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- Método AddProgram Servicios de Escritorio remoto
- Método AddProgram Servicios de Escritorio remoto, clase Win32_TSVirtualIP
- Win32_TSVirtualIP de clase Servicios de Escritorio remoto, método AddProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de573e8d04500917ed44d5a0453005b3aa691bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801724"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="68769-106">Método AddProgram de la \_ clase TSVirtualIP de Win32</span><span class="sxs-lookup"><span data-stu-id="68769-106">AddProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="68769-107">Agrega un programa a la lista de programas que utilizan la virtualización de IP.</span><span class="sxs-lookup"><span data-stu-id="68769-107">Adds a program to the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="68769-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68769-108">Syntax</span></span>


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="68769-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68769-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68769-110">*ProgramPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68769-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68769-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="68769-111">Type: **string**</span></span>

<span data-ttu-id="68769-112">Ruta de acceso y nombre de archivo del programa que se va a agregar a la lista.</span><span class="sxs-lookup"><span data-stu-id="68769-112">The path and file name of the program to add to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68769-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68769-113">Return value</span></span>

<span data-ttu-id="68769-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68769-114">Type: **uint32**</span></span>

<span data-ttu-id="68769-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="68769-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="68769-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="68769-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="68769-117">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="68769-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="68769-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68769-118">Requirements</span></span>



| <span data-ttu-id="68769-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="68769-119">Requirement</span></span> | <span data-ttu-id="68769-120">Value</span><span class="sxs-lookup"><span data-stu-id="68769-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68769-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68769-121">Minimum supported client</span></span><br/> | <span data-ttu-id="68769-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="68769-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="68769-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68769-123">Minimum supported server</span></span><br/> | <span data-ttu-id="68769-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="68769-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="68769-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68769-125">Namespace</span></span><br/>                | <span data-ttu-id="68769-126">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="68769-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="68769-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68769-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="68769-128"><dt>Bdaiface. h</dt></span><span class="sxs-lookup"><span data-stu-id="68769-128"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="68769-129">MOF</span><span class="sxs-lookup"><span data-stu-id="68769-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68769-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68769-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="68769-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68769-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68769-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68769-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68769-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="68769-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68769-134">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="68769-134">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





