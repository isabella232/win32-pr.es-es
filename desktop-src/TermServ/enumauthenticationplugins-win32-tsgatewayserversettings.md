---
title: Método EnumAuthenticationPlugins de la clase Win32_TSGatewayServerSettings
description: Enumera todos los complementos de autenticación registrados.
ms.assetid: a5c1859d-e20c-4c72-aef5-ef9941edf73e
ms.tgt_platform: multiple
keywords:
- Método EnumAuthenticationPlugins Servicios de Escritorio remoto
- Método EnumAuthenticationPlugins Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método EnumAuthenticationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthenticationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0cd9d059a79749f657c6191e68e7bcd08555cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676644"
---
# <a name="enumauthenticationplugins-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="b3fd0-106">Método EnumAuthenticationPlugins de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="b3fd0-106">EnumAuthenticationPlugins method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="b3fd0-107">Enumera todos los complementos de autenticación registrados.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-107">Enumerates all registered authentication plug-ins.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3fd0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3fd0-108">Syntax</span></span>


```mof
uint32 EnumAuthenticationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="b3fd0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3fd0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3fd0-110">*PluginNames* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b3fd0-110">*PluginNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fd0-111">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b3fd0-111">Type: **string\[\]**</span></span>

<span data-ttu-id="b3fd0-112">Una matriz de **cadena** que recibe los nombres de los complementos de autenticación registrados.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-112">A **string** array that receives the names of the registered authentication plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="b3fd0-113">*CLSID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b3fd0-113">*CLSIDs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fd0-114">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b3fd0-114">Type: **string\[\]**</span></span>

<span data-ttu-id="b3fd0-115">Una matriz de **cadena** que recibe los CLSID de los complementos de autenticación registrados.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-115">A **string** array that receives the CLSIDs of the registered authentication plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="b3fd0-116">*Descripciones* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b3fd0-116">*Descriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fd0-117">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b3fd0-117">Type: **string\[\]**</span></span>

<span data-ttu-id="b3fd0-118">Una matriz de **cadena** que recibe las descripciones de los complementos de autenticación registrados.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-118">A **string** array that receives the descriptions of the registered authentication plug-ins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3fd0-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3fd0-119">Return value</span></span>

<span data-ttu-id="b3fd0-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3fd0-120">Type: **uint32**</span></span>

<span data-ttu-id="b3fd0-121">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b3fd0-122">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b3fd0-123">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b3fd0-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3fd0-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3fd0-124">Remarks</span></span>

<span data-ttu-id="b3fd0-125">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b3fd0-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b3fd0-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b3fd0-127">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b3fd0-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="b3fd0-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b3fd0-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b3fd0-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3fd0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3fd0-130">Requirements</span></span>



| <span data-ttu-id="b3fd0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3fd0-131">Requirement</span></span> | <span data-ttu-id="b3fd0-132">Value</span><span class="sxs-lookup"><span data-stu-id="b3fd0-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3fd0-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3fd0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b3fd0-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b3fd0-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b3fd0-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3fd0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b3fd0-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3fd0-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="b3fd0-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b3fd0-137">Namespace</span></span><br/>                | <span data-ttu-id="b3fd0-138">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b3fd0-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b3fd0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b3fd0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3fd0-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3fd0-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3fd0-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3fd0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3fd0-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3fd0-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b3fd0-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3fd0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3fd0-144">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="b3fd0-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

