---
title: GUID de coherencia
description: Los GUID de coherencia son una estrategia de detección que permite a una aplicación detectar actualizaciones parciales.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075016"
---
# <a name="consistency-guids"></a><span data-ttu-id="37254-103">GUID de coherencia</span><span class="sxs-lookup"><span data-stu-id="37254-103">Consistency GUIDs</span></span>

<span data-ttu-id="37254-104">Los GUID de coherencia son una estrategia de detección que permite a una aplicación detectar actualizaciones parciales.</span><span class="sxs-lookup"><span data-stu-id="37254-104">Consistency GUIDs are a detection strategy that allows an application to detect partial updates.</span></span> <span data-ttu-id="37254-105">Se aplica un GUID de coherencia (identificador único global) a cada objeto de un conjunto relacionado.</span><span class="sxs-lookup"><span data-stu-id="37254-105">A consistency GUID (Globally Unique IDentifier) is applied to each object in a related set.</span></span> <span data-ttu-id="37254-106">En la implementación, una aplicación de origen genera un nuevo GUID y lo aplica a cada objeto que actualiza en el conjunto de objetos relacionados.</span><span class="sxs-lookup"><span data-stu-id="37254-106">In implementation, a source application generates a new GUID and applies it to each object it updates in the set of related objects.</span></span> <span data-ttu-id="37254-107">A continuación, aplica el nuevo GUID al resto de los objetos del conjunto y finaliza aplicando el nuevo GUID al objeto "Master".</span><span class="sxs-lookup"><span data-stu-id="37254-107">It then applies the new GUID to the rest of the objects in the set, and finishes by applying the new GUID to the "master" object.</span></span> <span data-ttu-id="37254-108">Normalmente, el objeto "Master" será un contenedor que sea el primario de los demás objetos del conjunto.</span><span class="sxs-lookup"><span data-stu-id="37254-108">Typically, the "master" object will be a container that is the parent of the other objects in the set.</span></span>

<span data-ttu-id="37254-109">Algunas consideraciones importantes:</span><span class="sxs-lookup"><span data-stu-id="37254-109">Some important considerations:</span></span>

-   <span data-ttu-id="37254-110">Los GUID de coherencia combinados con recuentos de objetos o sumas de comprobación son más efectivos que los GUID de coherencia solos, ya que es posible que la aplicación que lee los objetos no sepa Cuántos objetos tienen el GUID debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="37254-110">Consistency GUIDs combined with object counts or checksums are more effective than consistency GUIDs alone, because the application reading the objects may not know how many objects with the GUID should be present.</span></span>
-   <span data-ttu-id="37254-111">Las aplicaciones deben generar sus propios GUID (una API de Microsoft Win32, UuidCreate, proporciona esta función) y no usar los GUID generados por el sistema que se encuentran en el atributo **objectGUID** de un objeto.</span><span class="sxs-lookup"><span data-stu-id="37254-111">Applications must generate their own GUIDs (a Microsoft Win32 API, UuidCreate, provides this function), and not use the system-generated GUIDs found in an object's **objectGUID** attribute.</span></span> <span data-ttu-id="37254-112">Esto se debe a que un GUID de coherencia debe cambiar cada vez que se actualiza el conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="37254-112">This is because a consistency GUID needs to change each time the set of objects is updated.</span></span> <span data-ttu-id="37254-113">Los GUID de identidad de objeto encontrados en **objectGUID** nunca cambian una vez creado el objeto.</span><span class="sxs-lookup"><span data-stu-id="37254-113">Object identity GUIDs found in **objectGUID** never change after the object has been created.</span></span>
-   <span data-ttu-id="37254-114">Los GUID de coherencia suponen que ningún objeto se comparte entre conjuntos, por lo que cada conjunto puede tener un GUID de coherencia único.</span><span class="sxs-lookup"><span data-stu-id="37254-114">Consistency GUIDs assume that no object is shared among sets, so each set can have a unique consistency GUID.</span></span>

 

 




