---
title: Identificadores de reanudación de enumeración
description: Los identificadores de reanudación de enumeración son identificadores para la clave de reanudación real contenida en los datos de instancia de la función. Esto es necesario para la seguridad, la interoperabilidad y para simplificar el código del llamador de la función.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994257"
---
# <a name="enumeration-resume-handles"></a><span data-ttu-id="1838a-104">Identificadores de reanudación de enumeración</span><span class="sxs-lookup"><span data-stu-id="1838a-104">Enumeration Resume Handles</span></span>

<span data-ttu-id="1838a-105">Los identificadores de reanudación de enumeración son identificadores para la clave de reanudación real contenida en los datos de instancia de la función.</span><span class="sxs-lookup"><span data-stu-id="1838a-105">Enumeration resume handles are identifiers for the actual resume key contained in the instance data for the function.</span></span> <span data-ttu-id="1838a-106">Esto es necesario para la seguridad, la interoperabilidad y para simplificar el código del llamador de la función.</span><span class="sxs-lookup"><span data-stu-id="1838a-106">This is required for security, interoperability, and to simplify the caller code for the function.</span></span>

<span data-ttu-id="1838a-107">Si se pasa un **valor null** para el puntero al controlador de reanudación, no se almacena ningún identificador y no se puede continuar la búsqueda de enumeración.</span><span class="sxs-lookup"><span data-stu-id="1838a-107">If a **NULL** is passed for the pointer to the resume handle, no handle is stored and the enumeration search cannot be continued.</span></span> <span data-ttu-id="1838a-108">Esto resulta útil en los casos en los que la aplicación no desea enumerar todos los elementos.</span><span class="sxs-lookup"><span data-stu-id="1838a-108">This is useful in cases where the application does not want to enumerate all the items.</span></span>

<span data-ttu-id="1838a-109">Si se devuelve un error de una llamada de enumeración, el controlador de reanudación se debe tratar como no válido y no se puede usar para las llamadas de enumeración posteriores.</span><span class="sxs-lookup"><span data-stu-id="1838a-109">If an error is returned from an enumeration call, the resume handle must be treated as invalid and not used for any subsequent enumeration calls.</span></span> <span data-ttu-id="1838a-110">Cuando esto sucede, debe reiniciar la enumeración desde el principio.</span><span class="sxs-lookup"><span data-stu-id="1838a-110">When this occurs you must restart the enumeration from the beginning.</span></span>

 

 




