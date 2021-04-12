---
title: Marcas de creación de almacenamiento
description: Las marcas de creación de almacenamiento especifican qué debe hacer COM si un objeto Storage, stream o lockbytes existente tiene el mismo nombre que un nuevo objeto de almacenamiento o de secuencia que se va a crear.
ms.assetid: 5e079716-9f68-4f1d-9c76-9199e32d78ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0532e8dd817a7f442c26490cbdd37bf3cb34d0ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356738"
---
# <a name="storage-creation-flags"></a><span data-ttu-id="b0d89-103">Marcas de creación de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="b0d89-103">Storage Creation Flags</span></span>

<span data-ttu-id="b0d89-104">Las marcas de creación de almacenamiento especifican qué debe hacer COM si un objeto Storage, stream o lockbytes existente tiene el mismo nombre que un nuevo objeto de almacenamiento o de secuencia que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="b0d89-104">Storage creation flags specify what COM should do if an existing storage, stream, or lockbytes object has the same name as a new storage or stream object that you are creating.</span></span> <span data-ttu-id="b0d89-105">El valor predeterminado es devolver un mensaje de error y no crear el nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="b0d89-105">The default is to return an error message and not create the new object.</span></span> <span data-ttu-id="b0d89-106">Solo puede utilizar una de estas marcas en una llamada de creación determinada.</span><span class="sxs-lookup"><span data-stu-id="b0d89-106">You can use only one of these flags in a given creation call.</span></span>

 

 




