---
title: Acerca de DDEML
description: En este tema se describe el intercambio dinámico de datos.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Interfaz de usuario de Windows, Intercambio dinámico de datos (DDE)
- Intercambio dinámico de datos (DDE), acerca de
- DDE (Intercambio dinámico de datos), acerca de
- intercambio de datos, Intercambio dinámico de datos (DDE)
- Interfaz de usuario de Windows, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), acerca de
- DDEML (biblioteca de administración de Intercambio dinámico de datos), acerca de
- intercambio de datos, biblioteca de administración de Intercambio dinámico de datos (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532470"
---
# <a name="about-the-ddeml"></a><span data-ttu-id="87f75-111">Acerca de DDEML</span><span class="sxs-lookup"><span data-stu-id="87f75-111">About the DDEML</span></span>

<span data-ttu-id="87f75-112">Intercambio dinámico de datos (DDE) difiere del mecanismo de transferencia de datos del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="87f75-112">Dynamic Data Exchange (DDE) differs from the clipboard data-transfer mechanism.</span></span> <span data-ttu-id="87f75-113">Una diferencia es que el portapapeles se usa casi siempre como una respuesta única a una acción específica del usuario, por ejemplo, al hacer clic en **pegar** en un menú.</span><span class="sxs-lookup"><span data-stu-id="87f75-113">One difference is that the clipboard is almost always used as a one-time response to a specific action by the user — such as clicking **Paste** from a menu.</span></span> <span data-ttu-id="87f75-114">Aunque el DDE también puede ser iniciado por un usuario, normalmente continúa sin la implicación adicional del usuario.</span><span class="sxs-lookup"><span data-stu-id="87f75-114">Although DDE can also be initiated by a user, it typically continues without the user's further involvement.</span></span>

<span data-ttu-id="87f75-115">La biblioteca de administración de Intercambio dinámico de datos (DDEML) proporciona una interfaz que simplifica la tarea de agregar funcionalidad DDE a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="87f75-115">The Dynamic Data Exchange Management Library (DDEML) provides an interface that simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="87f75-116">En lugar de enviar, publicar y procesar directamente los mensajes DDE, una aplicación usa las funciones proporcionadas por DDEML para administrar las conversaciones DDE.</span><span class="sxs-lookup"><span data-stu-id="87f75-116">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="87f75-117">Una conversación DDE es la interacción entre las aplicaciones cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="87f75-117">A DDE conversation is the interaction between client and server applications.</span></span> <span data-ttu-id="87f75-118">El método DDEML también proporciona un medio para administrar las cadenas y los datos compartidos entre las aplicaciones DDE.</span><span class="sxs-lookup"><span data-stu-id="87f75-118">The DDEML also provides a means for managing the strings and data shared among DDE applications.</span></span> <span data-ttu-id="87f75-119">En lugar de utilizar átomos y punteros a objetos de memoria compartida, las aplicaciones DDE crean e intercambian los identificadores de cadena, que identifican cadenas, y los identificadores de datos, que identifican objetos DDE.</span><span class="sxs-lookup"><span data-stu-id="87f75-119">Instead of using atoms and pointers to shared memory objects, DDE applications create and exchange string handles, which identify strings, and data handles, which identify DDE objects.</span></span> <span data-ttu-id="87f75-120">DDEML proporciona una función ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) que permite a una aplicación de servidor registrar los nombres de servicio que admite.</span><span class="sxs-lookup"><span data-stu-id="87f75-120">The DDEML provides a function ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) that enables a server application to register the service names it supports.</span></span> <span data-ttu-id="87f75-121">Los nombres de servicio se difunden a otras aplicaciones del sistema, que usan los nombres para conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="87f75-121">The service names are then broadcast to other applications in the system, which use the names to connect to the server.</span></span> <span data-ttu-id="87f75-122">El DDEML también garantiza la compatibilidad entre las aplicaciones DDE, ya que exige que implementen el protocolo DDE de una manera coherente.</span><span class="sxs-lookup"><span data-stu-id="87f75-122">The DDEML also ensures compatibility among DDE applications by requiring them to implement the DDE protocol in a consistent manner.</span></span>

<span data-ttu-id="87f75-123">Las aplicaciones existentes que utilizan el protocolo DDE basado en mensajes son totalmente compatibles con las que usan DDEML; es decir, una aplicación que utilice DDE basado en mensajes puede establecer conversaciones y realizar transacciones con aplicaciones mediante DDEML.</span><span class="sxs-lookup"><span data-stu-id="87f75-123">Existing applications using the message-based DDE protocol are fully compatible with those that use the DDEML; that is, an application using message-based DDE can establish conversations and perform transactions with applications using the DDEML.</span></span> <span data-ttu-id="87f75-124">En lugar de usar mensajes DDE en la nueva aplicación, aproveche las ventajas de DDEML y las muchas mejoras que ofrece.</span><span class="sxs-lookup"><span data-stu-id="87f75-124">Instead of using DDE messages in your new application, take advantage of the DDEML and the many improvements it offers.</span></span>

<span data-ttu-id="87f75-125">Para usar DDEML, debe incluir DDEML. H archivo de encabezado en los archivos de código fuente, vincular con USER32. Archivo LIB y asegúrese de que el archivo de DDEML.DLL reside en la ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="87f75-125">To use the DDEML, you must include the DDEML.H header file in your source files, link with the USER32.LIB file, and ensure that the DDEML.DLL file resides in the system's path.</span></span>

<span data-ttu-id="87f75-126">Siempre que se produce un error en una función DDEML, una aplicación puede llamar a la función [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) para determinar la causa del error.</span><span class="sxs-lookup"><span data-stu-id="87f75-126">Whenever a DDEML function fails, an application can call the [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) function to determine the cause of the failure.</span></span> <span data-ttu-id="87f75-127">**DdeGetLastError** devuelve un valor de error que especifica la causa del error más reciente.</span><span class="sxs-lookup"><span data-stu-id="87f75-127">**DdeGetLastError** returns an error value that specifies the cause of the most recent error.</span></span>

 

 




