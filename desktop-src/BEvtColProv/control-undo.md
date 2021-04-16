---
description: Restaure la configuración activa del recopilador a partir del archivo de copia de seguridad anterior (determinado mediante el regreso de la marca de tiempo original actual).
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Método Undo de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 285f1ec39ea52f6c388e324f72745d72f65207e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659337"
---
# <a name="undo-method-of-the-control-class"></a><span data-ttu-id="060b1-103">Método Undo de la clase control</span><span class="sxs-lookup"><span data-stu-id="060b1-103">Undo method of the Control class</span></span>

<span data-ttu-id="060b1-104">Restaure la configuración activa del recopilador a partir del archivo de copia de seguridad anterior (determinado mediante el regreso de la marca de tiempo original actual).</span><span class="sxs-lookup"><span data-stu-id="060b1-104">Restore the active configuration of the collector from the previous backup file (determined by going back from the current original timestamp).</span></span> <span data-ttu-id="060b1-105">Si se ha establecido la configuración, significa deshacer ese cambio.</span><span class="sxs-lookup"><span data-stu-id="060b1-105">If the configuration has been just set, this means undoing that change.</span></span> <span data-ttu-id="060b1-106">Las llamadas consecutivas desharán a las configuraciones anteriores y anteriores.</span><span class="sxs-lookup"><span data-stu-id="060b1-106">The consecutive calls will undo to the earlier and earlier configurations.</span></span> <span data-ttu-id="060b1-107">Devuelve 1 si se realiza correctamente, 0 en caso de error.</span><span class="sxs-lookup"><span data-stu-id="060b1-107">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="060b1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="060b1-108">Syntax</span></span>


```mof
Uint32 Undo(
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



## <a name="parameters"></a><span data-ttu-id="060b1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="060b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="060b1-110">*OldTimestampLow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="060b1-110">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="060b1-111">Marca de tiempo de cuando se estableció la configuración anterior.</span><span class="sxs-lookup"><span data-stu-id="060b1-111">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="060b1-112">Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se ha cambiado entre).</span><span class="sxs-lookup"><span data-stu-id="060b1-112">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="060b1-113">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="060b1-113">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="060b1-114">*OldTimestampHigh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="060b1-114">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="060b1-115">Marca de tiempo de cuando se estableció la configuración anterior.</span><span class="sxs-lookup"><span data-stu-id="060b1-115">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="060b1-116">Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se ha cambiado entre).</span><span class="sxs-lookup"><span data-stu-id="060b1-116">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="060b1-117">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="060b1-117">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="060b1-118">*NewTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="060b1-118">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="060b1-119">Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="060b1-119">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="060b1-120">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="060b1-120">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="060b1-121">*NewTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="060b1-121">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="060b1-122">Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="060b1-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="060b1-123">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="060b1-123">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="060b1-124">*OriginalTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="060b1-124">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="060b1-125">Marca de tiempo original de la primera vez que se estableció la configuración restaurada.</span><span class="sxs-lookup"><span data-stu-id="060b1-125">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="060b1-126">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="060b1-126">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="060b1-127">*OriginalTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="060b1-127">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="060b1-128">Marca de tiempo original de la primera vez que se estableció la configuración restaurada.</span><span class="sxs-lookup"><span data-stu-id="060b1-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="060b1-129">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="060b1-129">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="060b1-130">*ErrorString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="060b1-130">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="060b1-131">Cadena de texto con la explicación del error.</span><span class="sxs-lookup"><span data-stu-id="060b1-131">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="060b1-132">*WarningString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="060b1-132">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="060b1-133">Cadena de texto con advertencias.</span><span class="sxs-lookup"><span data-stu-id="060b1-133">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="060b1-134">*InfoString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="060b1-134">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="060b1-135">Cadena de texto con información sobre la configuración.</span><span class="sxs-lookup"><span data-stu-id="060b1-135">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="060b1-136">*ErrorType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="060b1-136">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="060b1-137">El tipo del error: tenga en cuenta que 0 o falta indican que el proceso se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="060b1-137">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="060b1-138">0</span><span class="sxs-lookup"><span data-stu-id="060b1-138">0</span></span>
</dt> <dd>

<span data-ttu-id="060b1-139">Correcto.</span><span class="sxs-lookup"><span data-stu-id="060b1-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="060b1-140">1</span><span class="sxs-lookup"><span data-stu-id="060b1-140">1</span></span>
</dt> <dd>

<span data-ttu-id="060b1-141">formato de argumento incorrecto</span><span class="sxs-lookup"><span data-stu-id="060b1-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="060b1-142">2</span><span class="sxs-lookup"><span data-stu-id="060b1-142">2</span></span>
</dt> <dd>

<span data-ttu-id="060b1-143">valor de argumento no válido</span><span class="sxs-lookup"><span data-stu-id="060b1-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="060b1-144">3</span><span class="sxs-lookup"><span data-stu-id="060b1-144">3</span></span>
</dt> <dd>

<span data-ttu-id="060b1-145">error de recurso abierto de recursos (socket)</span><span class="sxs-lookup"><span data-stu-id="060b1-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="060b1-146">4</span><span class="sxs-lookup"><span data-stu-id="060b1-146">4</span></span>
</dt> <dd>

<span data-ttu-id="060b1-147">error de persistencia (escritura de archivo)</span><span class="sxs-lookup"><span data-stu-id="060b1-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="060b1-148">5</span><span class="sxs-lookup"><span data-stu-id="060b1-148">5</span></span>
</dt> <dd>

<span data-ttu-id="060b1-149">error de atomicidad (la marca de tiempo anterior no coincidía)</span><span class="sxs-lookup"><span data-stu-id="060b1-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="060b1-150">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="060b1-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="060b1-151">0</span><span class="sxs-lookup"><span data-stu-id="060b1-151">0</span></span>

<span data-ttu-id="060b1-152">Error</span><span class="sxs-lookup"><span data-stu-id="060b1-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="060b1-153">1</span><span class="sxs-lookup"><span data-stu-id="060b1-153">1</span></span>

<span data-ttu-id="060b1-154">Correcto</span><span class="sxs-lookup"><span data-stu-id="060b1-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="060b1-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="060b1-155">Requirements</span></span>



| <span data-ttu-id="060b1-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="060b1-156">Requirement</span></span> | <span data-ttu-id="060b1-157">Value</span><span class="sxs-lookup"><span data-stu-id="060b1-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="060b1-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="060b1-158">Minimum supported client</span></span><br/> | <span data-ttu-id="060b1-159">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="060b1-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="060b1-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="060b1-160">Minimum supported server</span></span><br/> | <span data-ttu-id="060b1-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="060b1-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="060b1-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="060b1-162">Namespace</span></span><br/>                | <span data-ttu-id="060b1-163">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="060b1-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="060b1-164">MOF</span><span class="sxs-lookup"><span data-stu-id="060b1-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="060b1-165"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="060b1-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="060b1-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="060b1-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="060b1-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="060b1-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="060b1-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="060b1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="060b1-169">**Control**</span><span class="sxs-lookup"><span data-stu-id="060b1-169">**Control**</span></span>](control.md)
</dt> </dl>

 

