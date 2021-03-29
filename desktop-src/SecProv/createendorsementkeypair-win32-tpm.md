---
description: Crea un par de claves de aprobación de 2048 bits en el TPM.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Método CreateEndorsementKeyPair de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540947"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a><span data-ttu-id="700b0-103">Método CreateEndorsementKeyPair de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="700b0-103">CreateEndorsementKeyPair method of the Win32\_Tpm class</span></span>

<span data-ttu-id="700b0-104">El método **CreateEndorsementKeyPair** de la clase [**Win32 \_ TPM**](win32-tpm.md) crea un par de claves de aprobación de 2048 bits en el TPM.</span><span class="sxs-lookup"><span data-stu-id="700b0-104">The **CreateEndorsementKeyPair** method of the [**Win32\_Tpm**](win32-tpm.md) class creates an 2048-bit endorsement key pair on the TPM.</span></span> <span data-ttu-id="700b0-105">El par de claves de aprobación debe estar disponible para que el método [**TakeOwnerShip**](takeownership-win32-tpm.md) se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="700b0-105">The endorsement key pair must be available for the [**TakeOwnership**](takeownership-win32-tpm.md) method to run successfully.</span></span> <span data-ttu-id="700b0-106">Puede usar el método [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) para detectar si la clave de aprobación ya existe en el TPM.</span><span class="sxs-lookup"><span data-stu-id="700b0-106">You can use the [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) method to detect whether the endorsement key already exists on the TPM.</span></span>

## <a name="syntax"></a><span data-ttu-id="700b0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="700b0-107">Syntax</span></span>


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a><span data-ttu-id="700b0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="700b0-108">Parameters</span></span>

<span data-ttu-id="700b0-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="700b0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="700b0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="700b0-110">Return value</span></span>

<span data-ttu-id="700b0-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="700b0-111">Type: **uint32**</span></span>

<span data-ttu-id="700b0-112">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="700b0-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="700b0-113">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="700b0-113">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="700b0-114">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="700b0-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="700b0-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="700b0-115">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="700b0-116"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="700b0-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="700b0-117">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="700b0-117">The method was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="700b0-118"><dt> **TPM \_ E \_ deshabilitado \_ cmd**</dt> <dt>2150105096 (0x80280008)</dt></span><span class="sxs-lookup"><span data-stu-id="700b0-118"><dt>**TPM\_E\_DISABLED\_CMD** </dt> <dt>2150105096 (0x80280008)</dt></span></span> </dl> | <span data-ttu-id="700b0-119">Ya existe un par de claves de aprobación en este TPM.</span><span class="sxs-lookup"><span data-stu-id="700b0-119">An endorsement key pair already exists on this TPM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="700b0-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="700b0-120">Remarks</span></span>

<span data-ttu-id="700b0-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="700b0-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="700b0-122">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="700b0-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="700b0-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="700b0-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="700b0-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="700b0-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="700b0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="700b0-125">Requirements</span></span>



| <span data-ttu-id="700b0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="700b0-126">Requirement</span></span> | <span data-ttu-id="700b0-127">Value</span><span class="sxs-lookup"><span data-stu-id="700b0-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="700b0-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="700b0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="700b0-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="700b0-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="700b0-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="700b0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="700b0-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="700b0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="700b0-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="700b0-132">Namespace</span></span><br/>                | <span data-ttu-id="700b0-133">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="700b0-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="700b0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="700b0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="700b0-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="700b0-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="700b0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="700b0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="700b0-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="700b0-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="700b0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="700b0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700b0-139">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="700b0-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
