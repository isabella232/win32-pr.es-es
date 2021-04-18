---
title: Método TSGStoreConsentMsg de la clase Win32_TSGatewayServerSettings
description: Actualiza el mensaje de consentimiento para el servidor de puerta de enlace.
ms.assetid: b3146d87-95af-4b6b-8c02-5ac4748fbe98
ms.tgt_platform: multiple
keywords:
- Método TSGStoreConsentMsg Servicios de Escritorio remoto
- Método TSGStoreConsentMsg Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método TSGStoreConsentMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907097739d21e1523aca3b719cdb5f18b6f3fa30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490984"
---
# <a name="tsgstoreconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="c33d4-106">Método TSGStoreConsentMsg de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="c33d4-106">TSGStoreConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="c33d4-107">Actualiza el mensaje de consentimiento para el servidor de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="c33d4-107">Updates the consent message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c33d4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c33d4-108">Syntax</span></span>


```mof
uint32 TSGStoreConsentMsg(
  [in] string TSGConMsgText
);
```



## <a name="parameters"></a><span data-ttu-id="c33d4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c33d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c33d4-110">*TSGConMsgText* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c33d4-110">*TSGConMsgText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33d4-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="c33d4-111">Type: **string**</span></span>

<span data-ttu-id="c33d4-112">Texto del mensaje de consentimiento.</span><span class="sxs-lookup"><span data-stu-id="c33d4-112">The consent message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c33d4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c33d4-113">Return value</span></span>

<span data-ttu-id="c33d4-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c33d4-114">Type: **uint32**</span></span>

<span data-ttu-id="c33d4-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="c33d4-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c33d4-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c33d4-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c33d4-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c33d4-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c33d4-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c33d4-118">Remarks</span></span>

<span data-ttu-id="c33d4-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="c33d4-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c33d4-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c33d4-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c33d4-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c33d4-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c33d4-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="c33d4-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c33d4-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c33d4-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c33d4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c33d4-124">Requirements</span></span>



| <span data-ttu-id="c33d4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c33d4-125">Requirement</span></span> | <span data-ttu-id="c33d4-126">Value</span><span class="sxs-lookup"><span data-stu-id="c33d4-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c33d4-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c33d4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c33d4-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c33d4-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c33d4-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c33d4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c33d4-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c33d4-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c33d4-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c33d4-131">Namespace</span></span><br/>                | <span data-ttu-id="c33d4-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c33d4-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c33d4-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c33d4-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c33d4-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c33d4-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c33d4-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c33d4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c33d4-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c33d4-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c33d4-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c33d4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33d4-138">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="c33d4-138">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

