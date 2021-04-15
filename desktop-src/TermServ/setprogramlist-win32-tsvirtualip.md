---
title: Método SetProgramList de la clase Win32_TSVirtualIP
description: Sobrescribe la lista de programas que utilizan la virtualización de IP.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- Método SetProgramList Servicios de Escritorio remoto
- Método SetProgramList Servicios de Escritorio remoto, clase Win32_TSVirtualIP
- Win32_TSVirtualIP de clase Servicios de Escritorio remoto, método SetProgramList
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f86c5d530b3393ac1be8858a7ce57ee70ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534408"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="b9754-106">Método SetProgramList de la \_ clase TSVirtualIP de Win32</span><span class="sxs-lookup"><span data-stu-id="b9754-106">SetProgramList method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="b9754-107">Sobrescribe la lista de programas que utilizan la virtualización de IP.</span><span class="sxs-lookup"><span data-stu-id="b9754-107">Overwrites the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9754-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9754-108">Syntax</span></span>


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a><span data-ttu-id="b9754-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9754-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9754-110">*ProgramList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9754-110">*ProgramList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9754-111">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b9754-111">Type: **string\[\]**</span></span>

<span data-ttu-id="b9754-112">Matriz de cadenas que contiene la ruta de acceso y los nombres de archivo de los programas que utilizan la virtualización de IP.</span><span class="sxs-lookup"><span data-stu-id="b9754-112">An array of strings that contain the path and file names of the programs that use IP virtualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9754-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9754-113">Return value</span></span>

<span data-ttu-id="b9754-114">Tipo: **unint32**</span><span class="sxs-lookup"><span data-stu-id="b9754-114">Type: **unint32**</span></span>

<span data-ttu-id="b9754-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="b9754-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b9754-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b9754-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="b9754-117">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="b9754-117">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9754-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9754-118">Requirements</span></span>



| <span data-ttu-id="b9754-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9754-119">Requirement</span></span> | <span data-ttu-id="b9754-120">Value</span><span class="sxs-lookup"><span data-stu-id="b9754-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9754-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9754-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b9754-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b9754-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b9754-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9754-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b9754-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9754-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b9754-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9754-125">Namespace</span></span><br/>                | <span data-ttu-id="b9754-126">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b9754-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b9754-127">MOF</span><span class="sxs-lookup"><span data-stu-id="b9754-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9754-128"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9754-128"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9754-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9754-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9754-130"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9754-130"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9754-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9754-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9754-132">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="b9754-132">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





