---
description: No se pueden crear instancias de las clases modificadas en el espacio de nombres localizado. Las clases modificadas en el espacio de nombres localizado se tratan como si fueran abstractas, aunque no contienen el calificador abstracto.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Consideraciones de la clase modificada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279622"
---
# <a name="amended-class-considerations"></a><span data-ttu-id="0c6ba-104">Consideraciones de la clase modificada</span><span class="sxs-lookup"><span data-stu-id="0c6ba-104">Amended Class Considerations</span></span>

<span data-ttu-id="0c6ba-105">No se pueden crear instancias de las clases modificadas en el espacio de nombres localizado.</span><span class="sxs-lookup"><span data-stu-id="0c6ba-105">You cannot create instances of the amended classes in the localized namespace.</span></span> <span data-ttu-id="0c6ba-106">Las clases modificadas en el espacio de nombres localizado se tratan como si fueran abstractas, aunque no contienen el calificador [**abstracto**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="0c6ba-106">Amended classes in the localized namespace are treated as if they are abstract although they do not contain the [**Abstract**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="0c6ba-107">Si recupera una clase modificada de un espacio de nombres localizado mediante la marca WBEM \_ \_ usar el indicador de \_ \_ calificadores modificados y genera una instancia a partir de ella, la instancia contiene todos los calificadores modificados de la clase modificada.</span><span class="sxs-lookup"><span data-stu-id="0c6ba-107">If you retrieve an amended class from a localized namespace using the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag and spawn an instance from it, the instance contains all of the amended qualifiers of the amended class.</span></span> <span data-ttu-id="0c6ba-108">No se puede almacenar esta nueva clase en el espacio de nombres que contiene la definición de clase básica a menos que realice la operación **Put** con la marca WBEM \_ use la marca de \_ \_ \_ calificadores modificados.</span><span class="sxs-lookup"><span data-stu-id="0c6ba-108">You cannot store this new class in the namespace that contains the basic class definition unless you perform the **put** operation with the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span> <span data-ttu-id="0c6ba-109">Esta marca indica a WMI que elimine todos los calificadores modificados antes de guardar el objeto.</span><span class="sxs-lookup"><span data-stu-id="0c6ba-109">This flag instructs WMI to strip away any amended qualifiers before saving the object.</span></span> <span data-ttu-id="0c6ba-110">Si no especifica \_ la marca WBEM \_ usar \_ \_ calificadores modificados, se produce un error en la operación **Put** con un \_ error de objeto modificado por WBEM E \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0c6ba-110">If you do not specify WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS, the **put** operation fails with a WBEM\_E\_AMENDED\_OBJECT error.</span></span>

 

 



