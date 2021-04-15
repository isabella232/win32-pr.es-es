---
title: Método Delete de la clase Win32_Terminal
description: Elimina el terminal especificado.
ms.assetid: 59d8cc73-aef1-49d2-a7a2-dd3cbe5a8c52
ms.tgt_platform: multiple
keywords:
- Eliminar método Servicios de Escritorio remoto
- Método Delete Servicios de Escritorio remoto, clase Win32_Terminal
- Clase Win32_Terminal Servicios de Escritorio remoto, método Delete
topic_type:
- apiref
api_name:
- Win32_Terminal.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b7120c78eada2b047f836219d3382e5ce1e2f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676609"
---
# <a name="delete-method-of-the-win32_terminal-class"></a><span data-ttu-id="1f332-106">Método Delete de la \_ clase de terminal Win32</span><span class="sxs-lookup"><span data-stu-id="1f332-106">Delete method of the Win32\_Terminal class</span></span>

<span data-ttu-id="1f332-107">El método **Delete** elimina el terminal especificado.</span><span class="sxs-lookup"><span data-stu-id="1f332-107">The **Delete** method deletes the specified terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f332-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f332-108">Syntax</span></span>


```mof
uint32 Delete(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a><span data-ttu-id="1f332-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f332-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f332-110">*NewTerminalName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f332-110">*NewTerminalName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f332-111">Nombre del terminal que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="1f332-111">Name of the terminal to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f332-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f332-112">Return value</span></span>

<span data-ttu-id="1f332-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="1f332-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1f332-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="1f332-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f332-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f332-115">Remarks</span></span>

<span data-ttu-id="1f332-116">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1f332-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1f332-117">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1f332-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1f332-118">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="1f332-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1f332-119">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1f332-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f332-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f332-120">Requirements</span></span>



| <span data-ttu-id="1f332-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f332-121">Requirement</span></span> | <span data-ttu-id="1f332-122">Value</span><span class="sxs-lookup"><span data-stu-id="1f332-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f332-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f332-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1f332-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f332-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f332-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f332-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1f332-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f332-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f332-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1f332-127">Namespace</span></span><br/>                | <span data-ttu-id="1f332-128">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1f332-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1f332-129">MOF</span><span class="sxs-lookup"><span data-stu-id="1f332-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f332-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f332-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f332-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f332-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f332-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f332-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f332-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f332-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f332-134">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="1f332-134">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

