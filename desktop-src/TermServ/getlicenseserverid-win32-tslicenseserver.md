---
title: Método GetLicenseServerId de la clase Win32_TSLicenseServer
description: Recupera el identificador del servidor de licencias Escritorio remoto si el servidor está activado actualmente.
ms.assetid: 0eb2cf82-3632-4693-97d2-0cfa814d8c94
ms.tgt_platform: multiple
keywords:
- Método GetLicenseServerId Servicios de Escritorio remoto
- Método GetLicenseServerId Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método GetLicenseServerId
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetLicenseServerId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a5883a5a52a0d111959e1f9fc1cbe9da5357d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422148"
---
# <a name="getlicenseserverid-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="3dd94-106">Método GetLicenseServerId de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="3dd94-106">GetLicenseServerId method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="3dd94-107">Recupera el identificador del servidor de licencias Escritorio remoto si el servidor está activado actualmente.</span><span class="sxs-lookup"><span data-stu-id="3dd94-107">Retrieves the Remote Desktop license server identifier if the server is currently activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd94-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3dd94-108">Syntax</span></span>


```mof
uint32 GetLicenseServerId(
  [out] string sLicenseServerId
);
```



## <a name="parameters"></a><span data-ttu-id="3dd94-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3dd94-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd94-110">*sLicenseServerId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3dd94-110">*sLicenseServerId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd94-111">Identificador del servidor de licencias Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="3dd94-111">Remote Desktop license server identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd94-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3dd94-112">Return value</span></span>

<span data-ttu-id="3dd94-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="3dd94-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3dd94-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="3dd94-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3dd94-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3dd94-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd94-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3dd94-116">Remarks</span></span>

<span data-ttu-id="3dd94-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="3dd94-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3dd94-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3dd94-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3dd94-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3dd94-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3dd94-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="3dd94-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3dd94-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3dd94-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd94-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dd94-122">Requirements</span></span>



| <span data-ttu-id="3dd94-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dd94-123">Requirement</span></span> | <span data-ttu-id="3dd94-124">Value</span><span class="sxs-lookup"><span data-stu-id="3dd94-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd94-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dd94-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd94-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3dd94-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3dd94-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dd94-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd94-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3dd94-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="3dd94-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3dd94-129">Namespace</span></span><br/>                | <span data-ttu-id="3dd94-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3dd94-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3dd94-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3dd94-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dd94-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3dd94-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3dd94-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3dd94-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dd94-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dd94-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd94-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3dd94-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd94-136">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="3dd94-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

