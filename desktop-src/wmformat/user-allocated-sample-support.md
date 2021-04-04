---
title: Compatibilidad de ejemplo asignada por el usuario
description: Compatibilidad de ejemplo asignada por el usuario
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- SDK de Windows Media Format, compatibilidad de ejemplo asignada por el usuario
- Advanced Systems Format (ASF), compatibilidad de ejemplo asignada por el usuario
- ASF (formato de sistemas avanzados), compatibilidad de ejemplo asignada por el usuario
- compatibilidad de ejemplo asignada por el usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075481"
---
# <a name="user-allocated-sample-support"></a><span data-ttu-id="890cb-107">Compatibilidad de ejemplo asignada por el usuario</span><span class="sxs-lookup"><span data-stu-id="890cb-107">User Allocated Sample Support</span></span>

<span data-ttu-id="890cb-108">En circunstancias normales, tanto el objeto lector como el objeto lector sincrónico crean un nuevo objeto de búfer para cada ejemplo entregado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="890cb-108">Under normal circumstances, both the reader object and the synchronous reader object create a new buffer object for each sample delivered to your application.</span></span> <span data-ttu-id="890cb-109">Esto se debe a que el objeto de lectura no tiene forma de saber lo que hace la aplicación con los ejemplos después de que los obtiene.</span><span class="sxs-lookup"><span data-stu-id="890cb-109">This is because the reading object has no way of knowing what your application does with the samples after it gets them.</span></span> <span data-ttu-id="890cb-110">Aunque muchas aplicaciones leen ejemplos solo para representarlas inmediatamente, es posible que algunas aplicaciones necesiten mantener muestras durante mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="890cb-110">Even though many applications read samples only to render them immediately, some applications may need to maintain samples for a long time.</span></span> <span data-ttu-id="890cb-111">El objeto de lectura no puede, por consiguiente, volver a usar ninguno de los búferes que asigna; los entrega a la aplicación, que, a su vez, tiene el control sobre ellas.</span><span class="sxs-lookup"><span data-stu-id="890cb-111">The reading object cannot, therefore, reuse any of the buffers it allocates; it delivers them to your application, which then has control over them.</span></span>

<span data-ttu-id="890cb-112">El problema de este enfoque es que un archivo puede contener un gran número de muestras.</span><span class="sxs-lookup"><span data-stu-id="890cb-112">The problem with this approach is that a file can contain an immense number of samples.</span></span> <span data-ttu-id="890cb-113">Si cada uno de ellos requiere la creación de un nuevo objeto de búfer, se desperdicia mucho tiempo de procesador asignando y liberando memoria.</span><span class="sxs-lookup"><span data-stu-id="890cb-113">If each one of them requires a new buffer object to be created, a lot of processor time is wasted allocating and releasing memory.</span></span> <span data-ttu-id="890cb-114">En aplicaciones dependientes del tiempo, como reproductores multimedia, esta sobrecarga puede ser muy perjudicial para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="890cb-114">In time-sensitive applications such as media players, this overhead can be very detrimental to performance.</span></span>

<span data-ttu-id="890cb-115">Para mitigar los problemas de rendimiento de las muestras asignadas por el lector, tanto el lector como el lector sincrónico admiten ejemplos asignados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="890cb-115">To alleviate the performance issues of reader-allocated samples, both the reader and the synchronous reader support user-allocated samples.</span></span> <span data-ttu-id="890cb-116">Para usar ejemplos asignados por la aplicación, el objeto de lectura realiza llamadas a un método de devolución de llamada de asignación de ejemplo que se implementa.</span><span class="sxs-lookup"><span data-stu-id="890cb-116">To use samples allocated by your application, the reading object makes calls to a sample allocation callback method that you implement.</span></span> <span data-ttu-id="890cb-117">La lógica usada por la devolución de llamada para enviar búferes al objeto de lectura es totalmente suya.</span><span class="sxs-lookup"><span data-stu-id="890cb-117">The logic used by the callback to deliver buffers to the reading object is entirely up to you.</span></span> <span data-ttu-id="890cb-118">Puede usar un grupo de búferes para todo el archivo o usar varios grupos de búferes, uno para cada salida o flujo, o cualquier otro esquema que funcione para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="890cb-118">You can use a pool of buffers for the entire file or use multiple pools of buffers, one for each output or stream, or any other scheme that works for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="890cb-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="890cb-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="890cb-120">**Asignar búferes para la lectura de archivos**</span><span class="sxs-lookup"><span data-stu-id="890cb-120">**Allocating Buffers for File Reading**</span></span>](allocating-buffers-for-file-reading.md)
</dt> <dt>

[<span data-ttu-id="890cb-121">**Características de lectura de archivos**</span><span class="sxs-lookup"><span data-stu-id="890cb-121">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




