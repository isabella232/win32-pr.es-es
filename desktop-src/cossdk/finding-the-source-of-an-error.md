---
description: Buscar el origen de un error
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Buscar el origen de un error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080267"
---
# <a name="finding-the-source-of-an-error"></a><span data-ttu-id="7dc6e-103">Buscar el origen de un error</span><span class="sxs-lookup"><span data-stu-id="7dc6e-103">Finding the Source of an Error</span></span>

<span data-ttu-id="7dc6e-104">Puede diagnosticar el origen y obtener una descripción de los errores de la aplicación mediante COM+ y otras herramientas.</span><span class="sxs-lookup"><span data-stu-id="7dc6e-104">You can diagnose the source and obtain a description of application errors by using COM+ and other tools.</span></span> <span data-ttu-id="7dc6e-105">Si detecta que el error de aplicación se debe a COM+, puede interpretar el mensaje de error que se ve en el archivo Winerror. h o mediante la utilidad de error Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="7dc6e-105">If you discover that the application error is caused by COM+, you can interpret the error message viewing the Winerror.h file or by using the Microsoft Visual C++ error utility.</span></span>

<span data-ttu-id="7dc6e-106">Si se produce un error en la aplicación de servidor o se produce un comportamiento inesperado, primero debe determinar dónde se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="7dc6e-106">If your server application is failing or causing unexpected behavior, you must first determine where the error occurred.</span></span> <span data-ttu-id="7dc6e-107">El sistema Visor de eventos realiza un seguimiento de los eventos de aplicación, seguridad y sistema.</span><span class="sxs-lookup"><span data-stu-id="7dc6e-107">The system Event Viewer tracks application, security, and system events.</span></span> <span data-ttu-id="7dc6e-108">Muchos errores "silenciosos" se registran aquí.</span><span class="sxs-lookup"><span data-stu-id="7dc6e-108">Many "silent" errors are recorded here.</span></span> <span data-ttu-id="7dc6e-109">Sin embargo, no todos los errores se muestran en el Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="7dc6e-109">However, not all errors are shown in the Event Viewer.</span></span>

<span data-ttu-id="7dc6e-110">En primer lugar, debe hacer referencia al registro de la aplicación en el Visor de eventos para comprobar la aplicación asociada con el mensaje de evento.</span><span class="sxs-lookup"><span data-stu-id="7dc6e-110">You should first refer to the application log in the Event Viewer to check the application associated with the event message.</span></span> <span data-ttu-id="7dc6e-111">(Dado que también puede archivar registros de eventos, puede realizar el seguimiento de un historial de eventos del error). Al hacer doble clic en una entrada del registro se activa una página de **propiedades de evento** , que proporciona más información sobre el evento del sistema.</span><span class="sxs-lookup"><span data-stu-id="7dc6e-111">(Because you can also archive event logs, you can track an event history of the error.) Double-clicking an entry in your log activates an **Event Properties** page, which provides further information about the system event.</span></span>

<span data-ttu-id="7dc6e-112">Para obtener más información sobre cómo depurar una aplicación COM+, vea [depurar aplicaciones com+](debugging-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="7dc6e-112">For more information on debugging a COM+ application, see [Debugging COM+ Applications](debugging-com--applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dc6e-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7dc6e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dc6e-114">Aislamiento de errores y Directiva FailFast</span><span class="sxs-lookup"><span data-stu-id="7dc6e-114">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="7dc6e-115">Cómo modifica COM+ los valores devueltos</span><span class="sxs-lookup"><span data-stu-id="7dc6e-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="7dc6e-116">Interpretar códigos de error</span><span class="sxs-lookup"><span data-stu-id="7dc6e-116">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="7dc6e-117">Estrategias para controlar errores en COM+</span><span class="sxs-lookup"><span data-stu-id="7dc6e-117">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="7dc6e-118">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="7dc6e-118">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



