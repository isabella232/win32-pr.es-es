---
description: Las acciones personalizadas de ICE se comunican llamando a MsiProcessMessage y publicando un \_ mensaje de tipo de usuario INSTALLMESSAGE.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Instrucciones de mensajes de ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4bee7dbf22184883e49da4d5a5f66f9debb577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001101"
---
# <a name="ice-message-guidelines"></a><span data-ttu-id="bb805-103">Instrucciones de mensajes de ICE</span><span class="sxs-lookup"><span data-stu-id="bb805-103">ICE Message Guidelines</span></span>

<span data-ttu-id="bb805-104">Las acciones personalizadas de ICE se comunican llamando a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) y publicando un \_ mensaje de tipo de usuario INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="bb805-104">ICE custom actions communicate by calling [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and posting an INSTALLMESSAGE\_USER type message.</span></span>

<span data-ttu-id="bb805-105">Al crear una cadena de mensaje para una acción personalizada ICE, dé formato a la cadena como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="bb805-105">When authoring a message string for an ICE custom action, format the string as follows.</span></span>

<span data-ttu-id="bb805-106">*Nombre de ICE* <tab> *Tipo* <tab> de mensaje *Descripción* <tab> de *Dirección URL o ubicación* <tab> de la ayuda *Nombre* <tab> de tabla *Nombre* <tab> de columna *Clave principal* <tab> *Clave principal* <tab> *Clave principal* .</span><span class="sxs-lookup"><span data-stu-id="bb805-106">*Name of ICE* <tab> *Message Type* <tab> *Description* <tab> *Help URL or location* <tab> *Table Name* <tab> *Column Name* <tab> *Primary Key* <tab> *Primary Key* <tab> *Primary Key* .</span></span> <span data-ttu-id="bb805-107">.</span><span class="sxs-lookup"><span data-stu-id="bb805-107">.</span></span> <span data-ttu-id="bb805-108">.</span><span class="sxs-lookup"><span data-stu-id="bb805-108">.</span></span> <span data-ttu-id="bb805-109">(se repite para tantas claves principales como sea necesario)</span><span class="sxs-lookup"><span data-stu-id="bb805-109">(repeat for as many primary keys as needed)</span></span>

<span data-ttu-id="bb805-110">Los tres primeros campos de la cadena son obligatorios en todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="bb805-110">The first three fields of the string are required in every message.</span></span>

<span data-ttu-id="bb805-111">El campo tipo de mensaje especifica si el ICE informa de un error, un error, una advertencia o un mensaje informativo.</span><span class="sxs-lookup"><span data-stu-id="bb805-111">The Message Type field specifies whether the ICE reports a Failure, Error, Warning, or Informational message.</span></span>



| <span data-ttu-id="bb805-112">Value</span><span class="sxs-lookup"><span data-stu-id="bb805-112">Value</span></span> | <span data-ttu-id="bb805-113">Tipo de mensaje</span><span class="sxs-lookup"><span data-stu-id="bb805-113">Message type</span></span>                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb805-114">0</span><span class="sxs-lookup"><span data-stu-id="bb805-114">0</span></span>     | <span data-ttu-id="bb805-115">Mensaje de error que informa del error de la acción personalizada ICE.</span><span class="sxs-lookup"><span data-stu-id="bb805-115">Failure message reporting the failure of the ICE custom action.</span></span>                                                                                                       |
| <span data-ttu-id="bb805-116">1</span><span class="sxs-lookup"><span data-stu-id="bb805-116">1</span></span>     | <span data-ttu-id="bb805-117">Mensaje de error de creación de base de datos que provoca un comportamiento incorrecto.</span><span class="sxs-lookup"><span data-stu-id="bb805-117">Error message reporting database authoring that cause incorrect behavior.</span></span>                                                                                             |
| <span data-ttu-id="bb805-118">2</span><span class="sxs-lookup"><span data-stu-id="bb805-118">2</span></span>     | <span data-ttu-id="bb805-119">Mensaje de advertencia que informa de la creación de bases de datos que provoca un comportamiento incorrecto en ciertos casos.</span><span class="sxs-lookup"><span data-stu-id="bb805-119">Warning message reporting database authoring that causes incorrect behavior in certain cases.</span></span> <span data-ttu-id="bb805-120">Las advertencias también pueden notificar efectos secundarios inesperados de la creación de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="bb805-120">Warnings can also report unexpected side-effects of database authoring.</span></span> |
| <span data-ttu-id="bb805-121">3</span><span class="sxs-lookup"><span data-stu-id="bb805-121">3</span></span>     | <span data-ttu-id="bb805-122">Mensaje informativo.</span><span class="sxs-lookup"><span data-stu-id="bb805-122">Informational message.</span></span>                                                                                                                                                |



 

<span data-ttu-id="bb805-123">Si la ayuda no está disponible, el campo dirección URL de ayuda puede ser la cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="bb805-123">If help is not available, the Help URL field may be the empty string.</span></span>

<span data-ttu-id="bb805-124">Los mensajes de error y de advertencia deben proporcionar el nombre de tabla, el nombre de columna y los campos de clave principal.</span><span class="sxs-lookup"><span data-stu-id="bb805-124">Error and Warning messages should provide the Table Name, Column Name, and Primary Key fields.</span></span> <span data-ttu-id="bb805-125">Si se omite alguno de estos campos, todos los campos que siguen al primer campo en blanco deben quedar fuera del mensaje.</span><span class="sxs-lookup"><span data-stu-id="bb805-125">If any of these fields are omitted, all of the fields following the first blank field must be left out of the message.</span></span> <span data-ttu-id="bb805-126">Por ejemplo, se proporciona un nombre de tabla sin un nombre de columna y claves principales o un nombre de tabla, y se proporciona un nombre de columna sin claves principales.</span><span class="sxs-lookup"><span data-stu-id="bb805-126">For example, a table name is provided without a column name and primary keys or a table name and a column name is provided with no primary keys.</span></span> <span data-ttu-id="bb805-127">Sin embargo, un nombre de columna y las claves principales no se pueden usar sin un nombre de tabla.</span><span class="sxs-lookup"><span data-stu-id="bb805-127">However a column name and primary keys cannot be used without a table name.</span></span> <span data-ttu-id="bb805-128">Es posible que se muestren varias claves principales hasta que se hayan dado valores a todas las claves principales de la tabla.</span><span class="sxs-lookup"><span data-stu-id="bb805-128">Multiple primary keys may be listed until all the primary keys in that table have been given values.</span></span>

## <a name="examples"></a><span data-ttu-id="bb805-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bb805-129">Examples</span></span>

<span data-ttu-id="bb805-130">El primer mensaje que se muestra [en la ICE de ejemplo en C++](sample-ice-in-c-.md):</span><span class="sxs-lookup"><span data-stu-id="bb805-130">The first message illustrated by the [Sample ICE in C++](sample-ice-in-c-.md):</span></span>

<span data-ttu-id="bb805-131">"ICE01 \\ T3 \\ Tse ha creado 04/29/1998 by <Insertar aquí el nombre del autor>".</span><span class="sxs-lookup"><span data-stu-id="bb805-131">"ICE01\\t3\\tCreated 04/29/1998 by <insert author's name here>."</span></span>

<span data-ttu-id="bb805-132">El segundo mensaje publicado por el ICE de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bb805-132">The second message posted by the sample ICE:</span></span>

<span data-ttu-id="bb805-133">"ICE01 \\ T3 \\ tLast modificó 05/06/1999 por <Insertar aquí el nombre del autor>".</span><span class="sxs-lookup"><span data-stu-id="bb805-133">"ICE01\\t3\\tLast modified 05/06/1999 by <insert author's name here>."</span></span>

<span data-ttu-id="bb805-134">El tercer mensaje publicado por el ICE de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bb805-134">The third message posted by the sample ICE.</span></span>

<span data-ttu-id="bb805-135">"ICE01 \\ T3 \\ tSimple ICE para ilustrar el concepto de hielo".</span><span class="sxs-lookup"><span data-stu-id="bb805-135">"ICE01\\t3\\tSimple ICE to illustrating the ICE concept".</span></span>

 

 



