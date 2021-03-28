---
description: Se envía a la función CPlApplet de una aplicación del panel de control para solicitarle que realice una inicialización global, especialmente la asignación de memoria.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: Mensaje de CPL_INIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984338"
---
# <a name="cpl_init-message"></a><span data-ttu-id="8da99-103">CPL \_ mensaje init</span><span class="sxs-lookup"><span data-stu-id="8da99-103">CPL\_INIT message</span></span>

<span data-ttu-id="8da99-104">Se envía a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de una aplicación del panel de control para solicitarle que realice una inicialización global, especialmente la asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="8da99-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to prompt it to perform global initialization, especially memory allocation.</span></span>


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a><span data-ttu-id="8da99-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8da99-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8da99-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8da99-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8da99-107">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8da99-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8da99-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8da99-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8da99-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8da99-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8da99-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8da99-110">Return value</span></span>

<span data-ttu-id="8da99-111">Si la inicialización se realiza correctamente, la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) debe devolver un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8da99-111">If initialization succeeds, the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function should return nonzero.</span></span> <span data-ttu-id="8da99-112">De lo contrario, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="8da99-112">Otherwise, it should return zero.</span></span>

<span data-ttu-id="8da99-113">Si [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) devuelve cero, la aplicación de control finaliza la comunicación y libera el archivo DLL que contiene la aplicación del panel de control.</span><span class="sxs-lookup"><span data-stu-id="8da99-113">If [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) returns zero, the controlling application ends communication and releases the DLL containing the Control Panel application.</span></span>

## <a name="remarks"></a><span data-ttu-id="8da99-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8da99-114">Remarks</span></span>

<span data-ttu-id="8da99-115">Dado que esta es la única manera en que una aplicación del panel de control puede indicar una condición de error, la aplicación debe asignar memoria en respuesta a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="8da99-115">Because this is the only way a Control Panel application can signal an error condition, the application should allocate memory in response to this message.</span></span>

<span data-ttu-id="8da99-116">Este mensaje se envía inmediatamente después de que se cargue el archivo DLL que contiene la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8da99-116">This message is sent immediately after the DLL containing the application is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="8da99-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8da99-117">Requirements</span></span>



| <span data-ttu-id="8da99-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da99-118">Requirement</span></span> | <span data-ttu-id="8da99-119">Value</span><span class="sxs-lookup"><span data-stu-id="8da99-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8da99-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8da99-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8da99-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8da99-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8da99-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8da99-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8da99-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8da99-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8da99-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8da99-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8da99-125"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8da99-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da99-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8da99-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da99-127">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="8da99-127">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
