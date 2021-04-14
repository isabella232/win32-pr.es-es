---
description: Control de errores en COM+ CRM
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Control de errores en COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496342"
---
# <a name="error-handling-in-the-com-crm"></a><span data-ttu-id="833a7-103">Control de errores en COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="833a7-103">Error Handling in the COM+ CRM</span></span>

<span data-ttu-id="833a7-104">Las aplicaciones de servidor COM+ implementan una directiva FailFast.</span><span class="sxs-lookup"><span data-stu-id="833a7-104">COM+ server applications implement a failfast policy.</span></span> <span data-ttu-id="833a7-105">Si se detecta un error interno grave, el proceso de aplicación de servidor se cierra y escribe un mensaje de error en el registro de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="833a7-105">If a serious internal error is detected, the server application process exits and writes an error message to the Windows event log.</span></span> <span data-ttu-id="833a7-106">Esto permite la detección rápida de problemas y es posible debido a la protección de los datos de la aplicación por el procesamiento de transacciones.</span><span class="sxs-lookup"><span data-stu-id="833a7-106">This allows quick detection of problems and is possible due to the protection of application data by transaction processing.</span></span> <span data-ttu-id="833a7-107">Compruebe siempre el registro de eventos de Windows en busca de errores de CRM, ya sea durante el desarrollo o durante la implementación final.</span><span class="sxs-lookup"><span data-stu-id="833a7-107">Always check the Windows event log for any errors from the CRM, either during development or during final deployment.</span></span>

<span data-ttu-id="833a7-108">Errores básicos en el uso de las interfaces de CRM, como argumentos no válidos o errores de secuencia (por ejemplo, si se intenta escribir una entrada de registro antes de registrar el compensador de CRM), devuelven códigos de error y no deben desencadenar FailFast.</span><span class="sxs-lookup"><span data-stu-id="833a7-108">Basic errors in using the CRM interfaces, such as invalid arguments or sequence errors (for example, trying to write a log record before registering the CRM Compensator), return error codes and should not trigger failfast.</span></span> <span data-ttu-id="833a7-109">Para el desarrollo de CRM, puede optar por establecer la clave del registro VTRACE1 (consulte [configuración del registro de com+ CRM](com--crm-registry-settings.md)), que hace que aparezca un mensaje en la ventana de salida del depurador para cada error.</span><span class="sxs-lookup"><span data-stu-id="833a7-109">For CRM development, you may choose to set the VTRACE1 registry key (see [COM+ CRM Registry Settings](com--crm-registry-settings.md)), which causes a message to appear in the debugger output window for each error.</span></span>

<span data-ttu-id="833a7-110">También se pueden producir errores transitorios.</span><span class="sxs-lookup"><span data-stu-id="833a7-110">Transient errors can also occur.</span></span> <span data-ttu-id="833a7-111">Normalmente, estos errores se deben a condiciones de control de tiempo y provocan que se devuelva un código de error.</span><span class="sxs-lookup"><span data-stu-id="833a7-111">These errors are typically caused by timing conditions and result in an error code being returned.</span></span> <span data-ttu-id="833a7-112">El desarrollador de CRM debe asegurarse de que se controlen estas condiciones de error.</span><span class="sxs-lookup"><span data-stu-id="833a7-112">The CRM developer should ensure that these error conditions are handled.</span></span> <span data-ttu-id="833a7-113">Por ejemplo, al escribir una entrada de registro, la transacción podría anularse debido a un tiempo de espera. Después, el método devuelve un error, que el autor de la llamada debe comprobar y controlar de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="833a7-113">For example, while writing a log record, the transaction could abort due to a time-out. The method then returns an error, which the caller should check for and handle appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="833a7-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="833a7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="833a7-115">Conceptos de Administrador de recursos de compensación de COM+</span><span class="sxs-lookup"><span data-stu-id="833a7-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



