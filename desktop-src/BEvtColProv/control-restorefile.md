---
description: Restaure la configuración activa del recopilador a partir de un archivo de copia de seguridad.
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: Método RestoreFile de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFile
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 330486da86c9cac5c5f700d2aea91e0844fdca09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998083"
---
# <a name="restorefile-method-of-the-control-class"></a><span data-ttu-id="7d3ec-103">Método RestoreFile de la clase control</span><span class="sxs-lookup"><span data-stu-id="7d3ec-103">RestoreFile method of the Control class</span></span>

<span data-ttu-id="7d3ec-104">Restaure la configuración activa del recopilador a partir de un archivo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-104">Restore the active configuration of the collector from a backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d3ec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d3ec-105">Syntax</span></span>


```mof
Uint32 RestoreFile(
  [in]  string File,
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



## <a name="parameters"></a><span data-ttu-id="7d3ec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d3ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d3ec-107">*Archivo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-107">*File* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-108">Nombre del archivo de copia de seguridad que se va a restaurar, en la lista devuelta por ListBackups ().</span><span class="sxs-lookup"><span data-stu-id="7d3ec-108">Name of the backup file to restore, from the list returned by ListBackups().</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-109">*OldTimestampLow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-110">Marca de tiempo de cuando se estableció la configuración anterior.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="7d3ec-111">Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se ha cambiado entre).</span><span class="sxs-lookup"><span data-stu-id="7d3ec-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="7d3ec-112">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7d3ec-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-113">*OldTimestampHigh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-114">Marca de tiempo de cuando se estableció la configuración anterior.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="7d3ec-115">Si no es 0, habilita la comprobación de atomicidad: la nueva configuración solo se aplicará si la marca de tiempo de la configuración anterior coincide (es decir, la configuración no se ha cambiado entre).</span><span class="sxs-lookup"><span data-stu-id="7d3ec-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="7d3ec-116">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7d3ec-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-117">*NewTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-118">Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="7d3ec-119">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7d3ec-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-120">*NewTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-121">Marca de tiempo de cuando se estableció la nueva configuración, si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="7d3ec-122">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7d3ec-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-123">*OriginalTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-124">Marca de tiempo original de la primera vez que se estableció la configuración restaurada.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="7d3ec-125">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7d3ec-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-126">*OriginalTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-127">Marca de tiempo original de la primera vez que se estableció la configuración restaurada.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="7d3ec-128">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="7d3ec-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-129">*ErrorString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-130">Cadena de texto con la explicación del error.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-131">*WarningString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-132">Cadena de texto con advertencias.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-133">*InfoString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-134">Cadena de texto con información sobre la configuración.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-135">*ErrorType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-136">El tipo del error: tenga en cuenta que 0 o falta indican que el proceso se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-136">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="7d3ec-137">0</span><span class="sxs-lookup"><span data-stu-id="7d3ec-137">0</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-138">Correcto.</span><span class="sxs-lookup"><span data-stu-id="7d3ec-138">Success.</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-139">1</span><span class="sxs-lookup"><span data-stu-id="7d3ec-139">1</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-140">formato de argumento incorrecto</span><span class="sxs-lookup"><span data-stu-id="7d3ec-140">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-141">2</span><span class="sxs-lookup"><span data-stu-id="7d3ec-141">2</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-142">valor de argumento no válido</span><span class="sxs-lookup"><span data-stu-id="7d3ec-142">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-143">3</span><span class="sxs-lookup"><span data-stu-id="7d3ec-143">3</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-144">error de recurso abierto de recursos (socket)</span><span class="sxs-lookup"><span data-stu-id="7d3ec-144">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-145">4</span><span class="sxs-lookup"><span data-stu-id="7d3ec-145">4</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-146">error de persistencia (escritura de archivo)</span><span class="sxs-lookup"><span data-stu-id="7d3ec-146">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="7d3ec-147">5</span><span class="sxs-lookup"><span data-stu-id="7d3ec-147">5</span></span>
</dt> <dd>

<span data-ttu-id="7d3ec-148">error de atomicidad (la marca de tiempo anterior no coincidía)</span><span class="sxs-lookup"><span data-stu-id="7d3ec-148">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d3ec-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d3ec-149">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="7d3ec-150">0</span><span class="sxs-lookup"><span data-stu-id="7d3ec-150">0</span></span>

<span data-ttu-id="7d3ec-151">Error</span><span class="sxs-lookup"><span data-stu-id="7d3ec-151">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="7d3ec-152">1</span><span class="sxs-lookup"><span data-stu-id="7d3ec-152">1</span></span>

<span data-ttu-id="7d3ec-153">Correcto</span><span class="sxs-lookup"><span data-stu-id="7d3ec-153">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d3ec-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d3ec-154">Requirements</span></span>



| <span data-ttu-id="7d3ec-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d3ec-155">Requirement</span></span> | <span data-ttu-id="7d3ec-156">Value</span><span class="sxs-lookup"><span data-stu-id="7d3ec-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3ec-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d3ec-157">Minimum supported client</span></span><br/> | <span data-ttu-id="7d3ec-158">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d3ec-158">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7d3ec-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d3ec-159">Minimum supported server</span></span><br/> | <span data-ttu-id="7d3ec-160">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7d3ec-160">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="7d3ec-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7d3ec-161">Namespace</span></span><br/>                | <span data-ttu-id="7d3ec-162">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="7d3ec-162">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="7d3ec-163">MOF</span><span class="sxs-lookup"><span data-stu-id="7d3ec-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d3ec-164"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d3ec-164"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d3ec-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d3ec-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d3ec-166"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d3ec-166"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7d3ec-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d3ec-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d3ec-168">**Control**</span><span class="sxs-lookup"><span data-stu-id="7d3ec-168">**Control**</span></span>](control.md)
</dt> </dl>

 

