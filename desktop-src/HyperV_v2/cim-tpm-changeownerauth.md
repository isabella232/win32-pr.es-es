---
description: Cambia la credencial de autorización de propietario del dispositivo de TPM. Se requieren las contraseñas de autorización de propietario antiguas y nuevas.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Método ChangeOwnerAuth de la clase CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687350"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a><span data-ttu-id="4b5ec-104">Método ChangeOwnerAuth de la \_ clase TPM CIM</span><span class="sxs-lookup"><span data-stu-id="4b5ec-104">ChangeOwnerAuth method of the CIM\_TPM class</span></span>

<span data-ttu-id="4b5ec-105">Cambia la credencial de autorización de propietario del dispositivo de TPM.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-105">Changes the owner authorization credential of the TPM device.</span></span> <span data-ttu-id="4b5ec-106">Se requieren las contraseñas de autorización de propietario antiguas y nuevas.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-106">The old and new owner authorization passwords are required.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b5ec-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b5ec-107">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="4b5ec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b5ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b5ec-109">*OldOwnerAuth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b5ec-109">*OldOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b5ec-110">Representa la antigua credencial de autorización de propietario necesaria para tomar posesión del dispositivo de TPM. La subclase **CIM \_ SharedCredential** puede ser necesaria con un valor distinto de NULL de **la \_ SharedCredential CIM**.**Propiedad Secret** del parámetro.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-110">Represents the old owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4b5ec-111">*NewOwnerAuth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b5ec-111">*NewOwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b5ec-112">Representa la nueva credencial de autorización de propietario necesaria para tomar posesión del dispositivo de TPM. La subclase **CIM \_ SharedCredential** puede ser necesaria con un valor distinto de NULL de **la \_ SharedCredential CIM**.**Propiedad Secret** del parámetro.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-112">Represents the new owner authorization credential required to take ownership of the TPM device.The **CIM\_SharedCredential** subclass may be required with non-null value of the **CIM\_SharedCredential**.**Secret** property for the parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b5ec-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b5ec-113">Return value</span></span>

<span data-ttu-id="4b5ec-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4b5ec-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="4b5ec-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4b5ec-116">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="4b5ec-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4b5ec-117">**Error desconocido o no especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="4b5ec-117">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4b5ec-118">**DMTF reservado** (3.. 4095)</span><span class="sxs-lookup"><span data-stu-id="4b5ec-118">**DMTF Reserved** (3..4095)</span></span>
</dt> <dt>

<span data-ttu-id="4b5ec-119">**Método reservado** (4096.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4b5ec-119">**Method Reserved** (4096..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4b5ec-120">**Proveedor especificado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="4b5ec-120">**Vendor Specified** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4b5ec-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b5ec-121">Requirements</span></span>



| <span data-ttu-id="4b5ec-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b5ec-122">Requirement</span></span> | <span data-ttu-id="4b5ec-123">Value</span><span class="sxs-lookup"><span data-stu-id="4b5ec-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b5ec-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b5ec-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4b5ec-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b5ec-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4b5ec-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b5ec-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4b5ec-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4b5ec-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4b5ec-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4b5ec-128">Namespace</span></span><br/>                | <span data-ttu-id="4b5ec-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4b5ec-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4b5ec-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4b5ec-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b5ec-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b5ec-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b5ec-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b5ec-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b5ec-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b5ec-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b5ec-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b5ec-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b5ec-135">**TPM de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="4b5ec-135">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




