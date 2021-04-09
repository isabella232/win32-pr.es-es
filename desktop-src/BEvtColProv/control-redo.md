---
description: Restablezca la configuración activa del recopilador del archivo de copia de seguridad posterior (determinado por el avance desde la marca de tiempo original actual). Si se ha deshecho la configuración, significa que se rehace el cambio deshecho.
ms.assetid: bd153ea3-9148-4e65-a44e-3f9fa1855f2f
ms.tgt_platform: multiple
title: Método redo de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Redo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5ed77aac62dca0bf81ed13474e8acebb0235ea71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152774"
---
# <a name="redo-method-of-the-control-class"></a><span data-ttu-id="8483c-104">Método redo de la clase control</span><span class="sxs-lookup"><span data-stu-id="8483c-104">Redo method of the Control class</span></span>

<span data-ttu-id="8483c-105">Restablezca la configuración activa del recopilador del archivo de copia de seguridad posterior (determinado por el avance desde la marca de tiempo original actual).</span><span class="sxs-lookup"><span data-stu-id="8483c-105">Reset the active configuration of the collector from the later backup file (determined by going forward from the current original timestamp).</span></span> <span data-ttu-id="8483c-106">Si se ha deshecho la configuración, significa que se rehace el cambio deshecho.</span><span class="sxs-lookup"><span data-stu-id="8483c-106">If the configuration has been undone, this means redoing the undone change.</span></span>

## <a name="syntax"></a><span data-ttu-id="8483c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8483c-107">Syntax</span></span>


```mof
Uint32 Redo(
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



## <a name="parameters"></a><span data-ttu-id="8483c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8483c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8483c-109">*OldTimestampLow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8483c-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8483c-110">Marca de tiempo de cuando se estableció la configuración anterior.</span><span class="sxs-lookup"><span data-stu-id="8483c-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="8483c-111">Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se ha cambiado entre).</span><span class="sxs-lookup"><span data-stu-id="8483c-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="8483c-112">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8483c-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8483c-113">*OldTimestampHigh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8483c-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8483c-114">Marca de tiempo de cuando se estableció la configuración anterior.</span><span class="sxs-lookup"><span data-stu-id="8483c-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="8483c-115">Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se ha cambiado entre).</span><span class="sxs-lookup"><span data-stu-id="8483c-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="8483c-116">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8483c-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8483c-117">*NewTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8483c-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8483c-118">Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="8483c-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="8483c-119">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8483c-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8483c-120">*NewTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8483c-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8483c-121">Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="8483c-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="8483c-122">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8483c-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8483c-123">*OriginalTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8483c-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8483c-124">Marca de tiempo original de la primera vez que se estableció la configuración restaurada.</span><span class="sxs-lookup"><span data-stu-id="8483c-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="8483c-125">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8483c-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8483c-126">*OriginalTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8483c-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8483c-127">Marca de tiempo original de la primera vez que se estableció la configuración restaurada.</span><span class="sxs-lookup"><span data-stu-id="8483c-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="8483c-128">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="8483c-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="8483c-129">*ErrorString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8483c-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8483c-130">Cadena de texto con la explicación del error.</span><span class="sxs-lookup"><span data-stu-id="8483c-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="8483c-131">*WarningString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8483c-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8483c-132">Cadena de texto con advertencias.</span><span class="sxs-lookup"><span data-stu-id="8483c-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="8483c-133">*InfoString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8483c-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8483c-134">Cadena de texto con información sobre la configuración.</span><span class="sxs-lookup"><span data-stu-id="8483c-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="8483c-135">*ErrorType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8483c-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8483c-136">Tipo del error.</span><span class="sxs-lookup"><span data-stu-id="8483c-136">The type of the error.</span></span> <span data-ttu-id="8483c-137">Tenga en cuenta que 0 o falta indican que el proceso se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8483c-137">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="8483c-138">0</span><span class="sxs-lookup"><span data-stu-id="8483c-138">0</span></span>
</dt> <dd>

<span data-ttu-id="8483c-139">Correcto.</span><span class="sxs-lookup"><span data-stu-id="8483c-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="8483c-140">1</span><span class="sxs-lookup"><span data-stu-id="8483c-140">1</span></span>
</dt> <dd>

<span data-ttu-id="8483c-141">formato de argumento incorrecto</span><span class="sxs-lookup"><span data-stu-id="8483c-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="8483c-142">2</span><span class="sxs-lookup"><span data-stu-id="8483c-142">2</span></span>
</dt> <dd>

<span data-ttu-id="8483c-143">valor de argumento no válido</span><span class="sxs-lookup"><span data-stu-id="8483c-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="8483c-144">3</span><span class="sxs-lookup"><span data-stu-id="8483c-144">3</span></span>
</dt> <dd>

<span data-ttu-id="8483c-145">error de recurso abierto de recursos (socket)</span><span class="sxs-lookup"><span data-stu-id="8483c-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="8483c-146">4</span><span class="sxs-lookup"><span data-stu-id="8483c-146">4</span></span>
</dt> <dd>

<span data-ttu-id="8483c-147">error de persistencia (escritura de archivo)</span><span class="sxs-lookup"><span data-stu-id="8483c-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="8483c-148">5</span><span class="sxs-lookup"><span data-stu-id="8483c-148">5</span></span>
</dt> <dd>

<span data-ttu-id="8483c-149">error de atomicidad (la marca de tiempo anterior no coincidía)</span><span class="sxs-lookup"><span data-stu-id="8483c-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8483c-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8483c-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="8483c-151">0</span><span class="sxs-lookup"><span data-stu-id="8483c-151">0</span></span>

<span data-ttu-id="8483c-152">Error</span><span class="sxs-lookup"><span data-stu-id="8483c-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8483c-153">1</span><span class="sxs-lookup"><span data-stu-id="8483c-153">1</span></span>

<span data-ttu-id="8483c-154">Correcto</span><span class="sxs-lookup"><span data-stu-id="8483c-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8483c-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8483c-155">Requirements</span></span>



| <span data-ttu-id="8483c-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="8483c-156">Requirement</span></span> | <span data-ttu-id="8483c-157">Value</span><span class="sxs-lookup"><span data-stu-id="8483c-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8483c-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8483c-158">Minimum supported client</span></span><br/> | <span data-ttu-id="8483c-159">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="8483c-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8483c-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8483c-160">Minimum supported server</span></span><br/> | <span data-ttu-id="8483c-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8483c-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="8483c-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8483c-162">Namespace</span></span><br/>                | <span data-ttu-id="8483c-163">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="8483c-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="8483c-164">MOF</span><span class="sxs-lookup"><span data-stu-id="8483c-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8483c-165"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8483c-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="8483c-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8483c-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8483c-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8483c-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="8483c-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="8483c-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8483c-169">**Control**</span><span class="sxs-lookup"><span data-stu-id="8483c-169">**Control**</span></span>](control.md)
</dt> </dl>

 

