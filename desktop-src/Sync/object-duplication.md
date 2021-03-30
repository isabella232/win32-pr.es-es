---
description: La función DuplicateHandle crea un identificador duplicado que se puede usar en otro proceso especificado.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Duplicación de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f8e0948ce55f5d25d7567346ecdec97f04b24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082984"
---
# <a name="object-duplication"></a><span data-ttu-id="b7ea9-103">Duplicación de objetos</span><span class="sxs-lookup"><span data-stu-id="b7ea9-103">Object Duplication</span></span>

<span data-ttu-id="b7ea9-104">La función [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) crea un identificador duplicado que se puede usar en otro proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="b7ea9-104">The [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function creates a duplicate handle that can be used by another specified process.</span></span> <span data-ttu-id="b7ea9-105">Este método de compartir identificadores de objetos es más complejo que el uso de objetos con nombre o herencia.</span><span class="sxs-lookup"><span data-stu-id="b7ea9-105">This method of sharing object handles is more complex than using named objects or inheritance.</span></span> <span data-ttu-id="b7ea9-106">Requiere la comunicación entre el proceso de creación y el proceso en el que se duplica el controlador.</span><span class="sxs-lookup"><span data-stu-id="b7ea9-106">It requires communication between the creating process and the process into which the handle is duplicated.</span></span> <span data-ttu-id="b7ea9-107">La información necesaria (el identificador de proceso y el valor de identificador) se puede comunicar mediante cualquiera de los métodos de comunicación entre procesos, como canalizaciones con nombre o memoria compartida con nombre.</span><span class="sxs-lookup"><span data-stu-id="b7ea9-107">The necessary information (the handle value and process identifier) can be communicated by any of the interprocess communication methods, such as named pipes or named shared memory.</span></span>

 

 
