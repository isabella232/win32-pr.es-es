---
title: Control de errores de aplicación de servidor
description: Si la aplicación de servidor procesa correctamente el archivo cargado, la aplicación debe devolver 200.
ms.assetid: fd0b10f1-52b4-4564-9683-620f3b965680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6019f296cb3b960369efc2c3ca8f25eb7738e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773392"
---
# <a name="handling-server-application-errors"></a><span data-ttu-id="e64d1-103">Control de errores de aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="e64d1-103">Handling Server Application Errors</span></span>

<span data-ttu-id="e64d1-104">Si la aplicación de servidor procesa correctamente el archivo cargado, la aplicación debe devolver 200.</span><span class="sxs-lookup"><span data-stu-id="e64d1-104">If the server application successfully processes the uploaded file, the application should return 200.</span></span> <span data-ttu-id="e64d1-105">Si la aplicación no devuelve 200, el cliente de BITS utiliza el código de error para determinar si el error es un error transitorio o un error grave.</span><span class="sxs-lookup"><span data-stu-id="e64d1-105">If the application does not return 200, the BITS client uses the error code to determine if the error is a transient error or fatal error.</span></span>

<span data-ttu-id="e64d1-106">Todos los códigos de error 3xx son errores transitorios excepto 300-305 y 307, que son errores irrecuperables.</span><span class="sxs-lookup"><span data-stu-id="e64d1-106">All 3xx error codes are transient errors except 300 - 305 and 307, which are fatal errors.</span></span> <span data-ttu-id="e64d1-107">Todos los códigos de error 4xx son errores irrecuperables, excepto 408 y 409, que son errores transitorios.</span><span class="sxs-lookup"><span data-stu-id="e64d1-107">All 4xx error codes are fatal errors except for 408 and 409, which are transient errors.</span></span> <span data-ttu-id="e64d1-108">Todos los códigos de error 5xx son errores transitorios excepto 501 y 505, que son errores irrecuperables.</span><span class="sxs-lookup"><span data-stu-id="e64d1-108">All 5xx error codes are transient errors except 501 and 505, which are fatal errors.</span></span> <span data-ttu-id="e64d1-109">El resto de códigos HTTP se consideran errores transitorios.</span><span class="sxs-lookup"><span data-stu-id="e64d1-109">All other HTTP codes are considered transient errors.</span></span> <span data-ttu-id="e64d1-110">Tenga en cuenta que un código de error 403 es el único código de error que impide que BITS publique el archivo de carga en la aplicación de servidor de nuevo.</span><span class="sxs-lookup"><span data-stu-id="e64d1-110">Note that a 403 error code is the only error code that prevents BITS from posting the upload file to the server application again.</span></span>

<span data-ttu-id="e64d1-111">Para recuperar el error, llame al método [**IBackgroundCopyError:: GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) .</span><span class="sxs-lookup"><span data-stu-id="e64d1-111">To retrieve the error, call the [**IBackgroundCopyError::GetError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyerror-geterror) method.</span></span> <span data-ttu-id="e64d1-112">El contexto de error será la \_ aplicación remota de contexto de error de BG \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e64d1-112">The error context will be BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION.</span></span>

 

 




