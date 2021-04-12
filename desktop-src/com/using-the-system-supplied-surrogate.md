---
title: Usar el suplente System-Supplied
description: Usar el suplente System-Supplied
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357723"
---
# <a name="using-the-system-supplied-surrogate"></a><span data-ttu-id="4414f-103">Usar el suplente System-Supplied</span><span class="sxs-lookup"><span data-stu-id="4414f-103">Using the System-Supplied Surrogate</span></span>

<span data-ttu-id="4414f-104">Para usar el suplente proporcionado por el sistema para el servidor DLL, registre el archivo DLL especificando una cadena vacía o **null** para el valor [DllSurrogate](dllsurrogate.md) en el registro.</span><span class="sxs-lookup"><span data-stu-id="4414f-104">To use the system-supplied surrogate for your DLL server, register the DLL specifying an empty string or **NULL** for the [DllSurrogate](dllsurrogate.md) value in the registry.</span></span> <span data-ttu-id="4414f-105">Cuando una solicitud de activación para un servidor DLL, por lo que se trata de COM, COM inicia el proceso suplente predeterminado y el archivo DLL solicitado (especificando el CLSID en la línea de comandos de inicio internamente) al mismo tiempo para evitar una llamada independiente.</span><span class="sxs-lookup"><span data-stu-id="4414f-105">When an activation request for a DLL server so designated comes to COM, COM launches the default surrogate process and the requested DLL (by specifying the CLSID on the launch command line internally) at the same time to avoid a separate call.</span></span> <span data-ttu-id="4414f-106">(Para obtener información sobre cómo ejecutar más de un servidor DLL en un proceso suplente, vea [uso compartido de suplentes](surrogate-sharing.md)).</span><span class="sxs-lookup"><span data-stu-id="4414f-106">(For information on running more than one DLL server in a surrogate process, see [Surrogate Sharing](surrogate-sharing.md).)</span></span>

<span data-ttu-id="4414f-107">La implementación predeterminada del proceso suplente es un servidor pseudo-COM de estilo de modelo de subprocesos mixtos.</span><span class="sxs-lookup"><span data-stu-id="4414f-107">The default implementation of the surrogate process is a mixed-threading model style pseudo-COM server.</span></span> <span data-ttu-id="4414f-108">Cuando se cargan varios servidores DLL en un único proceso suplente, este proceso garantiza que se crea una instancia de cada servidor DLL utilizando el modelo de subprocesos especificado en el registro para ese servidor.</span><span class="sxs-lookup"><span data-stu-id="4414f-108">When multiple DLL servers are loaded into a single surrogate process, this process ensures that each DLL server is instantiated using the threading model specified in the registry for that server.</span></span> <span data-ttu-id="4414f-109">Todos los servidores de subprocesos libres cargados residirán juntos en el apartamento multiproceso, mientras que cada servidor de subprocesos de Apartamento residirá en un contenedor uniproceso.</span><span class="sxs-lookup"><span data-stu-id="4414f-109">All loaded free-threaded servers will live together in the multithreaded apartment, while each apartment-threaded server will reside in a single-threaded apartment.</span></span> <span data-ttu-id="4414f-110">Si un servidor DLL admite ambos modelos de subprocesos, COM elegirá multithreading.</span><span class="sxs-lookup"><span data-stu-id="4414f-110">If a DLL server supports both threading models, COM will choose multithreading.</span></span>

<span data-ttu-id="4414f-111">Este proceso suplente se escribe para que COM controle tanto la descarga de los servidores DLL como la terminación del proceso suplente.</span><span class="sxs-lookup"><span data-stu-id="4414f-111">This surrogate process is written so that COM handles both the unloading of DLL servers and the terminating of the surrogate process.</span></span>

<span data-ttu-id="4414f-112">El suplente proporcionado por el sistema funcionará muy bien para la mayoría de los desarrolladores, así como para que sea muy fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="4414f-112">The system-provided surrogate will work very well for most developers, as well as being very easy to use.</span></span> <span data-ttu-id="4414f-113">Sin embargo, los desarrolladores con consideraciones especiales pueden decidir que es necesario un suplente personalizado.</span><span class="sxs-lookup"><span data-stu-id="4414f-113">However, those developers with special considerations may decide that a custom surrogate is necessary.</span></span> <span data-ttu-id="4414f-114">Para obtener más información, consulte [Writing a Custom suplente](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="4414f-114">For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4414f-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4414f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4414f-116">Suplentes DLL</span><span class="sxs-lookup"><span data-stu-id="4414f-116">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




