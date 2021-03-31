---
description: Establezca la nueva configuración activa del recopilador.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Método SetConfiguration de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806986"
---
# <a name="setconfiguration-method-of-the-control-class"></a><span data-ttu-id="f6ac7-103">Método SetConfiguration de la clase control</span><span class="sxs-lookup"><span data-stu-id="f6ac7-103">SetConfiguration method of the Control class</span></span>

<span data-ttu-id="f6ac7-104">Establezca la nueva configuración activa del recopilador.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-104">Set the new active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6ac7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6ac7-105">Syntax</span></span>


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="f6ac7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6ac7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6ac7-107">*Configuración* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f6ac7-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-108">Configuración que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-108">The configuration to activate.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-109">*OldTimestampLow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6ac7-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-110">Bits de orden inferior de una marca de tiempo que indica cuándo se estableció la configuración activa actual.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-110">The low-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="f6ac7-111">La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-111">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-112">*OldTimestampHigh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6ac7-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-113">Bits de orden superior de una marca de tiempo que indica cuándo se estableció la configuración activa actual.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-113">The high-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="f6ac7-114">La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-114">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-115">*NewTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6ac7-115">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-116">Cuando este método finaliza, este parámetro contiene los bits de orden inferior de una marca de tiempo que indica cuándo se estableció la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-116">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="f6ac7-117">La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-117">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-118">*NewTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6ac7-118">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-119">Cuando este método finaliza, este parámetro contiene los bits de orden superior de la marca de tiempo que indica cuándo se estableció la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-119">When this method returns, this parameter contains the high-order bits of the timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="f6ac7-120">La comprobación de atomicidad está habilitada si esta propiedad no está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-120">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-121">*ErrorString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6ac7-121">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-122">Cuando este método devuelve un error, este parámetro contiene la descripción del error.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-122">When this method returns, if there was an error, this parameter contains the error description.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-123">*WarningString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6ac7-123">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-124">Cuando este método finaliza, este parámetro contiene cualquier mensaje de advertencia para la operación.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-124">When this method returns, this parameter contains any warnings messages for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-125">*InfoString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6ac7-125">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-126">Cuando este método finaliza, este parámetro contiene información para la nueva configuración activa.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-126">When this method returns, this parameter contains information for the new active configuration.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-127">*ErrorType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f6ac7-127">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-128">Cuando este método devuelve un error, este parámetro indica el tipo de error.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-128">When this method returns, if there was an error, this parameter indicates the error type.</span></span>

<dt>

<span data-ttu-id="f6ac7-129">0</span><span class="sxs-lookup"><span data-stu-id="f6ac7-129">0</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-130">Falta la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-130">The new configuration is missing.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-131">1</span><span class="sxs-lookup"><span data-stu-id="f6ac7-131">1</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-132">El formato de la nueva configuración no es válido.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-132">The format of the new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-133">2</span><span class="sxs-lookup"><span data-stu-id="f6ac7-133">2</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-134">La nueva configuración no es válida.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-134">The new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-135">3</span><span class="sxs-lookup"><span data-stu-id="f6ac7-135">3</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-136">Error producido por un socket abierto.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-136">There was an error caused by an open socket.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-137">4</span><span class="sxs-lookup"><span data-stu-id="f6ac7-137">4</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-138">Se produjo un error de escritura en el archivo.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-138">There was a file write error.</span></span>

</dd> <dt>

<span data-ttu-id="f6ac7-139">5</span><span class="sxs-lookup"><span data-stu-id="f6ac7-139">5</span></span>
</dt> <dd>

<span data-ttu-id="f6ac7-140">Se produjo un error de atomicidad.</span><span class="sxs-lookup"><span data-stu-id="f6ac7-140">There was an atomicity error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6ac7-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6ac7-141">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="f6ac7-142">0</span><span class="sxs-lookup"><span data-stu-id="f6ac7-142">0</span></span>

<span data-ttu-id="f6ac7-143">Error</span><span class="sxs-lookup"><span data-stu-id="f6ac7-143">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="f6ac7-144">1</span><span class="sxs-lookup"><span data-stu-id="f6ac7-144">1</span></span>

<span data-ttu-id="f6ac7-145">Correcto</span><span class="sxs-lookup"><span data-stu-id="f6ac7-145">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6ac7-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6ac7-146">Requirements</span></span>



| <span data-ttu-id="f6ac7-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6ac7-147">Requirement</span></span> | <span data-ttu-id="f6ac7-148">Value</span><span class="sxs-lookup"><span data-stu-id="f6ac7-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6ac7-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6ac7-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f6ac7-150">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6ac7-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f6ac7-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6ac7-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f6ac7-152">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f6ac7-152">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="f6ac7-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6ac7-153">Namespace</span></span><br/>                | <span data-ttu-id="f6ac7-154">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="f6ac7-154">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="f6ac7-155">MOF</span><span class="sxs-lookup"><span data-stu-id="f6ac7-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6ac7-156"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6ac7-156"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6ac7-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6ac7-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6ac7-158"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6ac7-158"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f6ac7-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6ac7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ac7-160">**Control**</span><span class="sxs-lookup"><span data-stu-id="f6ac7-160">**Control**</span></span>](control.md)
</dt> </dl>

 

 




