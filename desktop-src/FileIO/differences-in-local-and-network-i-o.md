---
description: Diferencias entre la e/s local y la e/s de red en Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Diferencias en la e/s local y de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667703"
---
# <a name="differences-in-local-and-network-io"></a><span data-ttu-id="51f9f-103">Diferencias en la e/s local y de red</span><span class="sxs-lookup"><span data-stu-id="51f9f-103">Differences in Local and Network I/O</span></span>

<span data-ttu-id="51f9f-104">Hay algunas diferencias importantes entre la e/s local y la e/s de red en Windows:</span><span class="sxs-lookup"><span data-stu-id="51f9f-104">There are some notable differences between local I/O and network I/O on Windows:</span></span>

-   <span data-ttu-id="51f9f-105">La compatibilidad de e/s de red depende del redirector y del Protocolo de red.</span><span class="sxs-lookup"><span data-stu-id="51f9f-105">Network I/O support depends on the redirector and the network protocol.</span></span>
-   <span data-ttu-id="51f9f-106">El rendimiento de e/s de red depende del número de operaciones de e/s de red que se estén llevando a cabo y de la velocidad de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="51f9f-106">Network I/O performance depends on how many network I/O operations are taking place and the speed of the network connection.</span></span> <span data-ttu-id="51f9f-107">La aplicación debe ser capaz de controlar las operaciones de e/s de red con servidores que pueden ser mucho más rápidos o más lentos que el equipo local, así como cambios transitorios en la capacidad de la red.</span><span class="sxs-lookup"><span data-stu-id="51f9f-107">Your application must be able to handle network I/O operations with servers that may be much faster or slower than your local machine, as well as transient changes in network capacity.</span></span> <span data-ttu-id="51f9f-108">En estos casos, es posible que la aplicación necesite dejar más tiempo para que se complete la operación.</span><span class="sxs-lookup"><span data-stu-id="51f9f-108">In these cases, your application may need to allow more time for the operation to complete.</span></span>
-   <span data-ttu-id="51f9f-109">Las funciones que se usan para realizar la e/s de archivos locales pueden comportarse de forma diferente a través de la red.</span><span class="sxs-lookup"><span data-stu-id="51f9f-109">The functions you use to perform local file I/O may behave differently over the network.</span></span> <span data-ttu-id="51f9f-110">Por ejemplo, la operación de e/s de red que tarda mucho tiempo en completarse puede agotar el tiempo de espera. En algunas situaciones, es posible que los identificadores de archivo se queden abiertos de forma indefinida debido a esto.</span><span class="sxs-lookup"><span data-stu-id="51f9f-110">For example, a network I/O operation that takes a long time to complete may time out. In some situations, file handles may be left open indefinitely because of this.</span></span> <span data-ttu-id="51f9f-111">Otro ejemplo es que las funciones pueden devolver códigos de error de la aplicación para procesar que son específicos de la e/s de red.</span><span class="sxs-lookup"><span data-stu-id="51f9f-111">Another example is that functions may return error codes for your application to process that are specific to network I/O.</span></span>

 

 



