---
description: Para recuperar los elementos de una ruta de acceso, llame a la función PdhParseCounterPath. La función analiza los elementos de una ruta de acceso de contador y los devuelve en una \_ estructura de elementos de ruta de acceso de contador PDH \_ \_ .
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Obtener elementos de ruta de acceso de contador de una ruta de contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667317"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a><span data-ttu-id="1826e-104">Obtener elementos de ruta de acceso de contador de una ruta de contador</span><span class="sxs-lookup"><span data-stu-id="1826e-104">Obtaining Counter Path Elements from a Counter Path</span></span>

<span data-ttu-id="1826e-105">Para recuperar los elementos de una ruta de acceso, llame a la función [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) .</span><span class="sxs-lookup"><span data-stu-id="1826e-105">To retrieve the elements of a path, call the [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) function.</span></span> <span data-ttu-id="1826e-106">La función analiza los elementos de una ruta de acceso de contador y los devuelve en una estructura de [**\_ elementos de ruta de \_ acceso \_ de contador PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) .</span><span class="sxs-lookup"><span data-stu-id="1826e-106">The function parses the elements of a counter path and returns them in a [**PDH\_COUNTER\_PATH\_ELEMENTS**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) structure.</span></span>

<span data-ttu-id="1826e-107">Si tiene un nombre de instancia complejo (uno que contiene una instancia primaria e índice de instancia), puede llamar a la función [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) para extraer el nombre de instancia, el índice de instancia y el nombre principal.</span><span class="sxs-lookup"><span data-stu-id="1826e-107">If you have a complex instance name (one that contains a parent instance and instance index), you can call the [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) function to extract the instance name, instance index, and parent name.</span></span>

 

 



