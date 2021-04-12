---
title: El archivo IDL
description: El archivo IDL está formado por una o varias definiciones de interfaz, cada una de las cuales tiene un encabezado y un cuerpo.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487810"
---
# <a name="the-idl-file"></a><span data-ttu-id="79d5f-103">El archivo IDL</span><span class="sxs-lookup"><span data-stu-id="79d5f-103">The IDL File</span></span>

<span data-ttu-id="79d5f-104">El archivo IDL está formado por una o varias definiciones de interfaz, cada una de las cuales tiene un encabezado y un cuerpo.</span><span class="sxs-lookup"><span data-stu-id="79d5f-104">The IDL file consists of one or more interface definitions, each of which has a header and a body.</span></span> <span data-ttu-id="79d5f-105">El encabezado contiene información que se aplica a toda la interfaz, como el UUID.</span><span class="sxs-lookup"><span data-stu-id="79d5f-105">The header contains information that applies to the entire interface, such as the UUID.</span></span> <span data-ttu-id="79d5f-106">Esta información se incluye entre corchetes y va seguida de la **interfaz** de palabra clave y el nombre de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="79d5f-106">This information is enclosed in square brackets and is followed by the keyword **interface** and the interface name.</span></span> <span data-ttu-id="79d5f-107">El cuerpo contiene definiciones de tipos de datos y prototipos de función de estilo C, ampliados con atributos que describen cómo se transmiten los datos a través de la red.</span><span class="sxs-lookup"><span data-stu-id="79d5f-107">The body contains C-style data type definitions and function prototypes, augmented with attributes that describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="79d5f-108">En este ejemplo, el encabezado de interfaz contiene solo el UUID y el número de versión.</span><span class="sxs-lookup"><span data-stu-id="79d5f-108">In this example, the interface header contains only the UUID and the version number.</span></span> <span data-ttu-id="79d5f-109">El número de versión garantiza que cuando hay varias versiones de una interfaz RPC, solo se conectarán las versiones compatibles del cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="79d5f-109">The version number ensures that when there are multiple versions of an RPC interface, only compatible versions of the client and server will be connected.</span></span>

<span data-ttu-id="79d5f-110">El cuerpo de la interfaz contiene el prototipo de función para **HelloProc**.</span><span class="sxs-lookup"><span data-stu-id="79d5f-110">The interface body contains the function prototype for **HelloProc**.</span></span> <span data-ttu-id="79d5f-111">En este prototipo, el parámetro de función pszString tiene los atributos **\[** [**in**](/windows/desktop/Midl/in) **\]** y **\[** [**String**](/windows/desktop/Midl/string) **\]** .</span><span class="sxs-lookup"><span data-stu-id="79d5f-111">In this prototype, the function parameter pszString has the attributes **\[**[**in**](/windows/desktop/Midl/in)**\]** and **\[**[**string**](/windows/desktop/Midl/string)**\]**.</span></span> <span data-ttu-id="79d5f-112">El atributo in indica a la biblioteca **\[ en \]** tiempo de ejecución que el parámetro solo se pasa desde el cliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="79d5f-112">The **\[in\]** attribute tells the run-time library that the parameter is passed only from the client to the server.</span></span> <span data-ttu-id="79d5f-113">El atributo de **\[ cadena \]** especifica que el código auxiliar debe tratar el parámetro como una cadena de caracteres de estilo C.</span><span class="sxs-lookup"><span data-stu-id="79d5f-113">The **\[string\]** attribute specifies that the stub should treat the parameter as a C-style character string.</span></span>

<span data-ttu-id="79d5f-114">La aplicación cliente debe poder cerrar la aplicación de servidor, por lo que la interfaz contiene un prototipo para otra función remota,**Shutdown** , que se implementará más adelante en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="79d5f-114">The client application should be able to shut down the server application, so the interface contains a prototype for another remote function,**Shutdown** , that will be implemented later in this tutorial.</span></span>

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 