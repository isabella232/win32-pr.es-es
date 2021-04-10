---
description: Validar un texto de configuración para comprobar su exactitud sin establecerlo activo. Devuelve 1 si se realiza correctamente, 0 en caso de error.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Método ValidateConfiguration de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998081"
---
# <a name="validateconfiguration-method-of-the-control-class"></a><span data-ttu-id="11cf5-104">Método ValidateConfiguration de la clase control</span><span class="sxs-lookup"><span data-stu-id="11cf5-104">ValidateConfiguration method of the Control class</span></span>

<span data-ttu-id="11cf5-105">Validar un texto de configuración para comprobar su exactitud sin establecerlo activo.</span><span class="sxs-lookup"><span data-stu-id="11cf5-105">Validate a configuration text for correctness without setting it active.</span></span> <span data-ttu-id="11cf5-106">Devuelve 1 si se realiza correctamente, 0 en caso de error.</span><span class="sxs-lookup"><span data-stu-id="11cf5-106">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="11cf5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11cf5-107">Syntax</span></span>


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="11cf5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11cf5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11cf5-109">*Configuración* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="11cf5-109">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11cf5-110">Configuración que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="11cf5-110">The configuration to check.</span></span>

</dd> <dt>

<span data-ttu-id="11cf5-111">*ErrorString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="11cf5-111">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11cf5-112">Cuando este método devuelve un error, este parámetro contiene una descripción del error de validación de la operación.</span><span class="sxs-lookup"><span data-stu-id="11cf5-112">When this method returns, if there was a error, this parameter contains a description of the validation error for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="11cf5-113">*WarningString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="11cf5-113">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11cf5-114">Cuando este método finaliza, este parámetro contiene una descripción de las advertencias de validación para la operación.</span><span class="sxs-lookup"><span data-stu-id="11cf5-114">When this method returns, this parameter contains a description of any validation warnings for the operation.</span></span>

<span data-ttu-id="11cf5-115">Cadena de texto con advertencias.</span><span class="sxs-lookup"><span data-stu-id="11cf5-115">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="11cf5-116">*InfoString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="11cf5-116">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11cf5-117">Cuando este método finaliza, este parámetro contiene un conjunto de información sobre la configuración.</span><span class="sxs-lookup"><span data-stu-id="11cf5-117">When this method returns, this parameter contains a set of information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="11cf5-118">*ErrorType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="11cf5-118">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11cf5-119">Cuando este método finaliza, si se produjo un error de validación, este parámetro indica el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="11cf5-119">When this method returns, if there was a validation error, this parameter indicates the error type.</span></span>

<span data-ttu-id="11cf5-120">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="11cf5-120">The possible values are:</span></span>

<dt>

<span data-ttu-id="11cf5-121">0</span><span class="sxs-lookup"><span data-stu-id="11cf5-121">0</span></span>
</dt> <dd>

<span data-ttu-id="11cf5-122">Falta el argumento.</span><span class="sxs-lookup"><span data-stu-id="11cf5-122">The argument is missing.</span></span>

</dd> <dt>

<span data-ttu-id="11cf5-123">1</span><span class="sxs-lookup"><span data-stu-id="11cf5-123">1</span></span>
</dt> <dd>

<span data-ttu-id="11cf5-124">El formato del argumento no es válido.</span><span class="sxs-lookup"><span data-stu-id="11cf5-124">The argument format is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="11cf5-125">2</span><span class="sxs-lookup"><span data-stu-id="11cf5-125">2</span></span>
</dt> <dd>

<span data-ttu-id="11cf5-126">Un argumento de configuración no es válido.</span><span class="sxs-lookup"><span data-stu-id="11cf5-126">A configuration argument is invalid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11cf5-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11cf5-127">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="11cf5-128">0</span><span class="sxs-lookup"><span data-stu-id="11cf5-128">0</span></span>

<span data-ttu-id="11cf5-129">Error</span><span class="sxs-lookup"><span data-stu-id="11cf5-129">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="11cf5-130">1</span><span class="sxs-lookup"><span data-stu-id="11cf5-130">1</span></span>

<span data-ttu-id="11cf5-131">Correcto</span><span class="sxs-lookup"><span data-stu-id="11cf5-131">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11cf5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11cf5-132">Requirements</span></span>



| <span data-ttu-id="11cf5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="11cf5-133">Requirement</span></span> | <span data-ttu-id="11cf5-134">Value</span><span class="sxs-lookup"><span data-stu-id="11cf5-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11cf5-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11cf5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="11cf5-136">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="11cf5-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="11cf5-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11cf5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="11cf5-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="11cf5-138">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="11cf5-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="11cf5-139">Namespace</span></span><br/>                | <span data-ttu-id="11cf5-140">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="11cf5-140">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="11cf5-141">MOF</span><span class="sxs-lookup"><span data-stu-id="11cf5-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11cf5-142"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11cf5-142"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="11cf5-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11cf5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11cf5-144"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="11cf5-144"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="11cf5-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="11cf5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11cf5-146">**Control**</span><span class="sxs-lookup"><span data-stu-id="11cf5-146">**Control**</span></span>](control.md)
</dt> </dl>

 

 




