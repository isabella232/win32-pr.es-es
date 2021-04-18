---
title: Método SetSessionDirectoryProperty de la clase Win32_TSSessionDirectory
description: Establece la propiedad SessionDirectoryLocation o la propiedad SessionDirectoryClusterName de la clase.
ms.assetid: 728e1991-294f-4b80-86f8-a0c2cfd10e9c
ms.tgt_platform: multiple
keywords:
- Método SetSessionDirectoryProperty Servicios de Escritorio remoto
- Método SetSessionDirectoryProperty Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método SetSessionDirectoryProperty
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32357e662ec9b2edb05d75a2814d5215fc9ec7f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490084"
---
# <a name="setsessiondirectoryproperty-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="29568-106">Método SetSessionDirectoryProperty de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="29568-106">SetSessionDirectoryProperty method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="29568-107">Establece la propiedad **SessionDirectoryLocation** o la propiedad **SessionDirectoryClusterName** de la clase.</span><span class="sxs-lookup"><span data-stu-id="29568-107">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="29568-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29568-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryProperty(
  [in] string PropertyName,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="29568-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29568-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29568-110">*NombreDePropiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29568-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29568-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="29568-111">Type: **string**</span></span>

<span data-ttu-id="29568-112">Especifica la propiedad que está estableciendo el método.</span><span class="sxs-lookup"><span data-stu-id="29568-112">Specifies the property that the method is setting.</span></span>

<dt>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>

<span data-ttu-id="29568-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="29568-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span></span>


</dt> <dd>

<span data-ttu-id="29568-114">El método está estableciendo la propiedad **SessionDirectoryLocation** .</span><span class="sxs-lookup"><span data-stu-id="29568-114">The method is setting the **SessionDirectoryLocation** property.</span></span>

</dd> <dt>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>

<span data-ttu-id="29568-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="29568-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span></span>


</dt> <dd>

<span data-ttu-id="29568-116">El método está estableciendo la propiedad **SessionDirectoryClusterName** .</span><span class="sxs-lookup"><span data-stu-id="29568-116">The method is setting the **SessionDirectoryClusterName** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="29568-117">*Valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="29568-117">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29568-118">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="29568-118">Type: **string**</span></span>

<span data-ttu-id="29568-119">Nuevo valor de la propiedad especificada por el parámetro *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="29568-119">The new value for the property specified by the *PropertyName* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29568-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29568-120">Return value</span></span>

<span data-ttu-id="29568-121">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29568-121">Type: **uint32**</span></span>

<span data-ttu-id="29568-122">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="29568-122">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="29568-123">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="29568-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="29568-124">El método devuelve un error si la configuración está en control de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="29568-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="29568-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29568-125">Remarks</span></span>

<span data-ttu-id="29568-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="29568-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="29568-127">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="29568-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="29568-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="29568-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="29568-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="29568-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="29568-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29568-130">Requirements</span></span>



| <span data-ttu-id="29568-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="29568-131">Requirement</span></span> | <span data-ttu-id="29568-132">Value</span><span class="sxs-lookup"><span data-stu-id="29568-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29568-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29568-133">Minimum supported client</span></span><br/> | <span data-ttu-id="29568-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="29568-134">None supported</span></span><br/>                                                               |
| <span data-ttu-id="29568-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29568-135">Minimum supported server</span></span><br/> | <span data-ttu-id="29568-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29568-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29568-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="29568-137">Namespace</span></span><br/>                | <span data-ttu-id="29568-138">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="29568-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="29568-139">MOF</span><span class="sxs-lookup"><span data-stu-id="29568-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29568-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29568-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="29568-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29568-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29568-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29568-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29568-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="29568-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29568-144">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="29568-144">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

