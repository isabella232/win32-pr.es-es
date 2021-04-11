---
title: Método GetProtocolName de la clase Win32_TSGatewayServerSettings
description: Devuelve el nombre de protocolo para el índice de protocolo especificado.
ms.assetid: 6778cede-cc61-4e5d-9a29-ba88197fa8c6
ms.tgt_platform: multiple
keywords:
- Método GetProtocolName Servicios de Escritorio remoto
- Método GetProtocolName Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método GetProtocolName
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetProtocolName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81064581b209f047ac492faee6d442b082d038cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150503"
---
# <a name="getprotocolname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="6e53d-106">Método GetProtocolName de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="6e53d-106">GetProtocolName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="6e53d-107">Devuelve el nombre de protocolo para el índice de protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="6e53d-107">Returns the protocol name for the specified protocol index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e53d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e53d-108">Syntax</span></span>


```mof
uint32 GetProtocolName(
  [in]  uint32 ProtocolId,
  [out] string ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="6e53d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e53d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e53d-110">*ProtocolId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e53d-110">*ProtocolId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e53d-111">Índice del identificador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="6e53d-111">Index of the protocol identifier.</span></span> <span data-ttu-id="6e53d-112">El valor debe estar entre cero y el valor de la propiedad **MaxProtocols** .</span><span class="sxs-lookup"><span data-stu-id="6e53d-112">The value must be between zero and the value of the **MaxProtocols** property.</span></span>

</dd> <dt>

<span data-ttu-id="6e53d-113">*ProtocolName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6e53d-113">*ProtocolName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e53d-114">Devuelve el nombre del protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="6e53d-114">Returns the name of the specified protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e53d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e53d-115">Return value</span></span>

<span data-ttu-id="6e53d-116">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="6e53d-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6e53d-117">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6e53d-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6e53d-118">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6e53d-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e53d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e53d-119">Remarks</span></span>

<span data-ttu-id="6e53d-120">Se admite un protocolo.</span><span class="sxs-lookup"><span data-stu-id="6e53d-120">One protocol is supported.</span></span>

<span data-ttu-id="6e53d-121">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="6e53d-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6e53d-122">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6e53d-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6e53d-123">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="6e53d-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6e53d-124">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="6e53d-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6e53d-125">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6e53d-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e53d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e53d-126">Requirements</span></span>



| <span data-ttu-id="6e53d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e53d-127">Requirement</span></span> | <span data-ttu-id="6e53d-128">Value</span><span class="sxs-lookup"><span data-stu-id="6e53d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e53d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e53d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6e53d-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6e53d-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6e53d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e53d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6e53d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e53d-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6e53d-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6e53d-133">Namespace</span></span><br/>                | <span data-ttu-id="6e53d-134">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6e53d-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6e53d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6e53d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e53d-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e53d-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e53d-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e53d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e53d-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e53d-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6e53d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e53d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e53d-140">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="6e53d-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

