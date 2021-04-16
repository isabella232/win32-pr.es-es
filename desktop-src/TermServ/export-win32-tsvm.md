---
title: Método Export de la clase Win32_TSVm
description: Recupera la información de supervisión de sesión de máquina virtual.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Método de exportación Servicios de Escritorio remoto
- Método de exportación Servicios de Escritorio remoto, Win32_TSVm clase)
- Win32_TSVm de clase Servicios de Escritorio remoto, método Export
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676643"
---
# <a name="export-method-of-the-win32_tsvm-class"></a><span data-ttu-id="15f7a-106">Método Export de la \_ clase Win32 TSVm</span><span class="sxs-lookup"><span data-stu-id="15f7a-106">Export method of the Win32\_TSVm class</span></span>

<span data-ttu-id="15f7a-107">Recupera la información de supervisión de sesión de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="15f7a-107">Retrieves the virtual machine session monitoring information.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f7a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15f7a-108">Syntax</span></span>


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a><span data-ttu-id="15f7a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15f7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15f7a-110">*ExportFolderPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="15f7a-110">*ExportFolderPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15f7a-111">Ruta de acceso al lugar donde se exportará la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="15f7a-111">Path to where the virtual machine will be exported.</span></span>

</dd> <dt>

<span data-ttu-id="15f7a-112">*ExportJobObjectPath* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="15f7a-112">*ExportJobObjectPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15f7a-113">Si se ejecuta correctamente, devuelve la ruta de acceso del objeto ConcreteJob de HyperV.</span><span class="sxs-lookup"><span data-stu-id="15f7a-113">On a success returns the HyperV ConcreteJob object path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15f7a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15f7a-114">Return value</span></span>

<span data-ttu-id="15f7a-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="15f7a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="15f7a-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="15f7a-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="15f7a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15f7a-117">Requirements</span></span>



| <span data-ttu-id="15f7a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="15f7a-118">Requirement</span></span> | <span data-ttu-id="15f7a-119">Value</span><span class="sxs-lookup"><span data-stu-id="15f7a-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="15f7a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15f7a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="15f7a-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="15f7a-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="15f7a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15f7a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="15f7a-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15f7a-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="15f7a-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15f7a-124">Namespace</span></span><br/>                | <span data-ttu-id="15f7a-125">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="15f7a-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="15f7a-126">MOF</span><span class="sxs-lookup"><span data-stu-id="15f7a-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15f7a-127"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15f7a-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="15f7a-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15f7a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15f7a-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15f7a-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15f7a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="15f7a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f7a-131">**Win32 \_ TSVm**</span><span class="sxs-lookup"><span data-stu-id="15f7a-131">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





