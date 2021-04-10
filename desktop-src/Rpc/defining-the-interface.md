---
title: Definir la interfaz
description: Una definición de interfaz es una especificación formal sobre cómo una aplicación cliente y una aplicación de servidor se comunican entre sí.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- RPC llamada a procedimiento remoto, tareas, definir la interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f447847eeca39258b96ba129c46b3f7bcf054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075405"
---
# <a name="defining-the-interface"></a><span data-ttu-id="aacae-104">Definir la interfaz</span><span class="sxs-lookup"><span data-stu-id="aacae-104">Defining the Interface</span></span>

<span data-ttu-id="aacae-105">Una definición de interfaz es una especificación formal sobre cómo una aplicación cliente y una aplicación de servidor se comunican entre sí.</span><span class="sxs-lookup"><span data-stu-id="aacae-105">An interface definition is a formal specification for how a client application and a server application communicate with each other.</span></span> <span data-ttu-id="aacae-106">La interfaz define el modo en que el cliente y el servidor se reconocen entre sí, los procedimientos remotos a los que puede llamar la aplicación cliente y los tipos de datos de los parámetros de los procedimientos y los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="aacae-106">The interface defines how the client and server recognize each other, the remote procedures that the client application can call, and the data types for those procedures' parameters and return values.</span></span> <span data-ttu-id="aacae-107">También especifica cómo se transmiten los datos entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="aacae-107">It also specifies how the data is transmitted between client and server.</span></span>

<span data-ttu-id="aacae-108">Esta interfaz se define en el Lenguaje de definición de interfaz de Microsoft (MIDL), que consta de definiciones de lenguaje C que se han ampliado con palabras clave, denominadas atributos, que describen cómo se transmiten los datos a través de la red.</span><span class="sxs-lookup"><span data-stu-id="aacae-108">You define this interface in the Microsoft Interface Definition Language (MIDL) which consists of C-language definitions augmented with keywords, called attributes, which describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="aacae-109">El archivo de definición de interfaz (IDL) contiene definiciones de tipos, atributos y prototipos de función que describen cómo se transmiten los datos en la red.</span><span class="sxs-lookup"><span data-stu-id="aacae-109">The interface definition (IDL) file contains type definitions, attributes and function prototypes that describe how data is transmitted on the network.</span></span> <span data-ttu-id="aacae-110">El archivo de configuración de la aplicación (ACF) contiene atributos que configuran la aplicación para un entorno operativo determinado sin afectar a sus características de red.</span><span class="sxs-lookup"><span data-stu-id="aacae-110">The application configuration (ACF) file contains attributes that configure your application for a particular operating environment without affecting its network characteristics.</span></span>

 

 




