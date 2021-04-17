---
description: Protege la clave de cifrado del volumen mediante un identificador de seguridad Active Directory (SID).
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Método ProtectKeyWithAdSid de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688015"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d08b2-103">Método ProtectKeyWithAdSid de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="d08b2-103">ProtectKeyWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d08b2-104">El método **ProtectKeyWithAdSid** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) protege la clave de cifrado del volumen mediante el uso de un identificador de seguridad Active Directory (SID).</span><span class="sxs-lookup"><span data-stu-id="d08b2-104">The **ProtectKeyWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using a Active Directory security identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="d08b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d08b2-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="d08b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d08b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d08b2-107">*FriendlyName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d08b2-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d08b2-108">Cadena que especifica un identificador asignado por el usuario para este protector de clave.</span><span class="sxs-lookup"><span data-stu-id="d08b2-108">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="d08b2-109">Si no se especifica este parámetro, se utiliza un valor en blanco.</span><span class="sxs-lookup"><span data-stu-id="d08b2-109">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="d08b2-110">*SidString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d08b2-110">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08b2-111">Cadena que contiene la Active Directory SID usada para proteger la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="d08b2-111">String that contains the Active Directory SID used to protect the encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="d08b2-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="d08b2-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08b2-113">Marcas que cambian el comportamiento de la función.</span><span class="sxs-lookup"><span data-stu-id="d08b2-113">Flags that change the function behavior.</span></span> <span data-ttu-id="d08b2-114">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d08b2-114">This can be one of the following values.</span></span>



| <span data-ttu-id="d08b2-115">Value</span><span class="sxs-lookup"><span data-stu-id="d08b2-115">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="d08b2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d08b2-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="d08b2-117"><dt>**FVE \_ Marca de DPAPI \_ ng \_ \_ ninguno**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="d08b2-117"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="d08b2-118">Ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="d08b2-118">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="d08b2-119"><dt>**FVE \_ \_ \_ Desbloqueo de la marca de DPAPI ng \_ \_ como \_ \_ cuenta de servicio**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="d08b2-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="d08b2-120">Especifica que el protector basado en SID se protegió en una cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="d08b2-120">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="d08b2-121">Si se especifica esta marca, el llamador debe asegurarse de que se ejecuta como la cuenta de servicio adecuada antes de llamar a [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (por ejemplo, mediante la eliminación temporal de la suplantación).</span><span class="sxs-lookup"><span data-stu-id="d08b2-121">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d08b2-122">*VolumeKeyProtectorID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d08b2-122">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d08b2-123">Un identificador único asociado al protector creado.</span><span class="sxs-lookup"><span data-stu-id="d08b2-123">A unique identifier associated with the created protector.</span></span> <span data-ttu-id="d08b2-124">Puede usar esta cadena para administrar el protector de clave.</span><span class="sxs-lookup"><span data-stu-id="d08b2-124">You can use this string to manage the key protector.</span></span>

<span data-ttu-id="d08b2-125">Si la unidad admite el cifrado de hardware y BitLocker no ha tomado propiedad de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos de cada banda.</span><span class="sxs-lookup"><span data-stu-id="d08b2-125">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d08b2-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d08b2-126">Return value</span></span>

<span data-ttu-id="d08b2-127">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="d08b2-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d08b2-128">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d08b2-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="d08b2-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="d08b2-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d08b2-130"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="d08b2-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="d08b2-131">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d08b2-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d08b2-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d08b2-132">Remarks</span></span>

<span data-ttu-id="d08b2-133">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d08b2-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d08b2-134">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d08b2-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d08b2-135">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d08b2-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d08b2-136">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)</span><span class="sxs-lookup"><span data-stu-id="d08b2-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)</span></span>

<span data-ttu-id="d08b2-137">De forma predeterminada, no se puede Agregar una cuenta de Active Directory o un protector de grupo de forma remota.</span><span class="sxs-lookup"><span data-stu-id="d08b2-137">By default, you cannot add an Active Directory account or group protector remotely.</span></span> <span data-ttu-id="d08b2-138">Debe habilitar la delegación restringida en el controlador de dominio y el equipo de origen.</span><span class="sxs-lookup"><span data-stu-id="d08b2-138">You must enable constrained delegation on the domain controller and source computer.</span></span> <span data-ttu-id="d08b2-139">En el controlador de dominio, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d08b2-139">On the domain controller, perform the following steps:</span></span>

1.  <span data-ttu-id="d08b2-140">Abrir Administrador de servidores</span><span class="sxs-lookup"><span data-stu-id="d08b2-140">Open Server Manager</span></span>
2.  <span data-ttu-id="d08b2-141">Seleccionar equipos en roles de Active Directory</span><span class="sxs-lookup"><span data-stu-id="d08b2-141">Select Computers in Active Directory roles</span></span>
3.  <span data-ttu-id="d08b2-142">Seleccione el equipo cliente de destino y haga clic con el botón secundario en</span><span class="sxs-lookup"><span data-stu-id="d08b2-142">Select the target client computer and right click</span></span>
4.  <span data-ttu-id="d08b2-143">Seleccione la pestaña delegación</span><span class="sxs-lookup"><span data-stu-id="d08b2-143">Select the Delegation tab</span></span>
5.  <span data-ttu-id="d08b2-144">Seleccione el botón de radio "confiar en este equipo para la delegación solo a los servicios especificados"</span><span class="sxs-lookup"><span data-stu-id="d08b2-144">Select the "Trust this computer for delegation to specified services only" radio button</span></span>
6.  <span data-ttu-id="d08b2-145">Seleccione el botón de radio "usar solo Kerberos"</span><span class="sxs-lookup"><span data-stu-id="d08b2-145">Select the "Use Kerberos only" radio button</span></span>
7.  <span data-ttu-id="d08b2-146">Haga clic en Agregar</span><span class="sxs-lookup"><span data-stu-id="d08b2-146">Click Add</span></span>
8.  <span data-ttu-id="d08b2-147">Selección de "usuarios o equipos"</span><span class="sxs-lookup"><span data-stu-id="d08b2-147">Select "Users or Computers"</span></span>
9.  <span data-ttu-id="d08b2-148">Seleccionar host/como el nombre de entidad de seguridad de servicio</span><span class="sxs-lookup"><span data-stu-id="d08b2-148">Select host/ as the Service Principal Name</span></span>

<span data-ttu-id="d08b2-149">Realice los pasos del 3 al 9 en el equipo de origen.</span><span class="sxs-lookup"><span data-stu-id="d08b2-149">Perform steps 3 through 9 on the source computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d08b2-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d08b2-150">Requirements</span></span>



| <span data-ttu-id="d08b2-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="d08b2-151">Requirement</span></span> | <span data-ttu-id="d08b2-152">Value</span><span class="sxs-lookup"><span data-stu-id="d08b2-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d08b2-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d08b2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d08b2-154">Solo aplicaciones Windows 8 Enterprise, Windows 8 Pro \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="d08b2-154">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d08b2-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d08b2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d08b2-156">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d08b2-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d08b2-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d08b2-157">Namespace</span></span><br/>                | <span data-ttu-id="d08b2-158">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="d08b2-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d08b2-159">MOF</span><span class="sxs-lookup"><span data-stu-id="d08b2-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d08b2-160"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d08b2-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d08b2-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="d08b2-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08b2-162">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="d08b2-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
