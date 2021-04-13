---
title: Método IsTSinTSCGroup de la clase Win32_TSLicenseServer
description: Recupera si un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) es miembro del grupo local Terminal Server equipos en el servidor de licencias de Escritorio remoto.
ms.assetid: 61c39928-3a2b-4a36-ae4e-b9597a12d5e7
ms.tgt_platform: multiple
keywords:
- Método IsTSinTSCGroup Servicios de Escritorio remoto
- Método IsTSinTSCGroup Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsTSinTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSinTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d666457f053c8fd48abd904d099bfbfa93a0de6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535217"
---
# <a name="istsintscgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="882de-106">Método IsTSinTSCGroup de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="882de-106">IsTSinTSCGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="882de-107">Recupera si un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) es miembro del grupo local Terminal Server equipos en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="882de-107">Retrieves whether a Remote Desktop Session Host (RD Session Host) server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="882de-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="882de-108">Syntax</span></span>


```mof
uint32 IsTSinTSCGroup(
  [in]  string  tsname,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="882de-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="882de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="882de-110">*tsname* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="882de-110">*tsname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="882de-111">Nombre del servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="882de-111">Name of the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="882de-112">*IsMember* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="882de-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="882de-113">Valor booleano que indica si el servidor host de sesión de escritorio remoto es miembro del grupo local de Terminal Server equipos.</span><span class="sxs-lookup"><span data-stu-id="882de-113">Boolean value that indicates whether the RD Session Host server is a member of the Terminal Server Computers local group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="882de-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="882de-114">Return value</span></span>

<span data-ttu-id="882de-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="882de-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="882de-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="882de-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="882de-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="882de-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="882de-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="882de-118">Remarks</span></span>

<span data-ttu-id="882de-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="882de-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="882de-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="882de-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="882de-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="882de-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="882de-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="882de-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="882de-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="882de-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="882de-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="882de-124">Requirements</span></span>



| <span data-ttu-id="882de-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="882de-125">Requirement</span></span> | <span data-ttu-id="882de-126">Value</span><span class="sxs-lookup"><span data-stu-id="882de-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="882de-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="882de-127">Minimum supported client</span></span><br/> | <span data-ttu-id="882de-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="882de-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="882de-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="882de-129">Minimum supported server</span></span><br/> | <span data-ttu-id="882de-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="882de-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="882de-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="882de-131">Namespace</span></span><br/>                | <span data-ttu-id="882de-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="882de-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="882de-133">MOF</span><span class="sxs-lookup"><span data-stu-id="882de-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="882de-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="882de-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="882de-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="882de-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="882de-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="882de-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="882de-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="882de-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="882de-138">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="882de-138">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

