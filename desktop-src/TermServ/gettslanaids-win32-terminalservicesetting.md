---
title: Método GetTSLanaIds de la clase Win32_TerminalServiceSetting
description: Obtiene los identificadores y descripciones del adaptador de red de área local (LANA) de NetBIOS de Servicios de Escritorio remoto adaptadores de red.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- Método GetTSLanaIds Servicios de Escritorio remoto
- Método GetTSLanaIds Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método GetTSLanaIds
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d2b2357df7e6d7ccc2cb8a774ba34c50cb46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493199"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="4956d-106">Método GetTSLanaIds de la \_ clase TerminalServiceSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="4956d-106">GetTSLanaIds method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="4956d-107">El método **GetTSLanaIds** obtiene los identificadores de adaptador de red de área local (lana) NetBIOS y las descripciones de servicios de escritorio remoto adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="4956d-107">The **GetTSLanaIds** method gets the NetBIOS Local Area Network Adapter (LANA) IDs and descriptions of Remote Desktop Services network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="4956d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4956d-108">Syntax</span></span>


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="4956d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4956d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4956d-110">*LanaIdList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4956d-110">*LanaIdList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4956d-111">Matriz de números LANA.</span><span class="sxs-lookup"><span data-stu-id="4956d-111">Array of LANA numbers.</span></span>

</dd> <dt>

<span data-ttu-id="4956d-112">*LanaIdDescriptions* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4956d-112">*LanaIdDescriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4956d-113">Matriz de descripciones de LANA correspondiente a la matriz *LanaIdList* .</span><span class="sxs-lookup"><span data-stu-id="4956d-113">Array of LANA descriptions corresponding to the *LanaIdList* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4956d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4956d-114">Return value</span></span>

<span data-ttu-id="4956d-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="4956d-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4956d-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="4956d-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4956d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4956d-117">Remarks</span></span>

<span data-ttu-id="4956d-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4956d-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4956d-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4956d-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4956d-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="4956d-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4956d-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4956d-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4956d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4956d-122">Requirements</span></span>



| <span data-ttu-id="4956d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4956d-123">Requirement</span></span> | <span data-ttu-id="4956d-124">Value</span><span class="sxs-lookup"><span data-stu-id="4956d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4956d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4956d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4956d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4956d-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4956d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4956d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4956d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4956d-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4956d-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4956d-129">Namespace</span></span><br/>                | <span data-ttu-id="4956d-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4956d-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4956d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4956d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4956d-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4956d-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4956d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4956d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4956d-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4956d-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4956d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4956d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4956d-136">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="4956d-136">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

