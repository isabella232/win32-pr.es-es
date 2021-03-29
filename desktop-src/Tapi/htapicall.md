---
description: El tipo de datos HTAPICALL representa el identificador opaco de TAPI para una estructura de datos de llamada.
ms.assetid: a2a17b03-5779-411e-8959-6e2de5e53c5a
title: HTAPICALL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abd90dc8453be5f5bec18e92b384b7ace830d14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360455"
---
# <a name="htapicall"></a><span data-ttu-id="19987-103">HTAPICALL</span><span class="sxs-lookup"><span data-stu-id="19987-103">HTAPICALL</span></span>

<span data-ttu-id="19987-104">El tipo de datos **HTAPICALL** representa el identificador opaco de TAPI para una estructura de datos de llamada.</span><span class="sxs-lookup"><span data-stu-id="19987-104">The **HTAPICALL** datatype represents the TAPI opaque handle for a call data structure.</span></span> <span data-ttu-id="19987-105">TAPI debe resolver un valor de este tipo en una referencia a la instancia de la estructura de datos adecuada.</span><span class="sxs-lookup"><span data-stu-id="19987-105">TAPI must resolve a value of this type into a reference to the appropriate data structure instance.</span></span> <span data-ttu-id="19987-106">El proveedor de servicios no debe intentar hacer referencia a través de este como si fuera un puntero, realizar suposiciones sobre sus valores o interpretar su representación de forma que no sea pasar su valor a TAPI en los momentos adecuados.</span><span class="sxs-lookup"><span data-stu-id="19987-106">The service provider must not attempt to reference through this as if it were a pointer, make assumptions about its values, or interpret its representation in any way other than passing its value to TAPI at appropriate times.</span></span>

 

 



