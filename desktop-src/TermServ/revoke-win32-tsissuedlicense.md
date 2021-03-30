---
title: Método REVOKE de la clase Win32_TSIssuedLicense
description: Revoca el Servicios de Escritorio remoto licencias de acceso de cliente por dispositivo (RDS \ 160; Cal por dispositivo) representadas por el \_ objeto TSIssuedLicense de Win32. No es una función estática.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Método REVOKE Servicios de Escritorio remoto
- Método REVOKE Servicios de Escritorio remoto, clase Win32_TSIssuedLicense
- Clase Win32_TSIssuedLicense Servicios de Escritorio remoto, método REVOKE
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803866"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a><span data-ttu-id="d18b3-107">Método REVOKE de la \_ clase Win32 TSIssuedLicense</span><span class="sxs-lookup"><span data-stu-id="d18b3-107">Revoke method of the Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="d18b3-108">Revoca el Servicios de Escritorio remoto licencias de acceso de cliente por dispositivo (cal por dispositivo de RDS) representadas por el objeto [**\_ TSIssuedLicense de Win32**](win32-tsissuedlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="d18b3-108">Revokes the Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are represented by the [**Win32\_TSIssuedLicense**](win32-tsissuedlicense.md) object.</span></span> <span data-ttu-id="d18b3-109">No es una función estática.</span><span class="sxs-lookup"><span data-stu-id="d18b3-109">This is not a static function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d18b3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d18b3-110">Syntax</span></span>


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a><span data-ttu-id="d18b3-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d18b3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d18b3-112">*RevokableCals* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d18b3-112">*RevokableCals* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d18b3-113">Número de cal de RDS del mismo tipo que el objeto actual que se puede revocar.</span><span class="sxs-lookup"><span data-stu-id="d18b3-113">Number of RDS CALs of the same type as the current object that can be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="d18b3-114">*NextRevokeAllowedOn* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d18b3-114">*NextRevokeAllowedOn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d18b3-115">Fecha en la que el administrador puede intentar revocar las licencias.</span><span class="sxs-lookup"><span data-stu-id="d18b3-115">Date that the administrator can next try to revoke licenses.</span></span> <span data-ttu-id="d18b3-116">Este parámetro solo contiene datos válidos cuando se ha producido un error en la llamada al método **REVOKE** porque se ha alcanzado el número máximo de revocación.</span><span class="sxs-lookup"><span data-stu-id="d18b3-116">This parameter only contains valid data when the **Revoke** method call has failed because the maximum revoke count has been reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d18b3-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d18b3-117">Remarks</span></span>

<span data-ttu-id="d18b3-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="d18b3-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d18b3-119">Solo se pueden revocar las cal por dispositivo de RDS.</span><span class="sxs-lookup"><span data-stu-id="d18b3-119">Only RDS Per Device CALs can be revoked.</span></span>

<span data-ttu-id="d18b3-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d18b3-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d18b3-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d18b3-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d18b3-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d18b3-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d18b3-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d18b3-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d18b3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d18b3-124">Requirements</span></span>



| <span data-ttu-id="d18b3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d18b3-125">Requirement</span></span> | <span data-ttu-id="d18b3-126">Value</span><span class="sxs-lookup"><span data-stu-id="d18b3-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18b3-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d18b3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d18b3-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d18b3-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d18b3-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d18b3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d18b3-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d18b3-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d18b3-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d18b3-131">Namespace</span></span><br/>                | <span data-ttu-id="d18b3-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d18b3-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d18b3-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d18b3-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d18b3-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d18b3-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d18b3-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d18b3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d18b3-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d18b3-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d18b3-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="d18b3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18b3-138">**Win32 \_ TSIssuedLicense**</span><span class="sxs-lookup"><span data-stu-id="d18b3-138">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> </dl>

 

