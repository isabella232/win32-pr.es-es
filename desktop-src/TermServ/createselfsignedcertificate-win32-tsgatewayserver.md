---
title: Método CreateSelfSignedCertificate de la clase Win32_TSGatewayServer
description: Crea un certificado autofirmado y devuelve el hash del certificado como \ 0034; out \ 0034; parámetro.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Método CreateSelfSignedCertificate Servicios de Escritorio remoto
- Método CreateSelfSignedCertificate Servicios de Escritorio remoto, clase Win32_TSGatewayServer
- Win32_TSGatewayServer de clase Servicios de Escritorio remoto, método CreateSelfSignedCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489532"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="c5f4c-106">Método CreateSelfSignedCertificate de la \_ clase TSGatewayServer de Win32</span><span class="sxs-lookup"><span data-stu-id="c5f4c-106">CreateSelfSignedCertificate method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="c5f4c-107">Crea un certificado autofirmado y devuelve el hash del certificado como un parámetro "out".</span><span class="sxs-lookup"><span data-stu-id="c5f4c-107">Creates a self-signed certificate and returns the certificate hash as an "out" parameter.</span></span> <span data-ttu-id="c5f4c-108">Además, agrega el texto " \_ \_ certificado autofirmado de puerta de enlace de TS \_ \_ " a la propiedad de contexto de certificado para que el certificado se reconozca como un certificado de puerta de enlace de escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="c5f4c-108">Also, adds the text "TS\_GATEWAY\_SELF\_SIGNED\_CERTIFICATE" to the certificate context property so that the certificate is recognized as a Remote Desktop Gateway (RD Gateway) certificate.</span></span> <span data-ttu-id="c5f4c-109">Este método usa un contenedor de claves específico de puerta de enlace de escritorio remoto para crear el certificado.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-109">This method uses an RD Gateway-specific key container to create the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f4c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5f4c-110">Syntax</span></span>


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="c5f4c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5f4c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5f4c-112">*SubjectName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5f4c-112">*SubjectName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f4c-113">Nombre del firmante del certificado autofirmado.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-113">Subject name of the self-signed certificate.</span></span>

</dd> <dt>

<span data-ttu-id="c5f4c-114">*CertHash* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c5f4c-114">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f4c-115">El hash del certificado.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-115">The certificate hash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5f4c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5f4c-116">Remarks</span></span>

<span data-ttu-id="c5f4c-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c5f4c-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c5f4c-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c5f4c-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c5f4c-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="c5f4c-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c5f4c-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c5f4c-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5f4c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5f4c-122">Requirements</span></span>



| <span data-ttu-id="c5f4c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5f4c-123">Requirement</span></span> | <span data-ttu-id="c5f4c-124">Value</span><span class="sxs-lookup"><span data-stu-id="c5f4c-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f4c-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5f4c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c5f4c-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c5f4c-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c5f4c-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5f4c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c5f4c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5f4c-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c5f4c-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5f4c-129">Namespace</span></span><br/>                | <span data-ttu-id="c5f4c-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c5f4c-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c5f4c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c5f4c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5f4c-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5f4c-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5f4c-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5f4c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5f4c-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5f4c-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c5f4c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5f4c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f4c-136">**Win32 \_ TSGatewayServer**</span><span class="sxs-lookup"><span data-stu-id="c5f4c-136">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

