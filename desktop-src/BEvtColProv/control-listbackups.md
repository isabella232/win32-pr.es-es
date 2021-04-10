---
description: Devuelve la lista de los archivos de configuración de copia de seguridad guardados que se pueden restaurar.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Método ListBackups de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152775"
---
# <a name="listbackups-method-of-the-control-class"></a><span data-ttu-id="313ce-103">Método ListBackups de la clase control</span><span class="sxs-lookup"><span data-stu-id="313ce-103">ListBackups method of the Control class</span></span>

<span data-ttu-id="313ce-104">Devuelve la lista de los archivos de configuración de copia de seguridad guardados que se pueden restaurar.</span><span class="sxs-lookup"><span data-stu-id="313ce-104">Returns the list of the saved backup configuration files that can be restored.</span></span>

## <a name="syntax"></a><span data-ttu-id="313ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="313ce-105">Syntax</span></span>


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a><span data-ttu-id="313ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="313ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313ce-107">*OriginalTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="313ce-107">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="313ce-108">La marca de tiempo de cuando se estableció la configuración actual (si se restaura a partir de una copia de seguridad, contendrá la marca de tiempo original).</span><span class="sxs-lookup"><span data-stu-id="313ce-108">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="313ce-109">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="313ce-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="313ce-110">*OriginalTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="313ce-110">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="313ce-111">La marca de tiempo de cuando se estableció la configuración actual (si se restaura a partir de una copia de seguridad, contendrá la marca de tiempo original).</span><span class="sxs-lookup"><span data-stu-id="313ce-111">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="313ce-112">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="313ce-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="313ce-113">*Archivos* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="313ce-113">*Files* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="313ce-114">La lista de archivos de copia de seguridad disponibles, en orden de la más reciente a la más antigua.</span><span class="sxs-lookup"><span data-stu-id="313ce-114">The list of available backup files, in order from the newest to the oldest.</span></span>

</dd> <dt>

<span data-ttu-id="313ce-115">*FilesTimestampLow* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="313ce-115">*FilesTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="313ce-116">Para cada archivo de copia de seguridad, la marca de tiempo de cuando se estableció su configuración.</span><span class="sxs-lookup"><span data-stu-id="313ce-116">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="313ce-117">Esta es la parte baja de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="313ce-117">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="313ce-118">*FilesTimestampHigh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="313ce-118">*FilesTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="313ce-119">Para cada archivo de copia de seguridad, la marca de tiempo de cuando se estableció su configuración.</span><span class="sxs-lookup"><span data-stu-id="313ce-119">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="313ce-120">Esta es la parte alta de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="313ce-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313ce-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="313ce-121">Return value</span></span>

<span data-ttu-id="313ce-122">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="313ce-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="313ce-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="313ce-123">Requirements</span></span>



| <span data-ttu-id="313ce-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="313ce-124">Requirement</span></span> | <span data-ttu-id="313ce-125">Value</span><span class="sxs-lookup"><span data-stu-id="313ce-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="313ce-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="313ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="313ce-127">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="313ce-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="313ce-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="313ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="313ce-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="313ce-129">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="313ce-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="313ce-130">Namespace</span></span><br/>                | <span data-ttu-id="313ce-131">Raíz de \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="313ce-131">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="313ce-132">MOF</span><span class="sxs-lookup"><span data-stu-id="313ce-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="313ce-133"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="313ce-133"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="313ce-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="313ce-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="313ce-135"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="313ce-135"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="313ce-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="313ce-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313ce-137">**Control**</span><span class="sxs-lookup"><span data-stu-id="313ce-137">**Control**</span></span>](control.md)
</dt> </dl>

 

