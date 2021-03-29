---
title: Método SetTSRedirectorMode de la clase Win32_TSSessionDirectory
description: Establece el valor para indicar si el servidor actuará como redirector de Servicios de Escritorio remoto.
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- Método SetTSRedirectorMode Servicios de Escritorio remoto
- Método SetTSRedirectorMode Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método SetTSRedirectorMode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e3195a83a32dca0c8e4a96de211a72a66a8f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905566"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="2be5c-106">Método SetTSRedirectorMode de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="2be5c-106">SetTSRedirectorMode method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="2be5c-107">Establece el valor para indicar si el servidor actuará como redirector de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2be5c-107">Sets the value to indicate whether the server will act as a Remote Desktop Services redirector.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be5c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2be5c-108">Syntax</span></span>


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a><span data-ttu-id="2be5c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2be5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be5c-110">*TSRedirValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2be5c-110">*TSRedirValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2be5c-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2be5c-111">Type: **uint32**</span></span>

<span data-ttu-id="2be5c-112">Especifica si el servidor actuará como redirector de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2be5c-112">Specifies if the server will act as a Remote Desktop Services redirector.</span></span> <span data-ttu-id="2be5c-113">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2be5c-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="2be5c-114">0</span><span class="sxs-lookup"><span data-stu-id="2be5c-114">0</span></span>
</dt> <dd>

<span data-ttu-id="2be5c-115">El servidor actuará como redirector de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2be5c-115">The server will act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="2be5c-116">1</span><span class="sxs-lookup"><span data-stu-id="2be5c-116">1</span></span>
</dt> <dd>

<span data-ttu-id="2be5c-117">El servidor no actuará como redirector de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2be5c-117">The server will not act as a Remote Desktop Services redirector.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2be5c-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2be5c-118">Return value</span></span>

<span data-ttu-id="2be5c-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2be5c-119">Type: **uint32**</span></span>

<span data-ttu-id="2be5c-120">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="2be5c-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2be5c-121">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="2be5c-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="2be5c-122">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="2be5c-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="2be5c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2be5c-123">Remarks</span></span>

<span data-ttu-id="2be5c-124">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2be5c-124">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2be5c-125">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2be5c-125">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2be5c-126">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2be5c-126">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2be5c-127">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2be5c-127">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2be5c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2be5c-128">Requirements</span></span>



| <span data-ttu-id="2be5c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be5c-129">Requirement</span></span> | <span data-ttu-id="2be5c-130">Value</span><span class="sxs-lookup"><span data-stu-id="2be5c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2be5c-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2be5c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2be5c-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2be5c-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2be5c-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2be5c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2be5c-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2be5c-134">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="2be5c-135">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2be5c-135">End of client support</span></span><br/>    | <span data-ttu-id="2be5c-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2be5c-136">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2be5c-137">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2be5c-137">End of server support</span></span><br/>    | <span data-ttu-id="2be5c-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2be5c-138">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="2be5c-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2be5c-139">Namespace</span></span><br/>                | <span data-ttu-id="2be5c-140">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2be5c-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2be5c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2be5c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2be5c-142"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2be5c-142"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2be5c-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2be5c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2be5c-144"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2be5c-144"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be5c-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="2be5c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be5c-146">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="2be5c-146">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

