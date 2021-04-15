---
title: Método SetMaxMonitors de la clase Win32_TSClientSetting
description: Establece la propiedad MaxMonitors.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Método SetMaxMonitors Servicios de Escritorio remoto
- Método SetMaxMonitors Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método SetMaxMonitors
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676806"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="f7987-106">Método SetMaxMonitors de la \_ clase TSClientSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="f7987-106">SetMaxMonitors method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="f7987-107">Establece la propiedad **MaxMonitors** .</span><span class="sxs-lookup"><span data-stu-id="f7987-107">Sets the **MaxMonitors** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7987-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7987-108">Syntax</span></span>


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="f7987-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7987-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7987-110">*MaxMonitors* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f7987-110">*MaxMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7987-111">Especifica el nuevo número máximo de monitores admitidos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="f7987-111">Specifies the new maximum number of monitors supported by the server.</span></span> <span data-ttu-id="f7987-112">El valor mínimo es 1 y el valor máximo es 10.</span><span class="sxs-lookup"><span data-stu-id="f7987-112">The minimum value is 1 and the maximum value is 10.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7987-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7987-113">Return value</span></span>

<span data-ttu-id="f7987-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="f7987-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f7987-115">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f7987-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="f7987-116">El método devuelve un error si el servidor invalida la configuración de conexión del usuario.</span><span class="sxs-lookup"><span data-stu-id="f7987-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7987-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7987-117">Requirements</span></span>



| <span data-ttu-id="f7987-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7987-118">Requirement</span></span> | <span data-ttu-id="f7987-119">Value</span><span class="sxs-lookup"><span data-stu-id="f7987-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7987-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7987-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f7987-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f7987-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f7987-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7987-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f7987-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7987-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f7987-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f7987-124">Namespace</span></span><br/>                | <span data-ttu-id="f7987-125">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f7987-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f7987-126">MOF</span><span class="sxs-lookup"><span data-stu-id="f7987-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7987-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7987-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7987-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f7987-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7987-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7987-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7987-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7987-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7987-131">**Win32 \_ TSClientSetting**</span><span class="sxs-lookup"><span data-stu-id="f7987-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





