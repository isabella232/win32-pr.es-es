---
description: La \_ notificación SPFILENOTIFY TARGETEXISTS se envía a la rutina de devolución de llamada si el archivo que se va a copiar se puso en cola con la \_ marca NOOVERWRITE de la copia Sp \_ y ese archivo ya existe en el directorio de destino.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: Mensaje de SPFILENOTIFY_TARGETEXISTS (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423983"
---
# <a name="spfilenotify_targetexists-message"></a><span data-ttu-id="30eaa-103">SPFILENOTIFY \_ TARGETEXISTS</span><span class="sxs-lookup"><span data-stu-id="30eaa-103">SPFILENOTIFY\_TARGETEXISTS message</span></span>

<span data-ttu-id="30eaa-104">La notificación **SPFILENOTIFY \_ TARGETEXISTS** se envía a la rutina de devolución de llamada si el archivo que se va a copiar se puso en cola con la \_ marca NOOVERWRITE de la copia Sp \_ y ese archivo ya existe en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="30eaa-104">The **SPFILENOTIFY\_TARGETEXISTS** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NOOVERWRITE flag and that file already exists in the target directory.</span></span> <span data-ttu-id="30eaa-105">Se puede enviar a la rutina de devolución de llamada solo o combinarse mediante el operador OR, con las notificaciones de [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) y/o [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) .</span><span class="sxs-lookup"><span data-stu-id="30eaa-105">It can be sent to the callback routine alone or combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md) notifications.</span></span>


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="30eaa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30eaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30eaa-107">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="30eaa-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="30eaa-108">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contiene información sobre las rutas de acceso de los archivos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="30eaa-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="30eaa-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="30eaa-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="30eaa-110">Este parámetro no se usa a menos que se combine esta notificación, mediante el operador OR, con la notificación [**\_ LANGMISMATCH de SPFILENOTIFY**](spfilenotify-langmismatch.md) .</span><span class="sxs-lookup"><span data-stu-id="30eaa-110">This parameter is not used unless this notification is combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30eaa-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30eaa-111">Return value</span></span>

<span data-ttu-id="30eaa-112">La rutina de devolución de llamada debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="30eaa-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="30eaa-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="30eaa-113">Return code</span></span>                                                                          | <span data-ttu-id="30eaa-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="30eaa-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="30eaa-115"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="30eaa-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="30eaa-116">Sobrescriba el archivo en el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="30eaa-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="30eaa-117"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="30eaa-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="30eaa-118">Omitir la operación de copia actual.</span><span class="sxs-lookup"><span data-stu-id="30eaa-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="30eaa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30eaa-119">Requirements</span></span>



| <span data-ttu-id="30eaa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="30eaa-120">Requirement</span></span> | <span data-ttu-id="30eaa-121">Value</span><span class="sxs-lookup"><span data-stu-id="30eaa-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30eaa-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30eaa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="30eaa-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="30eaa-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="30eaa-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30eaa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="30eaa-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="30eaa-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30eaa-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30eaa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="30eaa-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="30eaa-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30eaa-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="30eaa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30eaa-129">Información general</span><span class="sxs-lookup"><span data-stu-id="30eaa-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="30eaa-130">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="30eaa-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="30eaa-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="30eaa-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="30eaa-132">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="30eaa-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="30eaa-133">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="30eaa-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="30eaa-134">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="30eaa-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="30eaa-135">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="30eaa-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="30eaa-136">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="30eaa-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




