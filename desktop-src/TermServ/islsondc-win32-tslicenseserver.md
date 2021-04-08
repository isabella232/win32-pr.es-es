---
title: Método IsLSonDC de la clase Win32_TSLicenseServer
description: Recupera si se ha instalado Escritorio remoto licencias (para la concesión de licencias de escritorio remoto) en un controlador de dominio.
ms.assetid: 43345dc8-c8b6-4c41-b26d-781293d07516
ms.tgt_platform: multiple
keywords:
- Método IsLSonDC Servicios de Escritorio remoto
- Método IsLSonDC Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsLSonDC
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSonDC
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ddbf01615903150ffa8f97fca88cfcf7fda937
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996590"
---
# <a name="islsondc-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="75bc0-106">Método IsLSonDC de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="75bc0-106">IsLSonDC method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="75bc0-107">Recupera si se ha instalado Escritorio remoto licencias (para la concesión de licencias de escritorio remoto) en un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="75bc0-107">Retrieves whether Remote Desktop Licensing (RD Licensing) is installed on a domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="75bc0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75bc0-108">Syntax</span></span>


```mof
uint32 IsLSonDC(
  [out] boolean OnDC
);
```



## <a name="parameters"></a><span data-ttu-id="75bc0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75bc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75bc0-110">*OnDC* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="75bc0-110">*OnDC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75bc0-111">Valor booleano que indica si la concesión de licencias de escritorio remoto está instalada en un controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="75bc0-111">Boolean value that indicates whether RD Licensing is installed on a domain controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75bc0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75bc0-112">Return value</span></span>

<span data-ttu-id="75bc0-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="75bc0-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="75bc0-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="75bc0-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="75bc0-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="75bc0-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75bc0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75bc0-116">Remarks</span></span>

<span data-ttu-id="75bc0-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="75bc0-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="75bc0-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="75bc0-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="75bc0-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="75bc0-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="75bc0-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="75bc0-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="75bc0-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="75bc0-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="75bc0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75bc0-122">Requirements</span></span>



| <span data-ttu-id="75bc0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="75bc0-123">Requirement</span></span> | <span data-ttu-id="75bc0-124">Value</span><span class="sxs-lookup"><span data-stu-id="75bc0-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="75bc0-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75bc0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75bc0-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="75bc0-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="75bc0-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75bc0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75bc0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75bc0-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="75bc0-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75bc0-129">Namespace</span></span><br/>                | <span data-ttu-id="75bc0-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="75bc0-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="75bc0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="75bc0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75bc0-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75bc0-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="75bc0-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75bc0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75bc0-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75bc0-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75bc0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="75bc0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75bc0-136">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="75bc0-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

