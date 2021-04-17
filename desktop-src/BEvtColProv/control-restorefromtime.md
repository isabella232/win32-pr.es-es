---
description: Restaure la configuración activa del recopilador a partir de un archivo de copia de seguridad, seleccionado por una marca de tiempo.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Método RestoreFromTime de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652351"
---
# <a name="restorefromtime-method-of-the-control-class"></a><span data-ttu-id="60793-103">Método RestoreFromTime de la clase control</span><span class="sxs-lookup"><span data-stu-id="60793-103">RestoreFromTime method of the Control class</span></span>

<span data-ttu-id="60793-104">Restaure la configuración activa del recopilador a partir de un archivo de copia de seguridad, seleccionado por una marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="60793-104">Restore the active configuration of the collector from a backup file, selected by a timestamp.</span></span>

## <a name="syntax"></a><span data-ttu-id="60793-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60793-105">Syntax</span></span>


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="60793-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60793-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60793-107">*TargetTimestampLow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60793-107">*TargetTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-108">Restaure al archivo de copia de seguridad en esta marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="60793-108">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="60793-109">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="60793-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="60793-110">*TargetTimestampHigh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60793-110">*TargetTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-111">Restaure al archivo de copia de seguridad en esta marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="60793-111">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="60793-112">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="60793-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="60793-113">*OldTimestampLow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60793-113">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-114">Marca de tiempo de cuando se estableció la configuración anterior.</span><span class="sxs-lookup"><span data-stu-id="60793-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="60793-115">Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se ha cambiado entre).</span><span class="sxs-lookup"><span data-stu-id="60793-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="60793-116">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="60793-116">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="60793-117">*OldTimestampHigh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="60793-117">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-118">Marca de tiempo de cuando se estableció la configuración anterior.</span><span class="sxs-lookup"><span data-stu-id="60793-118">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="60793-119">Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se ha cambiado entre).</span><span class="sxs-lookup"><span data-stu-id="60793-119">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="60793-120">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="60793-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="60793-121">*NewTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60793-121">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-122">Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="60793-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="60793-123">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="60793-123">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="60793-124">*NewTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60793-124">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-125">Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="60793-125">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="60793-126">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="60793-126">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="60793-127">*OriginalTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60793-127">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-128">Marca de tiempo original de la primera vez que se estableció la configuración restaurada.</span><span class="sxs-lookup"><span data-stu-id="60793-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="60793-129">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="60793-129">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="60793-130">*OriginalTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60793-130">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-131">Marca de tiempo original de la primera vez que se estableció la configuración restaurada.</span><span class="sxs-lookup"><span data-stu-id="60793-131">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="60793-132">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="60793-132">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="60793-133">*ErrorString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60793-133">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-134">Cadena de texto con la explicación del error.</span><span class="sxs-lookup"><span data-stu-id="60793-134">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="60793-135">*WarningString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60793-135">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-136">Cadena de texto con advertencias.</span><span class="sxs-lookup"><span data-stu-id="60793-136">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="60793-137">*InfoString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60793-137">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-138">Cadena de texto con información sobre la configuración.</span><span class="sxs-lookup"><span data-stu-id="60793-138">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="60793-139">*ErrorType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60793-139">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60793-140">El tipo del error: tenga en cuenta que 0 o falta indican que el proceso se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="60793-140">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="60793-141">0</span><span class="sxs-lookup"><span data-stu-id="60793-141">0</span></span>
</dt> <dd>

<span data-ttu-id="60793-142">Correcto.</span><span class="sxs-lookup"><span data-stu-id="60793-142">Success.</span></span>

</dd> <dt>

<span data-ttu-id="60793-143">1</span><span class="sxs-lookup"><span data-stu-id="60793-143">1</span></span>
</dt> <dd>

<span data-ttu-id="60793-144">formato de argumento incorrecto</span><span class="sxs-lookup"><span data-stu-id="60793-144">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="60793-145">2</span><span class="sxs-lookup"><span data-stu-id="60793-145">2</span></span>
</dt> <dd>

<span data-ttu-id="60793-146">valor de argumento no válido</span><span class="sxs-lookup"><span data-stu-id="60793-146">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="60793-147">3</span><span class="sxs-lookup"><span data-stu-id="60793-147">3</span></span>
</dt> <dd>

<span data-ttu-id="60793-148">error de recurso abierto de recursos (socket)</span><span class="sxs-lookup"><span data-stu-id="60793-148">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="60793-149">4</span><span class="sxs-lookup"><span data-stu-id="60793-149">4</span></span>
</dt> <dd>

<span data-ttu-id="60793-150">error de persistencia (escritura de archivo)</span><span class="sxs-lookup"><span data-stu-id="60793-150">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="60793-151">5</span><span class="sxs-lookup"><span data-stu-id="60793-151">5</span></span>
</dt> <dd>

<span data-ttu-id="60793-152">error de atomicidad (la marca de tiempo anterior no coincidía)</span><span class="sxs-lookup"><span data-stu-id="60793-152">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60793-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60793-153">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="60793-154">0</span><span class="sxs-lookup"><span data-stu-id="60793-154">0</span></span>

<span data-ttu-id="60793-155">Error</span><span class="sxs-lookup"><span data-stu-id="60793-155">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="60793-156">1</span><span class="sxs-lookup"><span data-stu-id="60793-156">1</span></span>

<span data-ttu-id="60793-157">Correcto</span><span class="sxs-lookup"><span data-stu-id="60793-157">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60793-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60793-158">Requirements</span></span>



| <span data-ttu-id="60793-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="60793-159">Requirement</span></span> | <span data-ttu-id="60793-160">Value</span><span class="sxs-lookup"><span data-stu-id="60793-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60793-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60793-161">Minimum supported client</span></span><br/> | <span data-ttu-id="60793-162">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="60793-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="60793-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60793-163">Minimum supported server</span></span><br/> | <span data-ttu-id="60793-164">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60793-164">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="60793-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60793-165">Namespace</span></span><br/>                | <span data-ttu-id="60793-166">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="60793-166">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="60793-167">MOF</span><span class="sxs-lookup"><span data-stu-id="60793-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60793-168"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60793-168"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="60793-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60793-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60793-170"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60793-170"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="60793-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="60793-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60793-172">**Control**</span><span class="sxs-lookup"><span data-stu-id="60793-172">**Control**</span></span>](control.md)
</dt> </dl>

 

