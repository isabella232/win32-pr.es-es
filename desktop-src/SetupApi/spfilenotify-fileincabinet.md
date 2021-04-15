---
description: La \_ notificación SPFILENOTIFY FILEINCABINET se envía a una rutina de devolución de llamada por SetupIterateCabinet para cada archivo que se encuentra en el archivo. cab. La rutina de devolución de llamada debe devolver un valor que indica si se va a extraer el archivo.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: Mensaje de SPFILENOTIFY_FILEINCABINET (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669783"
---
# <a name="spfilenotify_fileincabinet-message"></a><span data-ttu-id="529f5-104">SPFILENOTIFY \_ FILEINCABINET</span><span class="sxs-lookup"><span data-stu-id="529f5-104">SPFILENOTIFY\_FILEINCABINET message</span></span>

<span data-ttu-id="529f5-105">La notificación **SPFILENOTIFY \_ FILEINCABINET** se envía a una rutina de devolución de llamada por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para cada archivo que se encuentra en el archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="529f5-105">The **SPFILENOTIFY\_FILEINCABINET** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) for each file found in the cabinet.</span></span> <span data-ttu-id="529f5-106">La rutina de devolución de llamada debe devolver un valor que indica si se va a extraer el archivo.</span><span class="sxs-lookup"><span data-stu-id="529f5-106">The callback routine must return a value indicating whether to extract the file.</span></span>


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a><span data-ttu-id="529f5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="529f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="529f5-108">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="529f5-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="529f5-109">Puntero a un [**archivo \_ en la estructura de \_ \_ información de contenedor**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) que contiene información sobre el archivo en el archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="529f5-109">Pointer to a [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure that contains information about the file in the cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="529f5-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="529f5-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="529f5-111">Puntero a una cadena terminada en null que contiene el nombre de archivo del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="529f5-111">Pointer to a null-terminated string that contains the filename of the cabinet file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="529f5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="529f5-112">Return value</span></span>

<span data-ttu-id="529f5-113">La rutina de devolución de llamada debe devolver uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="529f5-113">Your callback routine should return one of the following.</span></span>



| <span data-ttu-id="529f5-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="529f5-114">Return code</span></span>                                                                                 | <span data-ttu-id="529f5-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="529f5-115">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="529f5-116"><dt>**FILEOP \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="529f5-116"><dt>**FILEOP\_SKIP**</dt></span></span> </dl> | <span data-ttu-id="529f5-117">No extraiga el archivo, omítalo.</span><span class="sxs-lookup"><span data-stu-id="529f5-117">Do not extract the file, skip it.</span></span><br/> |
| <dl> <span data-ttu-id="529f5-118"><dt>**FILEOP \_ Doit**</dt></span><span class="sxs-lookup"><span data-stu-id="529f5-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl> | <span data-ttu-id="529f5-119">Extrae el archivo.</span><span class="sxs-lookup"><span data-stu-id="529f5-119">Extract the file.</span></span><br/>                 |



 

<span data-ttu-id="529f5-120">Si la rutina de devolución de llamada devuelve FILEOP \_ doit, el nombre que se va a usar para el archivo extraído debe especificarse en el miembro **FullTargetName** del [**archivo en la estructura \_ de \_ \_ información de contenedor**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) pasada a la rutina en *parám1*.</span><span class="sxs-lookup"><span data-stu-id="529f5-120">If your callback routine returns FILEOP\_DOIT, the name to use for the extracted file should be specified in the **FullTargetName** member of the [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure passed to the routine in *Param1*.</span></span>

> [!Note]  
> <span data-ttu-id="529f5-121">No hay ninguna rutina de devolución de llamada del archivo. cab predeterminada.</span><span class="sxs-lookup"><span data-stu-id="529f5-121">There is no default cabinet callback routine.</span></span> <span data-ttu-id="529f5-122">La aplicación de instalación debe proporcionar una rutina de devolución de llamada para controlar las notificaciones enviadas por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="529f5-122">The setup application should supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="529f5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="529f5-123">Requirements</span></span>



| <span data-ttu-id="529f5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="529f5-124">Requirement</span></span> | <span data-ttu-id="529f5-125">Value</span><span class="sxs-lookup"><span data-stu-id="529f5-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="529f5-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="529f5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="529f5-127">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="529f5-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="529f5-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="529f5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="529f5-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="529f5-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="529f5-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="529f5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="529f5-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="529f5-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="529f5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="529f5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="529f5-133">Información general</span><span class="sxs-lookup"><span data-stu-id="529f5-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="529f5-134">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="529f5-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="529f5-135">**ARCHIVO \_ en \_ información de contenedor \_**</span><span class="sxs-lookup"><span data-stu-id="529f5-135">**FILE\_IN\_CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="529f5-136">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="529f5-136">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




