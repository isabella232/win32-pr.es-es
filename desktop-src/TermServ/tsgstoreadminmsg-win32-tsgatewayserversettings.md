---
title: Método TSGStoreAdminMsg de la clase Win32_TSGatewayServerSettings
description: Actualiza el mensaje administrativo para el servidor de puerta de enlace.
ms.assetid: 84e5b967-12fd-47a7-93e4-2550c15c4491
ms.tgt_platform: multiple
keywords:
- Método TSGStoreAdminMsg Servicios de Escritorio remoto
- Método TSGStoreAdminMsg Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método TSGStoreAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 398a027d28970b28b4a1e7db37b5fbfee06e881e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905304"
---
# <a name="tsgstoreadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="faa05-106">Método TSGStoreAdminMsg de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="faa05-106">TSGStoreAdminMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="faa05-107">Actualiza el mensaje administrativo para el servidor de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="faa05-107">Updates the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="faa05-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="faa05-108">Syntax</span></span>


```mof
uint32 TSGStoreAdminMsg(
  [in] string TSGAdmMsg,
  [in] string MsgStartTime,
  [in] string MsgEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="faa05-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="faa05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faa05-110">*TSGAdmMsg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="faa05-110">*TSGAdmMsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faa05-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="faa05-111">Type: **string**</span></span>

<span data-ttu-id="faa05-112">El texto del mensaje administrativo.</span><span class="sxs-lookup"><span data-stu-id="faa05-112">The administrative message text.</span></span>

</dd> <dt>

<span data-ttu-id="faa05-113">*MsgStartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="faa05-113">*MsgStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faa05-114">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="faa05-114">Type: **string**</span></span>

<span data-ttu-id="faa05-115">La hora de inicio del mensaje administrativo.</span><span class="sxs-lookup"><span data-stu-id="faa05-115">The administrative message start time.</span></span>

</dd> <dt>

<span data-ttu-id="faa05-116">*MsgEndTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="faa05-116">*MsgEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faa05-117">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="faa05-117">Type: **string**</span></span>

<span data-ttu-id="faa05-118">La hora de finalización del mensaje administrativo.</span><span class="sxs-lookup"><span data-stu-id="faa05-118">The administrative message end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faa05-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="faa05-119">Return value</span></span>

<span data-ttu-id="faa05-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="faa05-120">Type: **uint32**</span></span>

<span data-ttu-id="faa05-121">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="faa05-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="faa05-122">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="faa05-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="faa05-123">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="faa05-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="faa05-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="faa05-124">Remarks</span></span>

<span data-ttu-id="faa05-125">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="faa05-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="faa05-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="faa05-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="faa05-127">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="faa05-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="faa05-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="faa05-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="faa05-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="faa05-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="faa05-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faa05-130">Requirements</span></span>



| <span data-ttu-id="faa05-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="faa05-131">Requirement</span></span> | <span data-ttu-id="faa05-132">Value</span><span class="sxs-lookup"><span data-stu-id="faa05-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="faa05-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="faa05-133">Minimum supported client</span></span><br/> | <span data-ttu-id="faa05-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="faa05-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="faa05-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="faa05-135">Minimum supported server</span></span><br/> | <span data-ttu-id="faa05-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="faa05-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="faa05-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="faa05-137">Namespace</span></span><br/>                | <span data-ttu-id="faa05-138">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="faa05-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="faa05-139">MOF</span><span class="sxs-lookup"><span data-stu-id="faa05-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faa05-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="faa05-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="faa05-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="faa05-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faa05-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faa05-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="faa05-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="faa05-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa05-144">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="faa05-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

