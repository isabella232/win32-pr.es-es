---
title: Método QueryCertContext de la clase Win32_TSGatewayServerSettings
description: Indica si el certificado especificado está instalado.
ms.assetid: 25d56f72-befd-46b4-84ff-dca748eeaca4
ms.tgt_platform: multiple
keywords:
- Método QueryCertContext Servicios de Escritorio remoto
- Método QueryCertContext Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método QueryCertContext
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.QueryCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e158b348debc610682380d793b66949c5a7648
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492707"
---
# <a name="querycertcontext-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="bc8b8-106">Método QueryCertContext de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="bc8b8-106">QueryCertContext method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="bc8b8-107">Indica si el certificado especificado está instalado.</span><span class="sxs-lookup"><span data-stu-id="bc8b8-107">Indicates whether the specified certificate is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8b8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc8b8-108">Syntax</span></span>


```mof
uint32 QueryCertContext(
  [out] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="bc8b8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc8b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8b8-110">*CertHash* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bc8b8-110">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8b8-111">Hash del certificado utilizado por el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="bc8b8-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8b8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc8b8-112">Return value</span></span>

<span data-ttu-id="bc8b8-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="bc8b8-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bc8b8-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="bc8b8-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bc8b8-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bc8b8-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bc8b8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc8b8-116">Remarks</span></span>

<span data-ttu-id="bc8b8-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="bc8b8-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bc8b8-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bc8b8-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bc8b8-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bc8b8-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bc8b8-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="bc8b8-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bc8b8-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bc8b8-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8b8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc8b8-122">Requirements</span></span>



| <span data-ttu-id="bc8b8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc8b8-123">Requirement</span></span> | <span data-ttu-id="bc8b8-124">Value</span><span class="sxs-lookup"><span data-stu-id="bc8b8-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8b8-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc8b8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bc8b8-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bc8b8-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bc8b8-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc8b8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bc8b8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc8b8-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bc8b8-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bc8b8-129">Namespace</span></span><br/>                | <span data-ttu-id="bc8b8-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bc8b8-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bc8b8-131">MOF</span><span class="sxs-lookup"><span data-stu-id="bc8b8-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc8b8-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc8b8-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc8b8-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc8b8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc8b8-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc8b8-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bc8b8-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc8b8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8b8-136">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="bc8b8-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

