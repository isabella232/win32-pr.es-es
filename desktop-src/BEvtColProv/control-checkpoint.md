---
description: Si la configuración actual es el resultado de la operación de deshacer/rehacer/restaurar, la marca como si se hubiera establecido explícitamente, de modo que el historial conservará la hora en que se estableció y se creará un archivo de copia de seguridad en el siguiente cambio de configuración.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Método Checkpoint de la clase control (Srrestoreptapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 44453f647d55f29a9a6cfc5622e29dcc88ad2446
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152777"
---
# <a name="checkpoint-method-of-the-control-class"></a><span data-ttu-id="0a556-103">Método Checkpoint de la clase control</span><span class="sxs-lookup"><span data-stu-id="0a556-103">Checkpoint method of the Control class</span></span>

<span data-ttu-id="0a556-104">Si la configuración actual es el resultado de la operación de deshacer/rehacer/restaurar, la marca como si se hubiera establecido explícitamente, de modo que el historial conservará la hora en que se estableció y se creará un archivo de copia de seguridad en el siguiente cambio de configuración.</span><span class="sxs-lookup"><span data-stu-id="0a556-104">If the current configuration is a result of the Undo/Redo/Restore, marks it as if it has been set explicitly, so that the history will preserve the time when it was set, and a backup file will be created for it on the next configuration change.</span></span> <span data-ttu-id="0a556-105">Si la configuración actual ya estaba establecida explícitamente, no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="0a556-105">If the current configuration was already set explicitly, has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a556-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a556-106">Syntax</span></span>


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="0a556-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a556-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a556-108">*OldTimestampLow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a556-108">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a556-109">Marca de tiempo de cuando se estableció la configuración actual.</span><span class="sxs-lookup"><span data-stu-id="0a556-109">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="0a556-110">Si no es 0, habilita la comprobación de atomicidad: la acción se aplicará únicamente si la marca de tiempo de la configuración anterior coincide (es decir, si la configuración no se ha cambiado entre).</span><span class="sxs-lookup"><span data-stu-id="0a556-110">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="0a556-111">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0a556-111">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0a556-112">*OldTimestampHigh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a556-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a556-113">Marca de tiempo de cuando se estableció la configuración actual.</span><span class="sxs-lookup"><span data-stu-id="0a556-113">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="0a556-114">Si no es 0, habilita la comprobación de atomicidad: la acción se aplicará únicamente si la marca de tiempo de la configuración anterior coincide (es decir, si la configuración no se ha cambiado entre).</span><span class="sxs-lookup"><span data-stu-id="0a556-114">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="0a556-115">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="0a556-115">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="0a556-116">*ErrorString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a556-116">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a556-117">Cadena de texto con la explicación del error.</span><span class="sxs-lookup"><span data-stu-id="0a556-117">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="0a556-118">*WarningString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a556-118">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a556-119">Cadena de texto con advertencias.</span><span class="sxs-lookup"><span data-stu-id="0a556-119">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="0a556-120">*InfoString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a556-120">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a556-121">Cadena de texto con información sobre la configuración.</span><span class="sxs-lookup"><span data-stu-id="0a556-121">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="0a556-122">*ErrorType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a556-122">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a556-123">Tipo del error.</span><span class="sxs-lookup"><span data-stu-id="0a556-123">The type of the error.</span></span> <span data-ttu-id="0a556-124">Tenga en cuenta que 0 o falta indican que el proceso se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0a556-124">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="0a556-125">0</span><span class="sxs-lookup"><span data-stu-id="0a556-125">0</span></span>
</dt> <dd>

<span data-ttu-id="0a556-126">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0a556-126">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0a556-127">1</span><span class="sxs-lookup"><span data-stu-id="0a556-127">1</span></span>
</dt> <dd>

<span data-ttu-id="0a556-128">formato de argumento incorrecto</span><span class="sxs-lookup"><span data-stu-id="0a556-128">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="0a556-129">2</span><span class="sxs-lookup"><span data-stu-id="0a556-129">2</span></span>
</dt> <dd>

<span data-ttu-id="0a556-130">valor de argumento no válido</span><span class="sxs-lookup"><span data-stu-id="0a556-130">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="0a556-131">3</span><span class="sxs-lookup"><span data-stu-id="0a556-131">3</span></span>
</dt> <dd>

<span data-ttu-id="0a556-132">error de recurso abierto de recursos (socket)</span><span class="sxs-lookup"><span data-stu-id="0a556-132">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="0a556-133">4</span><span class="sxs-lookup"><span data-stu-id="0a556-133">4</span></span>
</dt> <dd>

<span data-ttu-id="0a556-134">error de persistencia (escritura de archivo)</span><span class="sxs-lookup"><span data-stu-id="0a556-134">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="0a556-135">5</span><span class="sxs-lookup"><span data-stu-id="0a556-135">5</span></span>
</dt> <dd>

<span data-ttu-id="0a556-136">error de atomicidad (la marca de tiempo anterior no coincidía)</span><span class="sxs-lookup"><span data-stu-id="0a556-136">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a556-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a556-137">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="0a556-138">0</span><span class="sxs-lookup"><span data-stu-id="0a556-138">0</span></span>

<span data-ttu-id="0a556-139">Error</span><span class="sxs-lookup"><span data-stu-id="0a556-139">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="0a556-140">1</span><span class="sxs-lookup"><span data-stu-id="0a556-140">1</span></span>

<span data-ttu-id="0a556-141">Correcto</span><span class="sxs-lookup"><span data-stu-id="0a556-141">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a556-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a556-142">Requirements</span></span>



| <span data-ttu-id="0a556-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a556-143">Requirement</span></span> | <span data-ttu-id="0a556-144">Value</span><span class="sxs-lookup"><span data-stu-id="0a556-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a556-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a556-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0a556-146">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a556-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0a556-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a556-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0a556-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0a556-148">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="0a556-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0a556-149">Namespace</span></span><br/>                | <span data-ttu-id="0a556-150">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="0a556-150">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="0a556-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a556-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a556-152"><dt>Srrestoreptapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a556-152"><dt>Srrestoreptapi.h</dt></span></span> </dl>          |
| <span data-ttu-id="0a556-153">MOF</span><span class="sxs-lookup"><span data-stu-id="0a556-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a556-154"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a556-154"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a556-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a556-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a556-156"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a556-156"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0a556-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a556-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a556-158">**Control**</span><span class="sxs-lookup"><span data-stu-id="0a556-158">**Control**</span></span>](control.md)
</dt> </dl>

 

