---
description: Cierra el subproceso de resolución de nombres de usuario.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Método DiskQuotaControl. ShutdownNameResolution (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082072"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a><span data-ttu-id="3705f-103">DiskQuotaControl. ShutdownNameResolution, método</span><span class="sxs-lookup"><span data-stu-id="3705f-103">DiskQuotaControl.ShutdownNameResolution method</span></span>

<span data-ttu-id="3705f-104">Cierra el subproceso de resolución de nombres de usuario.</span><span class="sxs-lookup"><span data-stu-id="3705f-104">Shuts down the user name resolution thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="3705f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3705f-105">Syntax</span></span>


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a><span data-ttu-id="3705f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3705f-106">Parameters</span></span>

<span data-ttu-id="3705f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3705f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3705f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3705f-108">Return value</span></span>

<span data-ttu-id="3705f-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3705f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3705f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3705f-110">Remarks</span></span>

<span data-ttu-id="3705f-111">La resolución de nombres del identificador de seguridad (SID) traduce el SID a los nombres de usuario en un subproceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="3705f-111">The security identifier (SID) name resolver translates SID to user names on a background thread.</span></span> <span data-ttu-id="3705f-112">Este subproceso se cierra automáticamente cuando se destruye el objeto de control de cuota asociado.</span><span class="sxs-lookup"><span data-stu-id="3705f-112">This thread is shut down automatically when the associated quota control object is destroyed.</span></span> <span data-ttu-id="3705f-113">Sin embargo, hay algunos casos en los que el subproceso ya no se necesita, pero el objeto todavía no está listo para ser destruido.</span><span class="sxs-lookup"><span data-stu-id="3705f-113">However, there are some cases when the thread is no longer needed, but the object is not yet ready to be destroyed.</span></span> <span data-ttu-id="3705f-114">Un ejemplo típico es cuando no se realiza ningún otro procesamiento, pero los clientes siguen conservando las referencias al objeto.</span><span class="sxs-lookup"><span data-stu-id="3705f-114">A typical example is when no further processing is taking place, but clients are still holding references to the object.</span></span> <span data-ttu-id="3705f-115">El método **ShutdownNameResolution** permite terminar el subproceso de resolución y liberar los recursos asociados sin destruir el objeto de control de cuota.</span><span class="sxs-lookup"><span data-stu-id="3705f-115">The **ShutdownNameResolution** method allows you to terminate the resolver thread and free the associated resources without destroying the quota control object.</span></span>

> [!Note]  
> <span data-ttu-id="3705f-116">Al cerrar el subproceso de resolución, se detiene inmediatamente la resolución de nombres asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3705f-116">When you shut down the resolver thread, asynchronous name resolution immediately stops.</span></span> <span data-ttu-id="3705f-117">Si posteriormente se realizan llamadas a métodos como [**adduser**](diskquotacontrol-adduser.md) o [**FindUser**](diskquotacontrol-finduser.md), el objeto de cuota podría volver a crear el subproceso de resolución.</span><span class="sxs-lookup"><span data-stu-id="3705f-117">If calls are subsequently made to methods such as [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md), the quota object might re-create the resolver thread.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3705f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3705f-118">Requirements</span></span>



| <span data-ttu-id="3705f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3705f-119">Requirement</span></span> | <span data-ttu-id="3705f-120">Value</span><span class="sxs-lookup"><span data-stu-id="3705f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3705f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3705f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3705f-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3705f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3705f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3705f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3705f-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3705f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3705f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3705f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3705f-126"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="3705f-126"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="3705f-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3705f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3705f-128"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3705f-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3705f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3705f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3705f-130">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="3705f-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




