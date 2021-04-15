---
description: La notificación de LANGMISMATCH de SPFILENOTIFY \_ se envía a la rutina de devolución de llamada si el idioma del archivo que se va a copiar no coincide con el idioma de un archivo de destino existente.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: Mensaje de SPFILENOTIFY_LANGMISMATCH (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669716"
---
# <a name="spfilenotify_langmismatch-message"></a><span data-ttu-id="464e4-103">SPFILENOTIFY \_ LANGMISMATCH</span><span class="sxs-lookup"><span data-stu-id="464e4-103">SPFILENOTIFY\_LANGMISMATCH message</span></span>

<span data-ttu-id="464e4-104">La notificación de **\_ LANGMISMATCH de SPFILENOTIFY** se envía a la rutina de devolución de llamada si el idioma del archivo que se va a copiar no coincide con el idioma de un archivo de destino existente.</span><span class="sxs-lookup"><span data-stu-id="464e4-104">The **SPFILENOTIFY\_LANGMISMATCH** notification is sent to the callback routine if the language of the file to be copied does not match the language of an existing target file.</span></span> <span data-ttu-id="464e4-105">Se puede enviar a la rutina de devolución de llamada solo o combinarse mediante el operador OR, con [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) o [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md).</span><span class="sxs-lookup"><span data-stu-id="464e4-105">It can be sent to the callback routine alone or combined, by using the OR operator, with [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md).</span></span>


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="464e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="464e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="464e4-107">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="464e4-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="464e4-108">Puntero a una estructura [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contiene información sobre las rutas de acceso de los archivos de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="464e4-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths of the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="464e4-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="464e4-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="464e4-110">Identifica los idiomas no coincidentes.</span><span class="sxs-lookup"><span data-stu-id="464e4-110">Identifies the mismatched languages.</span></span> <span data-ttu-id="464e4-111">Este miembro tiene el identificador de idioma del archivo de código fuente en la palabra baja y el identificador de idioma del archivo de destino existente en la palabra alta.</span><span class="sxs-lookup"><span data-stu-id="464e4-111">This member has the language identifier of the source file in the low word, and the language identifier of the existing target file in the high word.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="464e4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="464e4-112">Return value</span></span>

<span data-ttu-id="464e4-113">La rutina de devolución de llamada debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="464e4-113">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="464e4-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="464e4-114">Return code</span></span>                                                                          | <span data-ttu-id="464e4-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="464e4-115">Description</span></span>                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="464e4-116"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="464e4-116"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="464e4-117">Copie el archivo y sobrescriba el archivo existente.</span><span class="sxs-lookup"><span data-stu-id="464e4-117">Copy the file and overwrite the existing file.</span></span><br/>               |
| <dl> <span data-ttu-id="464e4-118"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="464e4-118"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="464e4-119">Omitir la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="464e4-119">Skip the copy operation.</span></span> <span data-ttu-id="464e4-120">No sobrescriba el archivo existente.</span><span class="sxs-lookup"><span data-stu-id="464e4-120">Do not overwrite the existing file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="464e4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="464e4-121">Requirements</span></span>



| <span data-ttu-id="464e4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="464e4-122">Requirement</span></span> | <span data-ttu-id="464e4-123">Value</span><span class="sxs-lookup"><span data-stu-id="464e4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="464e4-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="464e4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="464e4-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="464e4-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="464e4-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="464e4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="464e4-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="464e4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="464e4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="464e4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="464e4-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="464e4-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="464e4-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="464e4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="464e4-131">Información general</span><span class="sxs-lookup"><span data-stu-id="464e4-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="464e4-132">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="464e4-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="464e4-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="464e4-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="464e4-134">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="464e4-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="464e4-135">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="464e4-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="464e4-136">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="464e4-136">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="464e4-137">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="464e4-137">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="464e4-138">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="464e4-138">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




