---
title: Método SetServerWeight de la clase Win32_TSSessionDirectory
description: Establece el valor de peso del servidor para el equilibrio de carga de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).
ms.assetid: 9c7563e5-bb45-495d-90b0-43170b58581e
ms.tgt_platform: multiple
keywords:
- Método SetServerWeight Servicios de Escritorio remoto
- Método SetServerWeight Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método SetServerWeight
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetServerWeight
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e8456fa590de0c9d6236f96f3b09c16087d730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491608"
---
# <a name="setserverweight-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="01f91-106">Método SetServerWeight de la \_ clase TSSessionDirectory de Win32</span><span class="sxs-lookup"><span data-stu-id="01f91-106">SetServerWeight method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="01f91-107">Establece el valor de peso del servidor para el equilibrio de carga de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="01f91-107">Sets the server weight value for Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f91-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01f91-108">Syntax</span></span>


```mof
uint32 SetServerWeight(
  [in] uint32 ServerWeightValue
);
```



## <a name="parameters"></a><span data-ttu-id="01f91-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01f91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f91-110">*ServerWeightValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="01f91-110">*ServerWeightValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01f91-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01f91-111">Type: **uint32**</span></span>

<span data-ttu-id="01f91-112">Valor del peso del servidor.</span><span class="sxs-lookup"><span data-stu-id="01f91-112">The server weight value.</span></span> <span data-ttu-id="01f91-113">El intervalo válido es de 1 a 10000.</span><span class="sxs-lookup"><span data-stu-id="01f91-113">The valid range is 1 to 10000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01f91-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01f91-114">Remarks</span></span>

<span data-ttu-id="01f91-115">De forma predeterminada, en la interfaz de usuario de Servicios de Escritorio remoto configuración, el valor de peso del servidor es 100.</span><span class="sxs-lookup"><span data-stu-id="01f91-115">By default in the user interface of Remote Desktop Services Configuration, the server weight value is 100.</span></span> <span data-ttu-id="01f91-116">El peso del servidor es relativo.</span><span class="sxs-lookup"><span data-stu-id="01f91-116">The server weight is relative.</span></span> <span data-ttu-id="01f91-117">Por lo tanto, si asigna un valor de a un servidor de 100 y un valor de 200, el servidor con un peso relativo de 200 recibirá dos veces el número de sesiones.</span><span class="sxs-lookup"><span data-stu-id="01f91-117">Therefore, if you assign one server a value of 100, and one a value of 200, the server with a relative weight of 200 will receive twice the number of sessions.</span></span>

<span data-ttu-id="01f91-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="01f91-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="01f91-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="01f91-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="01f91-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="01f91-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="01f91-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="01f91-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="01f91-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01f91-122">Requirements</span></span>



| <span data-ttu-id="01f91-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="01f91-123">Requirement</span></span> | <span data-ttu-id="01f91-124">Value</span><span class="sxs-lookup"><span data-stu-id="01f91-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01f91-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01f91-125">Minimum supported client</span></span><br/> | <span data-ttu-id="01f91-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="01f91-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="01f91-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01f91-127">Minimum supported server</span></span><br/> | <span data-ttu-id="01f91-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01f91-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01f91-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01f91-129">Namespace</span></span><br/>                | <span data-ttu-id="01f91-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="01f91-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="01f91-131">MOF</span><span class="sxs-lookup"><span data-stu-id="01f91-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01f91-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01f91-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="01f91-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01f91-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01f91-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01f91-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01f91-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="01f91-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f91-136">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="01f91-136">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

