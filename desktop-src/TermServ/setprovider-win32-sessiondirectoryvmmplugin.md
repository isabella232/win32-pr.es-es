---
title: Método SetProvider de la clase Win32_SessionDirectoryVMMPlugin
description: Establece el nombre del proveedor del complemento.
ms.assetid: fefb7c19-2bab-4ae3-b88b-20da5fd19ff3
ms.tgt_platform: multiple
keywords:
- Método SetProvider Servicios de Escritorio remoto
- Método SetProvider Servicios de Escritorio remoto, clase Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de clase Servicios de Escritorio remoto, método SetProvider
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetProvider
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205a88ecbd67dcf3b009577fa7384e074cc68487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802258"
---
# <a name="setprovider-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="fe594-106">Método SetProvider de la \_ clase SessionDirectoryVMMPlugin de Win32</span><span class="sxs-lookup"><span data-stu-id="fe594-106">SetProvider method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="fe594-107">Establece el nombre del proveedor del complemento.</span><span class="sxs-lookup"><span data-stu-id="fe594-107">Sets the name of the plug-in provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe594-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe594-108">Syntax</span></span>


```mof
uint32 SetProvider(
  [in] string sProvider
);
```



## <a name="parameters"></a><span data-ttu-id="fe594-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe594-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe594-110">*sProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe594-110">*sProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe594-111">Nombre del proveedor del complemento.</span><span class="sxs-lookup"><span data-stu-id="fe594-111">The name of the plug-in provider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe594-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe594-112">Return value</span></span>

<span data-ttu-id="fe594-113">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="fe594-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fe594-114">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="fe594-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe594-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe594-115">Requirements</span></span>



| <span data-ttu-id="fe594-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe594-116">Requirement</span></span> | <span data-ttu-id="fe594-117">Value</span><span class="sxs-lookup"><span data-stu-id="fe594-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe594-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe594-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fe594-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fe594-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fe594-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe594-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fe594-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fe594-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="fe594-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fe594-122">Namespace</span></span><br/>                | <span data-ttu-id="fe594-123">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fe594-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="fe594-124">MOF</span><span class="sxs-lookup"><span data-stu-id="fe594-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe594-125"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe594-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe594-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fe594-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe594-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe594-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe594-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe594-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe594-129">**Win32 \_ SessionDirectoryVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="fe594-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





