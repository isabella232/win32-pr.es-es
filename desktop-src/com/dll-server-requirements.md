---
title: Requisitos del servidor DLL
description: Aunque la mayoría de los archivos DLL se pueden ejecutar en un suplente, algunos archivos dll no.
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076376"
---
# <a name="dll-server-requirements"></a><span data-ttu-id="e4783-103">Requisitos del servidor DLL</span><span class="sxs-lookup"><span data-stu-id="e4783-103">DLL Server Requirements</span></span>

<span data-ttu-id="e4783-104">Aunque la mayoría de los archivos DLL se pueden ejecutar en un suplente, algunos archivos dll no.</span><span class="sxs-lookup"><span data-stu-id="e4783-104">While most DLLs can run in a surrogate, some DLLs cannot.</span></span>

<span data-ttu-id="e4783-105">Si desea utilizar el suplente proporcionado por el sistema, el archivo DLL debe estar bien comportado.</span><span class="sxs-lookup"><span data-stu-id="e4783-105">The DLL must be well-behaved if you want to use the system-supplied surrogate.</span></span> <span data-ttu-id="e4783-106">Por ejemplo, un archivo DLL que llama a métodos que registran devoluciones de llamada del cliente intentaría invocar esas devoluciones de llamada como si los punteros de función recibidos fueran instrucciones en su espacio de direcciones, que no es el caso.</span><span class="sxs-lookup"><span data-stu-id="e4783-106">For example, a DLL that calls methods that register callbacks from the client would try to invoke those callbacks as if the function pointers it received were for instructions in its address space, which is not the case.</span></span> <span data-ttu-id="e4783-107">Del mismo modo, un archivo DLL que utiliza una variable global a la que espera que el cliente tenga acceso no funciona.</span><span class="sxs-lookup"><span data-stu-id="e4783-107">Similarly, a DLL that uses a global variable that it expects the client to access would not work.</span></span> <span data-ttu-id="e4783-108">En general, los parámetros que no se pueden serializar correctamente impedirán que el servidor DLL se ejecute fuera del proceso del cliente.</span><span class="sxs-lookup"><span data-stu-id="e4783-108">In general, parameters that cannot be properly marshaled will prevent the DLL server from running outside the client process.</span></span> <span data-ttu-id="e4783-109">En muchos casos, puede escribir un suplente personalizado diseñado específicamente para compensar el comportamiento "incorrecto".</span><span class="sxs-lookup"><span data-stu-id="e4783-109">In many cases, you can write a custom surrogate specifically designed to compensate for "bad" behavior.</span></span> <span data-ttu-id="e4783-110">(Para obtener más información, consulte [Writing a Custom suplente](writing-a-custom-surrogate.md)).</span><span class="sxs-lookup"><span data-stu-id="e4783-110">(For more information, see [Writing a Custom Surrogate](writing-a-custom-surrogate.md).)</span></span>

<span data-ttu-id="e4783-111">Si el servidor DLL usa interfaces personalizadas, tendría que asegurarse de que el código de serialización esté disponible para esas interfaces.</span><span class="sxs-lookup"><span data-stu-id="e4783-111">If the DLL server uses custom interfaces, you would have to ensure that marshaling code is available for those interfaces.</span></span> <span data-ttu-id="e4783-112">Por ejemplo, puede generar y registrar un archivo DLL de proxy, o proporcionar y registrar una biblioteca de tipos que permita que el servidor funcione correctamente mientras se ejecuta en un suplente.</span><span class="sxs-lookup"><span data-stu-id="e4783-112">For example, you could build and register a proxy DLL or provide and register a type library that would allow the server to function correctly while running in a surrogate.</span></span>

<span data-ttu-id="e4783-113">Los servidores DLL se cargarán solo en un proceso suplente que se ejecute en el contexto de seguridad adecuado.</span><span class="sxs-lookup"><span data-stu-id="e4783-113">DLL servers will be loaded only into a surrogate process running in the proper security context.</span></span> <span data-ttu-id="e4783-114">El contexto de seguridad para el suplente del servidor DLL se determina de la misma manera que para los servidores EXE.</span><span class="sxs-lookup"><span data-stu-id="e4783-114">The security context for the DLL server surrogate is determined in the same way as for EXE servers.</span></span> <span data-ttu-id="e4783-115">El suplente del servidor DLL se ejecuta en el mismo contexto de seguridad que el cliente, a menos que se establezca un valor **runas** , que determina el contexto de seguridad, en la sección del registro [AppID](appid-clsid.md) del servidor.</span><span class="sxs-lookup"><span data-stu-id="e4783-115">The DLL server surrogate runs in the same security context as the client, unless a **RunAs** value, which determines the security context, is set in the [AppID](appid-clsid.md) registry section for the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4783-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4783-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4783-117">Suplentes DLL</span><span class="sxs-lookup"><span data-stu-id="e4783-117">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 




