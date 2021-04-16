---
title: Método IsLSPublished de la clase Win32_TSLicenseServer
description: Recupera si el servidor de licencias de Escritorio remoto se publica en Active Directory Domain Services (AD \ 160; DS).
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- Método IsLSPublished Servicios de Escritorio remoto
- Método IsLSPublished Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsLSPublished
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69add751497ed52a107ea7183bb4b7cce4ea88c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676813"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="b209e-106">Método IsLSPublished de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="b209e-106">IsLSPublished method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="b209e-107">Recupera si el servidor de licencias de Escritorio remoto se publica en Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="b209e-107">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="b209e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b209e-108">Syntax</span></span>


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a><span data-ttu-id="b209e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b209e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b209e-110">*Publicado* \[ por enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b209e-110">*Published* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b209e-111">Valor booleano que indica si el servidor de licencias está publicado en AD DS.</span><span class="sxs-lookup"><span data-stu-id="b209e-111">Boolean value that indicates whether the license server is published in AD DS.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b209e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b209e-112">Return value</span></span>

<span data-ttu-id="b209e-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b209e-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b209e-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b209e-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b209e-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b209e-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b209e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b209e-116">Remarks</span></span>

<span data-ttu-id="b209e-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="b209e-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b209e-118">Si el servidor de licencias está publicado en AD DS, se detectará Escritorio remoto automáticamente en los servidores host de sesión de escritorio remoto (host de sesión de RD) del mismo bosque.</span><span class="sxs-lookup"><span data-stu-id="b209e-118">If the license server is published in AD DS, it will be automatically discoverable by Remote Desktop Session Host (RD Session Host) servers in the same forest.</span></span>

<span data-ttu-id="b209e-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b209e-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b209e-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b209e-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b209e-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="b209e-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b209e-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b209e-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b209e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b209e-123">Requirements</span></span>



| <span data-ttu-id="b209e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b209e-124">Requirement</span></span> | <span data-ttu-id="b209e-125">Value</span><span class="sxs-lookup"><span data-stu-id="b209e-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b209e-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b209e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b209e-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b209e-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b209e-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b209e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b209e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b209e-129">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b209e-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b209e-130">Namespace</span></span><br/>                | <span data-ttu-id="b209e-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b209e-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b209e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b209e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b209e-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b209e-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b209e-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b209e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b209e-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b209e-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b209e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b209e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b209e-137">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="b209e-137">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

