---
title: Suplentes DLL
description: Suplentes DLL
ms.assetid: fe30c0ae-1d19-4a5f-8ee3-8a5337c79c44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c3fcbd07b4c6317dfb6ac8ede772fc62035f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714258"
---
# <a name="dll-surrogates"></a><span data-ttu-id="05b88-103">Suplentes DLL</span><span class="sxs-lookup"><span data-stu-id="05b88-103">DLL Surrogates</span></span>

<span data-ttu-id="05b88-104">COM permite crear servidores DLL que se pueden cargar en un proceso EXE suplente.</span><span class="sxs-lookup"><span data-stu-id="05b88-104">COM makes it possible to create DLL servers that can be loaded into a surrogate EXE process.</span></span> <span data-ttu-id="05b88-105">Esto combina la facilidad de escritura de servidores DLL con las ventajas de la implementación ejecutable.</span><span class="sxs-lookup"><span data-stu-id="05b88-105">This combines the ease of writing DLL servers with the benefits of executable implementation.</span></span> <span data-ttu-id="05b88-106">Las herramientas de desarrollo como Microsoft Visual Studio facilitan la escritura de servidores DLL, pero un servidor DLL en sí mismo tiene límites.</span><span class="sxs-lookup"><span data-stu-id="05b88-106">Development tools like Microsoft Visual Studio facilitate the writing of DLL servers, but a DLL server in itself has limits.</span></span> <span data-ttu-id="05b88-107">La ejecución del servidor DLL en un proceso suplente ofrece varias ventajas posibles:</span><span class="sxs-lookup"><span data-stu-id="05b88-107">Running the DLL server in a surrogate process offers several possible benefits:</span></span>

-   <span data-ttu-id="05b88-108">Aislamiento de errores y la capacidad de atender a varios clientes simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="05b88-108">Fault isolation and the ability to service multiple clients simultaneously.</span></span>
-   <span data-ttu-id="05b88-109">En un entorno distribuido, se puede usar una implementación de servidor DLL para atender a los clientes remotos.</span><span class="sxs-lookup"><span data-stu-id="05b88-109">In a distributed environment, a DLL server implementation could be used to service remote clients.</span></span>
-   <span data-ttu-id="05b88-110">Puede permitir que los clientes ayuden a protegerse del código de servidor que no es de confianza, a la vez que permiten el acceso a los servicios que proporciona el servidor DLL.</span><span class="sxs-lookup"><span data-stu-id="05b88-110">It could permit clients to help protect themselves from untrusted server code while allowing them access to the services the DLL server provides.</span></span>
-   <span data-ttu-id="05b88-111">La ejecución de un servidor DLL en un suplente proporciona el archivo DLL con la seguridad del suplente.</span><span class="sxs-lookup"><span data-stu-id="05b88-111">Running a DLL server in a surrogate provides the DLL with the surrogate's security.</span></span>

<span data-ttu-id="05b88-112">COM proporciona un proceso suplente predeterminado, o puede escribir un suplente personalizado si tiene necesidades especiales.</span><span class="sxs-lookup"><span data-stu-id="05b88-112">COM provides a default surrogate process, or you can write a custom surrogate if you have special needs.</span></span>

<span data-ttu-id="05b88-113">En los temas siguientes se proporciona más información sobre los suplentes de DLL:</span><span class="sxs-lookup"><span data-stu-id="05b88-113">The following topics provide more information on DLL surrogates:</span></span>

-   [<span data-ttu-id="05b88-114">Requisitos del servidor DLL</span><span class="sxs-lookup"><span data-stu-id="05b88-114">DLL Server Requirements</span></span>](dll-server-requirements.md)
-   [<span data-ttu-id="05b88-115">Usar el suplente System-Supplied</span><span class="sxs-lookup"><span data-stu-id="05b88-115">Using the System-Supplied Surrogate</span></span>](using-the-system-supplied-surrogate.md)
-   [<span data-ttu-id="05b88-116">Escritura de un suplente personalizado</span><span class="sxs-lookup"><span data-stu-id="05b88-116">Writing a Custom Surrogate</span></span>](writing-a-custom-surrogate.md)

 

 




