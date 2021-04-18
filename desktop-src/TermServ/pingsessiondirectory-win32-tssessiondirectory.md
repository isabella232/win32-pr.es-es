---
title: Método PingSessionDirectory de la clase Win32_TSSessionDirectory
description: Comprueba si el servidor de agente de conexión a escritorio remoto (Broker) de Conexión a Escritorio remoto está disponible.
ms.assetid: 89243998-5ab2-4ea6-aa31-95ec63289055
ms.tgt_platform: multiple
keywords:
- Método PingSessionDirectory Servicios de Escritorio remoto
- Método PingSessionDirectory Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método PingSessionDirectory
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.PingSessionDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4022a0c34094a19651522c3f8153038c6d9df503
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534426"
---
# <a name="pingsessiondirectory-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="e8c7d-106">Método PingSessionDirectory de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="e8c7d-106">PingSessionDirectory method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="e8c7d-107">Comprueba si el servidor de agente de conexión a escritorio remoto (Broker) de Conexión a Escritorio remoto está disponible.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-107">Checks whether the Remote Desktop Connection Broker (RD Connection Broker) server is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c7d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8c7d-108">Syntax</span></span>


```mof
uint32 PingSessionDirectory(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="e8c7d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8c7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c7d-110">*NombreDeServidor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8c7d-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c7d-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="e8c7d-111">Type: **string**</span></span>

<span data-ttu-id="e8c7d-112">Nombre del servidor de agente de conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-112">Name of the RD Connection Broker server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c7d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8c7d-113">Return value</span></span>

<span data-ttu-id="e8c7d-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e8c7d-114">Type: **uint32**</span></span>

<span data-ttu-id="e8c7d-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e8c7d-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c7d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8c7d-117">Remarks</span></span>

<span data-ttu-id="e8c7d-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e8c7d-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e8c7d-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e8c7d-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e8c7d-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e8c7d-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c7d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8c7d-122">Requirements</span></span>



| <span data-ttu-id="e8c7d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8c7d-123">Requirement</span></span> | <span data-ttu-id="e8c7d-124">Value</span><span class="sxs-lookup"><span data-stu-id="e8c7d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c7d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8c7d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e8c7d-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e8c7d-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e8c7d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8c7d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e8c7d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8c7d-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8c7d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e8c7d-129">Namespace</span></span><br/>                | <span data-ttu-id="e8c7d-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e8c7d-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e8c7d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e8c7d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8c7d-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8c7d-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8c7d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8c7d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8c7d-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8c7d-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8c7d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8c7d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c7d-136">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="e8c7d-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

