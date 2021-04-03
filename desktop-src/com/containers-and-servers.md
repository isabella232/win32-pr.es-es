---
title: Contenedores y servidores
description: Contenedores y servidores
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903854"
---
# <a name="containers-and-servers"></a><span data-ttu-id="f1cc0-103">Contenedores y servidores</span><span class="sxs-lookup"><span data-stu-id="f1cc0-103">Containers and Servers</span></span>

<span data-ttu-id="f1cc0-104">Las aplicaciones de documentos compuestos son de dos tipos básicos: aplicaciones de contenedor y aplicaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-104">Compound document applications are of two basic types: container applications and server applications.</span></span> <span data-ttu-id="f1cc0-105">Las aplicaciones contenedoras OLE proporcionan a los usuarios la capacidad de crear, editar, guardar y recuperar documentos compuestos.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-105">OLE container applications provide users with the ability to create, edit, save, and retrieve compound documents.</span></span> <span data-ttu-id="f1cc0-106">Las aplicaciones de servidor OLE proporcionan a los usuarios los medios para crear documentos y otras representaciones de datos que se pueden incluir como vínculos o incrustaciones en aplicaciones de contenedor.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-106">OLE server applications provide users with the means to create documents and other data representations that can be contained as either links or embeddings in container applications.</span></span> <span data-ttu-id="f1cc0-107">Una aplicación OLE puede ser una aplicación contenedora, una aplicación de servidor o ambas.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-107">An OLE application can be a container application, a server application, or both.</span></span>

<span data-ttu-id="f1cc0-108">Las aplicaciones de servidor OLE también difieren en si se implementan como *servidores en proceso* o *servidores locales*.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-108">OLE server applications also differ in whether they are implemented as *in-process servers* or *local servers*.</span></span> <span data-ttu-id="f1cc0-109">Un servidor en proceso es una biblioteca de vínculos dinámicos (DLL) que se ejecuta en el espacio de proceso de la aplicación contenedora.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-109">An in-process server is a dynamic link library (DLL) that runs in the container application's process space.</span></span> <span data-ttu-id="f1cc0-110">Puede ejecutar un servidor en proceso solo desde dentro de la aplicación contenedora.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-110">You can run an in-process server only from within the container application.</span></span>

> [!Note]  
> <span data-ttu-id="f1cc0-111">Las versiones futuras de OLE habilitarán la vinculación e incrustación a través de los límites del equipo, de modo que una aplicación contenedora en un equipo podrá usar un objeto de documento compuesto proporcionado por un *servidor remoto* que se ejecuta en otro equipo.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-111">Future releases of OLE will enable linking and embedding across computer boundaries, so that a container application on one computer will be able to use a compound document object provided by a *remote server* running on another computer.</span></span> <span data-ttu-id="f1cc0-112">Desde el punto de vista de una aplicación contenedora, cualquier aplicación de servidor OLE que se ejecute en su propio espacio de proceso, ya sea en el mismo equipo o en un equipo remoto, es un *servidor fuera de processÂ*.</span><span class="sxs-lookup"><span data-stu-id="f1cc0-112">From a container application's point of view, any OLE server application that runs in its own process space, whether on the same computer or a remote computer, is an *out-of-processÂ server*.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f1cc0-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f1cc0-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1cc0-114">Documentos compuestos</span><span class="sxs-lookup"><span data-stu-id="f1cc0-114">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="f1cc0-115">Servidores en proceso</span><span class="sxs-lookup"><span data-stu-id="f1cc0-115">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




