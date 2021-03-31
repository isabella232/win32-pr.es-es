---
description: La notificación de NEEDNEWCABINET de SPFILENOTIFY \_ se envía mediante SetupIterateCabinet para indicar que el archivo actual continúa en otro contenedor.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: Mensaje de SPFILENOTIFY_NEEDNEWCABINET (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278981"
---
# <a name="spfilenotify_neednewcabinet-message"></a><span data-ttu-id="68ff4-103">SPFILENOTIFY \_ NEEDNEWCABINET</span><span class="sxs-lookup"><span data-stu-id="68ff4-103">SPFILENOTIFY\_NEEDNEWCABINET message</span></span>

<span data-ttu-id="68ff4-104">La notificación de **\_ NEEDNEWCABINET de SPFILENOTIFY** se envía mediante [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) para indicar que el archivo actual continúa en otro contenedor.</span><span class="sxs-lookup"><span data-stu-id="68ff4-104">The **SPFILENOTIFY\_NEEDNEWCABINET** notification is sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate that the current file continues in another cabinet.</span></span> <span data-ttu-id="68ff4-105">A continuación, la rutina de devolución de llamada puede llamar a [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)o crear su propio cuadro de diálogo para solicitar al usuario que inserte el siguiente disco.</span><span class="sxs-lookup"><span data-stu-id="68ff4-105">Your callback routine can then call [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), or create its own dialog box to prompt the user to insert the next disk.</span></span>


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a><span data-ttu-id="68ff4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68ff4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68ff4-107">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="68ff4-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="68ff4-108">Puntero a una estructura de [**\_ información**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) del archivo. cab que contiene información sobre el contenedor y el archivo que se va a extraer.</span><span class="sxs-lookup"><span data-stu-id="68ff4-108">Pointer to a [**CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) structure that contains information about the cabinet and the file to be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="68ff4-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="68ff4-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="68ff4-110">Si la devolución de llamada NO devuelve ningún \_ error, este parámetro es un puntero a una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="68ff4-110">If the callback returns NO\_ERROR, this parameter is a pointer to a null-terminated string.</span></span> <span data-ttu-id="68ff4-111">Si la cadena no está vacía, especifica una nueva ruta de acceso al archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="68ff4-111">If the string is not empty, it specifies a new path to the cabinet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68ff4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68ff4-112">Return value</span></span>

<span data-ttu-id="68ff4-113">La rutina debe devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="68ff4-113">Your routine should return one of the following values.</span></span>



| <span data-ttu-id="68ff4-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="68ff4-114">Return code</span></span>                                                                                 | <span data-ttu-id="68ff4-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="68ff4-115">Description</span></span>                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68ff4-116"><dt>**SIN \_ errores**</dt></span><span class="sxs-lookup"><span data-stu-id="68ff4-116"><dt>**NO\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="68ff4-117">No se encontró ningún error y continúe procesando el archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="68ff4-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="68ff4-118"><dt>\**Error \_* de XXX \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="68ff4-118"><dt>\**ERROR\_* XXX\*\*\*</dt></span></span> </dl> | <span data-ttu-id="68ff4-119">Se produjo un error del tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="68ff4-119">An error of the specified type occurred.</span></span> <span data-ttu-id="68ff4-120">La función [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) devolverá **false** y el código de error especificado será devuelto por una llamada a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="68ff4-120">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="68ff4-121">No hay ninguna rutina de devolución de llamada del archivo. cab predeterminada; por lo tanto, debe proporcionar una rutina de devolución de llamada para controlar las notificaciones enviadas por [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="68ff4-121">There is no default cabinet callback routine; thus, you must supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="remarks"></a><span data-ttu-id="68ff4-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68ff4-122">Remarks</span></span>

<span data-ttu-id="68ff4-123">Si la rutina de devolución de llamada NO devuelve ningún \_ error, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) comprueba el búfer señalado por *parám2*.</span><span class="sxs-lookup"><span data-stu-id="68ff4-123">If the callback routine returns NO\_ERROR, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) checks the buffer pointed to by *Param2*.</span></span> <span data-ttu-id="68ff4-124">Si el búfer no está vacío, contiene una nueva ruta de acceso de origen.</span><span class="sxs-lookup"><span data-stu-id="68ff4-124">If the buffer is not empty, then it contains a new source path.</span></span> <span data-ttu-id="68ff4-125">Si el búfer está vacío, se supone que la ruta de acceso de origen no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="68ff4-125">If the buffer is empty, the source path is assumed to be unchanged.</span></span>

<span data-ttu-id="68ff4-126">La función de devolución de llamada debe asegurarse de que el archivo. cab es accesible antes de que vuelva, llamando a la función [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) , en caso de que sea necesario insertar nuevos medios.</span><span class="sxs-lookup"><span data-stu-id="68ff4-126">Your callback function should ensure that the cabinet is accessible before it returns, calling the [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) function, if new media needs to be inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="68ff4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68ff4-127">Requirements</span></span>



| <span data-ttu-id="68ff4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="68ff4-128">Requirement</span></span> | <span data-ttu-id="68ff4-129">Value</span><span class="sxs-lookup"><span data-stu-id="68ff4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68ff4-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68ff4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="68ff4-131">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="68ff4-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="68ff4-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68ff4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="68ff4-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="68ff4-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68ff4-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68ff4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="68ff4-135"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="68ff4-135"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68ff4-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="68ff4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ff4-137">Información general</span><span class="sxs-lookup"><span data-stu-id="68ff4-137">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="68ff4-138">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="68ff4-138">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="68ff4-139">**información del archivo. cab \_**</span><span class="sxs-lookup"><span data-stu-id="68ff4-139">**CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="68ff4-140">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="68ff4-140">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

