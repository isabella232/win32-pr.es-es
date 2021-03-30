---
description: La \_ notificación SPFILENOTIFY QUEUESCAN \_ SIGNERINFO se envía a una rutina de devolución de llamada por SetupScanFileQueue para cada nodo de la subcola de copia de la cola de archivos.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: Mensaje de SPFILENOTIFY_QUEUESCAN_SIGNERINFO (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002326"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a><span data-ttu-id="efc5c-103">SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO</span><span class="sxs-lookup"><span data-stu-id="efc5c-103">SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO message</span></span>

<span data-ttu-id="efc5c-104">La notificación **SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO** se envía a una rutina de devolución de llamada por [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) para cada nodo de la subcola de copia de la cola de archivos.</span><span class="sxs-lookup"><span data-stu-id="efc5c-104">The **SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="efc5c-105">Esto solo se produce si se llamó a la función **SetupScanFileQueue** especificando la marca SPQ \_ scan \_ use \_ callback \_ SIGNERINFO.</span><span class="sxs-lookup"><span data-stu-id="efc5c-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK\_SIGNERINFO.</span></span> <span data-ttu-id="efc5c-106">Disponible a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="efc5c-106">Available starting with Windows XP.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="efc5c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="efc5c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc5c-108">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="efc5c-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="efc5c-109">Puntero a una estructura de [**\_ SIGNERINFO de FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) .</span><span class="sxs-lookup"><span data-stu-id="efc5c-109">Pointer to a [**FILEPATHS\_SIGNERINFO**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) structure.</span></span> <span data-ttu-id="efc5c-110">El miembro de **destino** es el nombre de archivo del archivo de destino en el sistema.</span><span class="sxs-lookup"><span data-stu-id="efc5c-110">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="efc5c-111">El miembro de **origen** es la ruta de acceso esperada del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="efc5c-111">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="efc5c-112">El miembro **Win32Error** es el error de firma.</span><span class="sxs-lookup"><span data-stu-id="efc5c-112">The **Win32Error** member is the signing error.</span></span> <span data-ttu-id="efc5c-113">Se devuelve la información de la firma si la rutina de devolución de llamada devuelve **Win32Error**= = no hay ningún \_ error.</span><span class="sxs-lookup"><span data-stu-id="efc5c-113">Signature information is returned if the callback routine returns **Win32Error**==NO\_ERROR.</span></span> <span data-ttu-id="efc5c-114">El miembro **DigitalSigner** es el firmante digital.</span><span class="sxs-lookup"><span data-stu-id="efc5c-114">The **DigitalSigner** member is the digital signer.</span></span> <span data-ttu-id="efc5c-115">El miembro **version** es la versión.</span><span class="sxs-lookup"><span data-stu-id="efc5c-115">The **Version** member is the version.</span></span> <span data-ttu-id="efc5c-116">**CatalogFile** es el archivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="efc5c-116">The **CatalogFile** is the catalog file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc5c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="efc5c-117">Return value</span></span>

<span data-ttu-id="efc5c-118">La rutina de devolución de llamada debe devolver un [código de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="efc5c-118">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="efc5c-119">Si la rutina de devolución de llamada NO devuelve ningún \_ error, el análisis de cola continúa y devuelve si la rutina devuelve cualquier otro código de error, el análisis de cola se anula y [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="efc5c-119">If the callback routine returns NO\_ERROR, the queue scan continues, and returns If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="efc5c-120">La función [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) no controla esta notificación.</span><span class="sxs-lookup"><span data-stu-id="efc5c-120">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="efc5c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efc5c-121">Requirements</span></span>



| <span data-ttu-id="efc5c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="efc5c-122">Requirement</span></span> | <span data-ttu-id="efc5c-123">Value</span><span class="sxs-lookup"><span data-stu-id="efc5c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efc5c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efc5c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="efc5c-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="efc5c-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="efc5c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efc5c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="efc5c-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="efc5c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="efc5c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efc5c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="efc5c-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="efc5c-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efc5c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="efc5c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc5c-131">Información general</span><span class="sxs-lookup"><span data-stu-id="efc5c-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="efc5c-132">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="efc5c-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="efc5c-133">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="efc5c-133">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

