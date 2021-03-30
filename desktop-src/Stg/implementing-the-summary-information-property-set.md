---
title: Implementar el conjunto de propiedades de información de Resumen
description: Hay directrices que se deben seguir al implementar un conjunto de propiedades de información de resumen para el almacenamiento estructurado.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementar el conjunto de propiedades de información de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772835"
---
# <a name="implementing-the-summary-information-property-set"></a><span data-ttu-id="4e920-104">Implementar el conjunto de propiedades de información de Resumen</span><span class="sxs-lookup"><span data-stu-id="4e920-104">Implementing the Summary Information Property Set</span></span>

<span data-ttu-id="4e920-105">Hay directrices que se deben seguir al implementar un conjunto de propiedades de información de resumen para el almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="4e920-105">There are guidelines to follow when implementing a summary information property set for Structured Storage.</span></span>

<span data-ttu-id="4e920-106">A continuación se indican las instrucciones para implementar [el conjunto de propiedades de información de Resumen](the-summary-information-property-set.md):</span><span class="sxs-lookup"><span data-stu-id="4e920-106">The following are the guidelines for implementing [The Summary Information Property Set](the-summary-information-property-set.md):</span></span>

-   <span data-ttu-id="4e920-107">**PID \_ de La plantilla** hace referencia a un documento externo que contiene información de formato y estilo.</span><span class="sxs-lookup"><span data-stu-id="4e920-107">**PID\_TEMPLATE** refers to an external document containing format and style information.</span></span> <span data-ttu-id="4e920-108">El proceso por el que se encuentra la plantilla está definido por la implementación.</span><span class="sxs-lookup"><span data-stu-id="4e920-108">The process by which the template is located is implementation-defined.</span></span>
-   <span data-ttu-id="4e920-109">**PID \_ de LASTAUTHOR** es el nombre almacenado en la información del usuario por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e920-109">**PID\_LASTAUTHOR** is the name stored in User Information by the application.</span></span> <span data-ttu-id="4e920-110">Por ejemplo, Mary crea un documento en su equipo y lo asigna a John, que luego lo modifica y lo guarda.</span><span class="sxs-lookup"><span data-stu-id="4e920-110">For example, Mary creates a document on her computer and gives it to John, who then modifies and saves it.</span></span> <span data-ttu-id="4e920-111">Mary es el autor, Juan es el último valor guardado por.</span><span class="sxs-lookup"><span data-stu-id="4e920-111">Mary is the author, John is the last saved by value.</span></span>
-   <span data-ttu-id="4e920-112">**PID \_ de REVNUMBER** es el número de veces que se ha llamado al comando File/Save en este documento.</span><span class="sxs-lookup"><span data-stu-id="4e920-112">**PID\_REVNUMBER** is the number of times the File/Save command has been called on this document.</span></span>
-   <span data-ttu-id="4e920-113">Cada uno de los valores de fecha y hora debe almacenarse en la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="4e920-113">Each of the date/time values must be stored in Universal Coordinated Time (UTC).</span></span>
-   <span data-ttu-id="4e920-114">**PID \_ de CREATE \_ DTM** es una propiedad de solo lectura; Esta propiedad debe establecerse cuando se crea un documento, pero no debe cambiarse posteriormente.</span><span class="sxs-lookup"><span data-stu-id="4e920-114">**PID\_CREATE\_DTM** is a read-only property; this property should be set when a document is created, but should not be subsequently changed.</span></span>
-   <span data-ttu-id="4e920-115">En **la \_ miniatura de PID**, las aplicaciones deben almacenar datos en formato **CF \_ DIB** o **CF \_ METAFILEPICT** .</span><span class="sxs-lookup"><span data-stu-id="4e920-115">For **PID\_THUMBNAIL**, applications should store data in **CF\_DIB** or **CF\_METAFILEPICT** format.</span></span> <span data-ttu-id="4e920-116">**CF \_** Se recomienda METAFILEPICT.</span><span class="sxs-lookup"><span data-stu-id="4e920-116">**CF\_METAFILEPICT** is recommended.</span></span>
-   <span data-ttu-id="4e920-117">**PID \_ de La seguridad** es el nivel de seguridad sugerido para el documento.</span><span class="sxs-lookup"><span data-stu-id="4e920-117">**PID\_SECURITY** is the suggested security level for the document.</span></span> <span data-ttu-id="4e920-118">Al anotar el nivel de seguridad del documento, una aplicación que no sea el autor del documento puede ajustar su interfaz de usuario a las propiedades.</span><span class="sxs-lookup"><span data-stu-id="4e920-118">By noting the security level on the document, an application other than the originator of the document can adjust its user interface to the properties.</span></span> <span data-ttu-id="4e920-119">Una aplicación no debe mostrar ninguna información sobre un documento protegido mediante contraseña ni permitir modificaciones en los documentos Read-Only o bloqueados para anotaciones.</span><span class="sxs-lookup"><span data-stu-id="4e920-119">An application should not display any information about a password-protected document or enable modifications to enforced Read-Only or Locked-for-Annotations documents.</span></span> <span data-ttu-id="4e920-120">Si el usuario intenta modificar propiedades, la aplicación debería advertir al usuario sobre el estado recomendado Read-Only.</span><span class="sxs-lookup"><span data-stu-id="4e920-120">If the user attempts to modify properties, the application should warn the user about the Read-Only Recommended status.</span></span>



| <span data-ttu-id="4e920-121">Nivel de seguridad</span><span class="sxs-lookup"><span data-stu-id="4e920-121">Security level</span></span>         | <span data-ttu-id="4e920-122">Value</span><span class="sxs-lookup"><span data-stu-id="4e920-122">Value</span></span> |
|------------------------|-------|
| <span data-ttu-id="4e920-123">None</span><span class="sxs-lookup"><span data-stu-id="4e920-123">None</span></span>                   | <span data-ttu-id="4e920-124">0</span><span class="sxs-lookup"><span data-stu-id="4e920-124">0</span></span>     |
| <span data-ttu-id="4e920-125">Contraseña protegida</span><span class="sxs-lookup"><span data-stu-id="4e920-125">Password protected</span></span>     | <span data-ttu-id="4e920-126">1</span><span class="sxs-lookup"><span data-stu-id="4e920-126">1</span></span>     |
| <span data-ttu-id="4e920-127">Recomendado solo lectura</span><span class="sxs-lookup"><span data-stu-id="4e920-127">Read-only recommended</span></span>  | <span data-ttu-id="4e920-128">2</span><span class="sxs-lookup"><span data-stu-id="4e920-128">2</span></span>     |
| <span data-ttu-id="4e920-129">Solo lectura forzada</span><span class="sxs-lookup"><span data-stu-id="4e920-129">Read-only enforced</span></span>     | <span data-ttu-id="4e920-130">4</span><span class="sxs-lookup"><span data-stu-id="4e920-130">4</span></span>     |
| <span data-ttu-id="4e920-131">Bloqueado para anotaciones</span><span class="sxs-lookup"><span data-stu-id="4e920-131">Locked for annotations</span></span> | <span data-ttu-id="4e920-132">8</span><span class="sxs-lookup"><span data-stu-id="4e920-132">8</span></span>     |



 

 

 




