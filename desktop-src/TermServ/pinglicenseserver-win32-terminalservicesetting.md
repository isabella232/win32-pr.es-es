---
title: Método PingLicenseServer de la clase Win32_TerminalServiceSetting
description: PingLicenseServer ya no está disponible.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Método PingLicenseServer Servicios de Escritorio remoto
- Método PingLicenseServer Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método PingLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422271"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="fc11a-106">Método PingLicenseServer de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="fc11a-106">PingLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="fc11a-107">\[**PingLicenseServer** ya no está disponible para su uso a partir de Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="fc11a-107">\[**PingLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="fc11a-108">**Windows Server 2008:** Hace ping en el servidor de licencias para determinar si se trata de un servidor de licencias válido.</span><span class="sxs-lookup"><span data-stu-id="fc11a-108">**Windows Server 2008:** Pings the license server to determine if it is a valid license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc11a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc11a-109">Syntax</span></span>


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="fc11a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc11a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc11a-111">*NombreDeServidor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc11a-111">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc11a-112">Nombre del servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="fc11a-112">Name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc11a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc11a-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="fc11a-114">**S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="fc11a-114">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="fc11a-115">El servidor es un servidor de licencias válido.</span><span class="sxs-lookup"><span data-stu-id="fc11a-115">The server is a valid license server.</span></span>

</dd> <dt>

<span data-ttu-id="fc11a-116">**S \_ false**</span><span class="sxs-lookup"><span data-stu-id="fc11a-116">**S\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="fc11a-117">El servidor de licencias no es válido.</span><span class="sxs-lookup"><span data-stu-id="fc11a-117">The license server is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc11a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc11a-118">Remarks</span></span>

<span data-ttu-id="fc11a-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fc11a-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fc11a-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fc11a-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fc11a-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="fc11a-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fc11a-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fc11a-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc11a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc11a-123">Requirements</span></span>



| <span data-ttu-id="fc11a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc11a-124">Requirement</span></span> | <span data-ttu-id="fc11a-125">Value</span><span class="sxs-lookup"><span data-stu-id="fc11a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc11a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc11a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fc11a-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fc11a-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fc11a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc11a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fc11a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc11a-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc11a-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fc11a-130">End of client support</span></span><br/>    | <span data-ttu-id="fc11a-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fc11a-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fc11a-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fc11a-132">End of server support</span></span><br/>    | <span data-ttu-id="fc11a-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc11a-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc11a-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc11a-134">Namespace</span></span><br/>                | <span data-ttu-id="fc11a-135">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fc11a-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fc11a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="fc11a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc11a-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc11a-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc11a-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc11a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc11a-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc11a-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc11a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc11a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc11a-141">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="fc11a-141">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

