---
title: Método EnvironmentVariables de la clase Win32_TSExpandEnvironmentVariables
description: Expande las variables de entorno definidas por el sistema. | Método EnvironmentVariables de la clase Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Método EnvironmentVariables Servicios de Escritorio remoto
- Método EnvironmentVariables Servicios de Escritorio remoto, clase Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables de clase Servicios de Escritorio remoto, método EnvironmentVariables
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678685"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="55faa-107">Método EnvironmentVariables de la \_ clase TSExpandEnvironmentVariables de Win32</span><span class="sxs-lookup"><span data-stu-id="55faa-107">EnvironmentVariables method of the Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="55faa-108">Expande las variables de entorno definidas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="55faa-108">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="55faa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55faa-109">Syntax</span></span>


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a><span data-ttu-id="55faa-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55faa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55faa-111">*OriginalString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55faa-111">*OriginalString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55faa-112">Cadena que contiene las variables de entorno que se van a expandir.</span><span class="sxs-lookup"><span data-stu-id="55faa-112">A string that contains the environment variables to expand.</span></span>

</dd> <dt>

<span data-ttu-id="55faa-113">*ExpandedString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="55faa-113">*ExpandedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55faa-114">Una cadena con las variables de entorno expandidas.</span><span class="sxs-lookup"><span data-stu-id="55faa-114">A string with the environment variables expanded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55faa-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55faa-115">Remarks</span></span>

<span data-ttu-id="55faa-116">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="55faa-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="55faa-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="55faa-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="55faa-118">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="55faa-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="55faa-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="55faa-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="55faa-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="55faa-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="55faa-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55faa-121">Requirements</span></span>



| <span data-ttu-id="55faa-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="55faa-122">Requirement</span></span> | <span data-ttu-id="55faa-123">Value</span><span class="sxs-lookup"><span data-stu-id="55faa-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55faa-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55faa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="55faa-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="55faa-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="55faa-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55faa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="55faa-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55faa-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55faa-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="55faa-128">Namespace</span></span><br/>                | <span data-ttu-id="55faa-129">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="55faa-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="55faa-130">MOF</span><span class="sxs-lookup"><span data-stu-id="55faa-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55faa-131"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55faa-131"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="55faa-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55faa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55faa-133"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55faa-133"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55faa-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="55faa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55faa-135">**Win32 \_ TSExpandEnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="55faa-135">**Win32\_TSExpandEnvironmentVariables**</span></span>](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

