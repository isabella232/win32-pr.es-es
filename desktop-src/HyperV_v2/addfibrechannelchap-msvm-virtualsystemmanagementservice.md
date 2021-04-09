---
description: Agrega parámetros DH-CHAP (Diffie Hellman-protocolo de autenticación de desafío mutuo) a un puerto de Canal de fibra sintético en una máquina virtual.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Método AddFibreChannelChap de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002020"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="480c5-103">Método AddFibreChannelChap de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="480c5-103">AddFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="480c5-104">Agrega parámetros DH-CHAP (Diffie Hellman-protocolo de autenticación de desafío mutuo) a un puerto de Canal de fibra sintético en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="480c5-104">Adds DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters to a synthetic Fibre Channel port on a virtual machine.</span></span> <span data-ttu-id="480c5-105">Este método producirá un error si la máquina virtual se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="480c5-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="480c5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="480c5-106">Syntax</span></span>


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a><span data-ttu-id="480c5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="480c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="480c5-108">*FcPortSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="480c5-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="480c5-109">Matriz de cadenas que contiene una instancia incrustada de la clase [**MSVM \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) que describe la configuración de los puertos canal de fibra sintéticos para las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="480c5-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that describes settings for synthetic Fibre Channel ports for virtual machines.</span></span> <span data-ttu-id="480c5-110">La propiedad **InstanceID** de cada una de estas instancias identifica los elementos que se van a modificar.</span><span class="sxs-lookup"><span data-stu-id="480c5-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="480c5-111">*SecretEncoding* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="480c5-111">*SecretEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="480c5-112">Especifica el tipo de codificación para el secreto compartido.</span><span class="sxs-lookup"><span data-stu-id="480c5-112">Specifies the type of encoding for the shared secret.</span></span>

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

<span data-ttu-id="480c5-113">**ASCII imprimible** (1)</span><span class="sxs-lookup"><span data-stu-id="480c5-113">**Printable ASCII** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="480c5-114">**Binario** (2)</span><span class="sxs-lookup"><span data-stu-id="480c5-114">**Binary** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="480c5-115">*SharedSecret* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="480c5-115">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="480c5-116">Especifica el secreto compartido.</span><span class="sxs-lookup"><span data-stu-id="480c5-116">Specifies the shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="480c5-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="480c5-117">Return value</span></span>

<span data-ttu-id="480c5-118">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="480c5-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="480c5-119">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="480c5-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="480c5-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="480c5-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="480c5-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="480c5-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="480c5-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="480c5-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="480c5-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="480c5-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="480c5-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="480c5-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="480c5-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="480c5-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="480c5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="480c5-131">Requirements</span></span>



| <span data-ttu-id="480c5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="480c5-132">Requirement</span></span> | <span data-ttu-id="480c5-133">Value</span><span class="sxs-lookup"><span data-stu-id="480c5-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="480c5-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="480c5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="480c5-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="480c5-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="480c5-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="480c5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="480c5-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="480c5-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="480c5-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="480c5-138">Namespace</span></span><br/>                | <span data-ttu-id="480c5-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="480c5-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="480c5-140">MOF</span><span class="sxs-lookup"><span data-stu-id="480c5-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="480c5-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="480c5-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="480c5-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="480c5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="480c5-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="480c5-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="480c5-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="480c5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="480c5-145">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="480c5-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




