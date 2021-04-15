---
title: Método CreateWinstation de la clase Win32_TerminalServiceSetting
description: Crea una nueva pila de agentes de escucha basada en la combinación única de nombre del agente de escucha y NIC.
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- Método CreateWinstation Servicios de Escritorio remoto
- Método CreateWinstation Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método CreateWinstation
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 112237a00e9e92a2074ee0b95f9964d73f083e43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676610"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f5d8b-106">Método CreateWinstation de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="f5d8b-106">CreateWinstation method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f5d8b-107">El método **CreateWinstation** crea una nueva pila de agentes de escucha basada en la combinación única de nombre del agente de escucha y NIC.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-107">The **CreateWinstation** method creates a new listener stack based on the unique combination of listener name and NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d8b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5d8b-108">Syntax</span></span>


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a><span data-ttu-id="f5d8b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5d8b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d8b-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f5d8b-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d8b-111">Nombre del agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-111">Listener name.</span></span>

</dd> <dt>

<span data-ttu-id="f5d8b-112">*WinstaDriverName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5d8b-112">*WinstaDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d8b-113">El nombre del controlador de la estación de la</span><span class="sxs-lookup"><span data-stu-id="f5d8b-113">The winstation driver name.</span></span>

</dd> <dt>

<span data-ttu-id="f5d8b-114">*LanaId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5d8b-114">*LanaId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d8b-115">Número de adaptador de red de área local (LANA) de NetBIOS para la NIC.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-115">NetBIOS Local Area Network Adapter (LANA) number for the NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d8b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5d8b-116">Return value</span></span>

<span data-ttu-id="f5d8b-117">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f5d8b-118">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5d8b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5d8b-119">Remarks</span></span>

<span data-ttu-id="f5d8b-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f5d8b-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f5d8b-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f5d8b-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f5d8b-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f5d8b-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f5d8b-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d8b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5d8b-124">Requirements</span></span>



| <span data-ttu-id="f5d8b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5d8b-125">Requirement</span></span> | <span data-ttu-id="f5d8b-126">Value</span><span class="sxs-lookup"><span data-stu-id="f5d8b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d8b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5d8b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d8b-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5d8b-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5d8b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5d8b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d8b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5d8b-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5d8b-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f5d8b-131">Namespace</span></span><br/>                | <span data-ttu-id="f5d8b-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f5d8b-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f5d8b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f5d8b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5d8b-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5d8b-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5d8b-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5d8b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5d8b-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5d8b-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5d8b-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5d8b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d8b-138">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="f5d8b-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

