---
description: Solución de problemas
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Solución de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686443"
---
# <a name="troubleshooting"></a><span data-ttu-id="173aa-103">Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="173aa-103">Troubleshooting</span></span>

<span data-ttu-id="173aa-104">Si tiene problemas para diagnosticar los errores de la aplicación, consulte las sugerencias de solución de problemas siguientes:</span><span class="sxs-lookup"><span data-stu-id="173aa-104">If you are having trouble diagnosing your application errors, refer to the following of troubleshooting tips:</span></span>

-   <span data-ttu-id="173aa-105">Asegúrese de que el Coordinador de transacciones distribuidas (DTC) se está ejecutando en todos los servidores.</span><span class="sxs-lookup"><span data-stu-id="173aa-105">Make sure that the Distributed Transaction Coordinator (DTC) is running on all servers.</span></span>
-   <span data-ttu-id="173aa-106">Compruebe la comunicación de red comprobando primero en un equipo local para comprobar que la aplicación funciona.</span><span class="sxs-lookup"><span data-stu-id="173aa-106">Check network communication by first testing on a local computer to verify that the application works.</span></span> <span data-ttu-id="173aa-107">Si está ejecutando TCP/IP en la red, puede usar la utilidad de ping.exe para comprobar que los equipos están en la red.</span><span class="sxs-lookup"><span data-stu-id="173aa-107">If you are running TCP/IP on your network, you can use the ping.exe utility to verify that the machines are on the network.</span></span>
-   <span data-ttu-id="173aa-108">Asegúrese de que SQL y DTC están ubicados en el mismo equipo o de que el programa de configuración del cliente de DTC especifica que el DTC está en otro equipo.</span><span class="sxs-lookup"><span data-stu-id="173aa-108">Make sure that SQL and DTC are located on the same computer or that the DTC Client Configuration program specifies that the DTC is on another computer.</span></span> <span data-ttu-id="173aa-109">Si no es así, SQLConnect devolverá un error internamente cuando se llame desde un componente transaccional.</span><span class="sxs-lookup"><span data-stu-id="173aa-109">If not, SQLConnect will return an error internally when called from a transactional component.</span></span>
-   <span data-ttu-id="173aa-110">Establezca el tiempo de espera de la transacción en un número mayor que el valor predeterminado de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="173aa-110">Set the transaction time-out to a higher number than the default 60 seconds.</span></span> <span data-ttu-id="173aa-111">Una vez transcurrido el tiempo de espera de la transacción, COM+ anula la transacción.</span><span class="sxs-lookup"><span data-stu-id="173aa-111">After the transaction time-out has elapsed, COM+ aborts the transaction.</span></span> <span data-ttu-id="173aa-112">Todas las llamadas subsiguientes al componente devuelven inmediatamente con el contexto \_ E \_ anulado.</span><span class="sxs-lookup"><span data-stu-id="173aa-112">All subsequent calls to the component return immediately with CONTEXT\_E\_ABORTED.</span></span>
-   <span data-ttu-id="173aa-113">Asegúrese de que los controladores ODBC son seguros para subprocesos y no tienen afinidad de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="173aa-113">Make sure that your ODBC drivers are thread-safe and do not have thread affinity.</span></span>
-   <span data-ttu-id="173aa-114">Si tiene dificultades para conseguir que una aplicación funcione en varios servidores, reinicie el cliente y, a continuación, compruebe que el controlador de dominio está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="173aa-114">If you have difficulty getting an application to work over several servers, reboot the client and then verify that your domain controller is configured properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="173aa-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="173aa-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="173aa-116">Aislamiento de errores y Directiva FailFast</span><span class="sxs-lookup"><span data-stu-id="173aa-116">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="173aa-117">Buscar el origen de un error</span><span class="sxs-lookup"><span data-stu-id="173aa-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="173aa-118">Cómo modifica COM+ los valores devueltos</span><span class="sxs-lookup"><span data-stu-id="173aa-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="173aa-119">Interpretar códigos de error</span><span class="sxs-lookup"><span data-stu-id="173aa-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="173aa-120">Estrategias para controlar errores en COM+</span><span class="sxs-lookup"><span data-stu-id="173aa-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



