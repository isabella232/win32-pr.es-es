---
title: Qué debe hacer la instalación
description: El OID debe hacer referencia a los nuevos atributos a los que se hace referencia en el paso 3 porque el nombre del nuevo atributo no está presente en la caché de esquema en este momento.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Qué debe hacer la instalación de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993883"
---
# <a name="what-the-installation-must-do"></a><span data-ttu-id="fc21b-104">Qué debe hacer la instalación</span><span class="sxs-lookup"><span data-stu-id="fc21b-104">What the Installation Must Do</span></span>

<span data-ttu-id="fc21b-105">Las aplicaciones que extienden el esquema deben aplicar las actualizaciones tal y como se describe en el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="fc21b-105">Applications that extend the schema, must apply updates as described in the following procedure.</span></span>

<span data-ttu-id="fc21b-106">**Para aplicar actualizaciones al extender el esquema**</span><span class="sxs-lookup"><span data-stu-id="fc21b-106">**To apply updates when extending the schema**</span></span>

1.  <span data-ttu-id="fc21b-107">Agregue los nuevos atributos.</span><span class="sxs-lookup"><span data-stu-id="fc21b-107">Add the new attributes.</span></span>
2.  <span data-ttu-id="fc21b-108">Agregue las nuevas clases.</span><span class="sxs-lookup"><span data-stu-id="fc21b-108">Add the new classes.</span></span>
3.  <span data-ttu-id="fc21b-109">Agregue los nuevos atributos a las clases.</span><span class="sxs-lookup"><span data-stu-id="fc21b-109">Add the new attributes to classes.</span></span>
4.  <span data-ttu-id="fc21b-110">Desencadenar una recarga de caché.</span><span class="sxs-lookup"><span data-stu-id="fc21b-110">Trigger a cache reload.</span></span>

<span data-ttu-id="fc21b-111">El OID debe hacer referencia a los nuevos atributos a los que se hace referencia en el paso 3 porque el nombre del nuevo atributo no está presente en la caché de esquema en este momento.</span><span class="sxs-lookup"><span data-stu-id="fc21b-111">New attributes referenced in Step 3 must be referred to by its OID because the new attribute name is not present in the schema cache at this point.</span></span>

<span data-ttu-id="fc21b-112">El paso 4 no es necesario si las extensiones no se van a usar inmediatamente; las extensiones aparecerán en la caché de esquema en unos 5 minutos, en función de la carga del sistema.</span><span class="sxs-lookup"><span data-stu-id="fc21b-112">Step 4 is unnecessary if the extensions will not be used immediately; the extensions will appear in the schema cache in approximately 5 minutes, depending on system load.</span></span> <span data-ttu-id="fc21b-113">Para obtener más información acerca de la caché de esquema y cómo desencadenar una recarga de caché, vea [actualizar la caché de esquema](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="fc21b-113">For more information about the schema cache and how to trigger a cache reload, see [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>

 

 




