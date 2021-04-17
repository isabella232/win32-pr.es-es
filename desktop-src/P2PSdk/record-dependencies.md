---
description: La infraestructura del mismo nivel no garantiza el orden de recepción y procesamiento de registros.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Dependencias de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667384"
---
# <a name="record-dependencies"></a><span data-ttu-id="ff27d-103">Dependencias de registro</span><span class="sxs-lookup"><span data-stu-id="ff27d-103">Record Dependencies</span></span>

<span data-ttu-id="ff27d-104">La infraestructura del mismo nivel no garantiza el orden de recepción y procesamiento de registros.</span><span class="sxs-lookup"><span data-stu-id="ff27d-104">The Peer Infrastructure does not guarantee the order for receiving and processing records.</span></span> <span data-ttu-id="ff27d-105">Si la aplicación tiene dependencias de registros, lo que significa que el procesamiento o la validación de un registro se basa en otro registro, la aplicación debe ser capaz de controlar las situaciones en las que los registros se pueden recibir en un orden arbitrario e impredecible.</span><span class="sxs-lookup"><span data-stu-id="ff27d-105">If your application has record dependencies, which means that the processing or validation of one record relies on another record, then your application must be able to handle situations when records might be received in an arbitrary and unpredictable order.</span></span> <span data-ttu-id="ff27d-106">Por ejemplo, una aplicación de chat puede tener dos tipos de registros: un registro que contiene información acerca de un usuario específico y un registro que contiene un mensaje de chat que hace referencia al registro del usuario.</span><span class="sxs-lookup"><span data-stu-id="ff27d-106">For example, a chat application may have two types of records: a record that contains information about a specific user, and a record that contains a chat message that refers to the user record.</span></span>

<span data-ttu-id="ff27d-107">Una aplicación debe ser capaz de controlar la situación cuando se recibe un registro de mensaje de chat antes del registro del usuario para el mensaje de chat.</span><span class="sxs-lookup"><span data-stu-id="ff27d-107">An application must be able to handle the situation when a chat message record is received before the user record for the chat message.</span></span> <span data-ttu-id="ff27d-108">Una manera de controlar la situación es esperar el registro de usuario mediante una lista en **espera**, o una caché y un temporizador.</span><span class="sxs-lookup"><span data-stu-id="ff27d-108">One way to handle the situation is to wait for the user record by using a **stand-by list**, or a cache and timer.</span></span> <span data-ttu-id="ff27d-109">La aplicación puede examinar periódicamente cada registro de la lista o la memoria caché y, a continuación, controlar la situación en que se recibe el registro de usuario necesario.</span><span class="sxs-lookup"><span data-stu-id="ff27d-109">The application can periodically examine each record in the list or cache, and then handle the situation when the required user record is received.</span></span>

<span data-ttu-id="ff27d-110">Para controlar las dependencias de registro, una aplicación bien diseñada consta de lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ff27d-110">To handle record dependencies, a well-designed application consists of the following:</span></span>

-   <span data-ttu-id="ff27d-111">Comprueba siempre las dependencias del registro antes de realizar una acción.</span><span class="sxs-lookup"><span data-stu-id="ff27d-111">Always checks for record dependencies before performing an action.</span></span>
-   <span data-ttu-id="ff27d-112">Prevé las condiciones que pueden producirse cuando los registros se reciben en un orden inesperado y, a continuación, controla la situación.</span><span class="sxs-lookup"><span data-stu-id="ff27d-112">Anticipates conditions that might occur when records are received in an unexpected order, and then handles the situation.</span></span>

 

 



