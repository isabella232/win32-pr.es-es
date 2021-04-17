---
title: Método SetName de la clase Win32_SessionDirectoryVMMPlugin
description: Establece el nombre del complemento.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- SetName (método) Servicios de Escritorio remoto
- Método SetName Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Clase Win32_SessionDirectoryVMMPlugin Servicios de Escritorio remoto, método SetName
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9902e8d5931f0800dc6c62d36815f4f78db73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359731"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="4f0ee-106">Método SetName de la \_ clase SessionDirectoryVMMPlugin de Win32</span><span class="sxs-lookup"><span data-stu-id="4f0ee-106">SetName method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="4f0ee-107">Establece el nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-107">Sets the name of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f0ee-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f0ee-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a><span data-ttu-id="4f0ee-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f0ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f0ee-110">*sName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f0ee-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f0ee-111">Nombre del complemento.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-111">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f0ee-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f0ee-112">Return value</span></span>

<span data-ttu-id="4f0ee-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4f0ee-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="4f0ee-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f0ee-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f0ee-115">Requirements</span></span>



| <span data-ttu-id="4f0ee-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f0ee-116">Requirement</span></span> | <span data-ttu-id="4f0ee-117">Value</span><span class="sxs-lookup"><span data-stu-id="4f0ee-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f0ee-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f0ee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4f0ee-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4f0ee-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4f0ee-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f0ee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4f0ee-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f0ee-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="4f0ee-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f0ee-122">Namespace</span></span><br/>                | <span data-ttu-id="4f0ee-123">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4f0ee-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="4f0ee-124">MOF</span><span class="sxs-lookup"><span data-stu-id="4f0ee-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f0ee-125"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f0ee-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f0ee-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f0ee-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f0ee-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f0ee-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f0ee-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f0ee-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f0ee-129">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="4f0ee-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





