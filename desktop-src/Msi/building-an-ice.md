---
description: Si no puede encontrar los evaluadores de coherencia internos que necesita entre las acciones personalizadas de ICE existentes enumeradas en la referencia de ICE, tendrá que preparar su propia ICE para validar el paquete.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Creación de un ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667010"
---
# <a name="building-an-ice"></a><span data-ttu-id="0d071-103">Creación de un ICE</span><span class="sxs-lookup"><span data-stu-id="0d071-103">Building An ICE</span></span>

<span data-ttu-id="0d071-104">Si no puede encontrar los [evaluadores de coherencia internos](internal-consistency-evaluators-ices.md) que necesita entre las acciones personalizadas de ICE existentes enumeradas en la [referencia de ICE](ice-reference.md), tendrá que preparar su propia ICE para validar el paquete.</span><span class="sxs-lookup"><span data-stu-id="0d071-104">If you are unable to find the [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) you need among the existing ICE custom actions listed in the [ICE Reference](ice-reference.md), you will need to prepare your own ICE to validate your package.</span></span>

<span data-ttu-id="0d071-105">Al crear acciones personalizadas de ICE, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0d071-105">When authoring ICE custom actions you should do the following:</span></span>

-   <span data-ttu-id="0d071-106">Basar el ICEs solo en acciones personalizadas de los tipos que aparecen en la tabla mostrada.</span><span class="sxs-lookup"><span data-stu-id="0d071-106">Base the ICEs only on custom actions of types listed in the table shown.</span></span>
-   <span data-ttu-id="0d071-107">Llame a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) y publique un \_ tipo de usuario de INSTALLMESSAGE de mensaje.</span><span class="sxs-lookup"><span data-stu-id="0d071-107">Call [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and post an INSTALLMESSAGE\_USER type of message.</span></span> <span data-ttu-id="0d071-108">Al crear los mensajes ICE, siga el formato del mensaje en las [instrucciones del mensaje de ICE](ice-message-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="0d071-108">When authoring your ICE messages follow the message format in the [ICE Message Guidelines](ice-message-guidelines.md).</span></span>
-   <span data-ttu-id="0d071-109">Escriba el ICE de modo que capture cualquier error de API y siempre devuelva el ERROR \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="0d071-109">Write your ICE such that it captures any API errors and always returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="0d071-110">Esto es necesario para permitir que se ejecuten las acciones personalizadas posteriores después del error de un ICE.</span><span class="sxs-lookup"><span data-stu-id="0d071-110">This is necessary to allow subsequent custom actions to run following the failure of an ICE.</span></span>

<span data-ttu-id="0d071-111">Las acciones personalizadas de ICE se limitan a los siguientes tipos de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="0d071-111">ICE custom actions are limited to the following custom action types.</span></span>



| <span data-ttu-id="0d071-112">Tipo de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="0d071-112">Custom action type</span></span>                                 | <span data-ttu-id="0d071-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d071-113">Description</span></span>               |
|----------------------------------------------------|---------------------------|
| [<span data-ttu-id="0d071-114">Tipo de acción personalizada 1</span><span class="sxs-lookup"><span data-stu-id="0d071-114">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="0d071-115">DLL en secuencia binaria</span><span class="sxs-lookup"><span data-stu-id="0d071-115">DLL in binary stream</span></span>      |
| [<span data-ttu-id="0d071-116">Tipo de acción personalizada 2</span><span class="sxs-lookup"><span data-stu-id="0d071-116">Custom Action Type 2</span></span>](custom-action-type-2.md)   | <span data-ttu-id="0d071-117">EXE en una secuencia binaria</span><span class="sxs-lookup"><span data-stu-id="0d071-117">EXE in binary stream</span></span>      |
| [<span data-ttu-id="0d071-118">Tipo de acción personalizada 5</span><span class="sxs-lookup"><span data-stu-id="0d071-118">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="0d071-119">JScript en secuencia binaria</span><span class="sxs-lookup"><span data-stu-id="0d071-119">JScript in binary stream</span></span>  |
| [<span data-ttu-id="0d071-120">Tipo de acción personalizada 6</span><span class="sxs-lookup"><span data-stu-id="0d071-120">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="0d071-121">VBScript en una secuencia binaria</span><span class="sxs-lookup"><span data-stu-id="0d071-121">VBScript in binary stream</span></span> |
| [<span data-ttu-id="0d071-122">Tipo de acción personalizada 37</span><span class="sxs-lookup"><span data-stu-id="0d071-122">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="0d071-123">Código JScript como cadena</span><span class="sxs-lookup"><span data-stu-id="0d071-123">JScript code as string</span></span>    |
| [<span data-ttu-id="0d071-124">Tipo de acción personalizada 38</span><span class="sxs-lookup"><span data-stu-id="0d071-124">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="0d071-125">Código VBScript como cadena</span><span class="sxs-lookup"><span data-stu-id="0d071-125">VBScript code as string</span></span>   |



 

<span data-ttu-id="0d071-126">Al crear una acción personalizada ICE, no haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="0d071-126">When authoring an ICE custom action, do not do the following:</span></span>

-   <span data-ttu-id="0d071-127">No asuma que el identificador del motor que recibe el ICE es una instancia de instalación de la base de datos del instalador.</span><span class="sxs-lookup"><span data-stu-id="0d071-127">Do not assume that the handle to the engine that the ICE receives is an installation instance of the installer database.</span></span> <span data-ttu-id="0d071-128">Si no es una instancia de instalación, no se han definido determinadas propiedades, no se resuelven los directorios de origen y de destino, y no se definen los Estados de las características actuales.</span><span class="sxs-lookup"><span data-stu-id="0d071-128">If it is not a installation instance, certain properties are not defined, the source and target directories are not resolved, and current feature states are not defined.</span></span>
-   <span data-ttu-id="0d071-129">No confíe en la ejecución anterior, o no en la ejecución, de cualquier acción del instalador, acción personalizada u otro ICE.</span><span class="sxs-lookup"><span data-stu-id="0d071-129">Do not rely on the prior execution, or non-execution, of any installer action, custom action, or another ICE.</span></span> <span data-ttu-id="0d071-130">Dado que una ICE anterior puede haber creado columnas temporales en una tabla, los autores deben hacer referencia a las columnas por nombre siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="0d071-130">Because a prior ICE may have created temporary columns in any table, authors should reference columns by name whenever possible.</span></span> <span data-ttu-id="0d071-131">ICEs debe limpiar las columnas o tablas temporales antes de salir.</span><span class="sxs-lookup"><span data-stu-id="0d071-131">ICEs should cleanup any temporary columns or tables before they exit.</span></span>
-   <span data-ttu-id="0d071-132">No asuma que los autores tienen acceso a una imagen del directorio de origen de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0d071-132">Do not assume that authors have access to an image of the source directory of the database.</span></span>
-   <span data-ttu-id="0d071-133">No asuma que los cambios realizados en la base de datos no se conservan.</span><span class="sxs-lookup"><span data-stu-id="0d071-133">Do not assume that changes made to the database do not persist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d071-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d071-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d071-135">ICE de ejemplo en C++</span><span class="sxs-lookup"><span data-stu-id="0d071-135">Sample ICE in C++</span></span>](sample-ice-in-c-.md)
</dt> <dt>

[<span data-ttu-id="0d071-136">ICE de ejemplo en VBScript</span><span class="sxs-lookup"><span data-stu-id="0d071-136">Sample ICE in VBScript</span></span>](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



