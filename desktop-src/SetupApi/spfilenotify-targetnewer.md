---
description: La notificación de TARGETNEWER de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada si el archivo que se va a copiar se ha puesto en cola con la copia de SP \_ \_ más reciente o se \_ \_ \_ han especificado las marcas más recientes en el directorio de destino.
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: Mensaje de SPFILENOTIFY_TARGETNEWER (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667657"
---
# <a name="spfilenotify_targetnewer-message"></a><span data-ttu-id="f3202-103">SPFILENOTIFY \_ TARGETNEWER</span><span class="sxs-lookup"><span data-stu-id="f3202-103">SPFILENOTIFY\_TARGETNEWER message</span></span>

<span data-ttu-id="f3202-104">La notificación de **\_ TARGETNEWER de SPFILENOTIFY** se envía a la rutina de devolución de llamada si el archivo que se va a copiar se ha puesto en cola con la copia de SP \_ \_ más reciente o se \_ \_ \_ han especificado las marcas más recientes en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="f3202-104">The **SPFILENOTIFY\_TARGETNEWER** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NEWER or SP\_COPY\_FORCE\_NEWER flags specified and a newer version of the file already exists in the target directory.</span></span> <span data-ttu-id="f3202-105">Se puede enviar a la rutina de devolución de llamada solo o a ORed junto con [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) o [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md).</span><span class="sxs-lookup"><span data-stu-id="f3202-105">It can be sent to the callback routine alone or ORed together with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md).</span></span>


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="f3202-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3202-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3202-107">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="f3202-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="f3202-108">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contiene información sobre las rutas de acceso de los archivos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="f3202-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="f3202-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="f3202-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="f3202-110">Este parámetro no se usa a menos que se combine esta notificación, mediante el operador OR, con [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md).</span><span class="sxs-lookup"><span data-stu-id="f3202-110">This parameter is not used unless this notification is combined, by using the OR operator, with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3202-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3202-111">Return value</span></span>

<span data-ttu-id="f3202-112">La rutina de devolución de llamada debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f3202-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="f3202-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f3202-113">Return code</span></span>                                                                          | <span data-ttu-id="f3202-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3202-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="f3202-115"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="f3202-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="f3202-116">Sobrescriba el archivo en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="f3202-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="f3202-117"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="f3202-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="f3202-118">Omitir la operación de copia actual.</span><span class="sxs-lookup"><span data-stu-id="f3202-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="f3202-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3202-119">Requirements</span></span>



| <span data-ttu-id="f3202-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3202-120">Requirement</span></span> | <span data-ttu-id="f3202-121">Value</span><span class="sxs-lookup"><span data-stu-id="f3202-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3202-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3202-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3202-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f3202-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f3202-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3202-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3202-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3202-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3202-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3202-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3202-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3202-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3202-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3202-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3202-129">Información general</span><span class="sxs-lookup"><span data-stu-id="f3202-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="f3202-130">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="f3202-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="f3202-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="f3202-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="f3202-132">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="f3202-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="f3202-133">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="f3202-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="f3202-134">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="f3202-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="f3202-135">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="f3202-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="f3202-136">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="f3202-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




