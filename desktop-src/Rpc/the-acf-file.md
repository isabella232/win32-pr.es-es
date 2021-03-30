---
title: El archivo ACF
description: El archivo ACF permite personalizar la interfaz RPC del cliente o de las aplicaciones de servidor sin que ello afecte a las características de red de la interfaz.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995584"
---
# <a name="the-acf-file"></a><span data-ttu-id="fcd1b-103">El archivo ACF</span><span class="sxs-lookup"><span data-stu-id="fcd1b-103">The ACF File</span></span>

<span data-ttu-id="fcd1b-104">El archivo ACF permite personalizar la interfaz RPC del cliente o de las aplicaciones de servidor sin que ello afecte a las características de red de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="fcd1b-104">The ACF file enables you to customize your client and/or server applications' RPC interface without affecting the network characteristics of the interface.</span></span> <span data-ttu-id="fcd1b-105">Por ejemplo, si la aplicación cliente contiene una estructura de datos compleja que solo tiene significado en el equipo local, puede especificar en el archivo ACF cómo se pueden representar los datos de esa estructura en una forma independiente del equipo para las llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="fcd1b-105">For example, if your client application contains a complex data structure that only has meaning on the local machine, you can specify in the ACF file how the data in that structure can be represented in a machine-independent form for remote procedure calls.</span></span>

<span data-ttu-id="fcd1b-106">En este tutorial se muestra otro uso del archivo ACF, que especifica el tipo de identificador de enlace que representa la conexión entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="fcd1b-106">This tutorial demonstrates another use of the ACF file—specifying the type of binding handle that represents the connection between client and server.</span></span> <span data-ttu-id="fcd1b-107">El **\[** atributo de [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) del **\]** encabezado ACF permite que la aplicación cliente seleccione un servidor para su llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="fcd1b-107">The **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]** attribute in the ACF header allows the client application to select a server for its remote procedure call.</span></span> <span data-ttu-id="fcd1b-108">ACF define el identificador para que sea del identificador de [**tipo \_ t**](/windows/desktop/Midl/handle-t) (un tipo de datos primitivo de MIDL).</span><span class="sxs-lookup"><span data-stu-id="fcd1b-108">The ACF defines the handle to be of the type [**handle\_t**](/windows/desktop/Midl/handle-t) (a MIDL primitive data type).</span></span> <span data-ttu-id="fcd1b-109">El compilador MIDL colocará el nombre del identificador de enlace que especificó ACF, Hello \_ IfHandle en el archivo de encabezado que genera.</span><span class="sxs-lookup"><span data-stu-id="fcd1b-109">The MIDL compiler will put the binding handle name that the ACF specified, hello\_IfHandle into the header file it generates.</span></span> <span data-ttu-id="fcd1b-110">Tenga en cuenta que este archivo ACF concreto tiene un cuerpo vacío.</span><span class="sxs-lookup"><span data-stu-id="fcd1b-110">Notice that this particular ACF file has an empty body.</span></span>

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

<span data-ttu-id="fcd1b-111">El compilador MIDL tiene una opción, [**/App \_ config**](/windows/desktop/Midl/-app-config), que le permite incluir determinados atributos ACF, como el **\_ identificador implícito**, en el archivo IDL, en lugar de crear un archivo ACF independiente.</span><span class="sxs-lookup"><span data-stu-id="fcd1b-111">The MIDL compiler has an option, [**/app\_config**](/windows/desktop/Midl/-app-config), that lets you include certain ACF attributes, such as **implicit\_handle**, in the IDL file, rather than creating a separate ACF file.</span></span> <span data-ttu-id="fcd1b-112">Considere la posibilidad de usar esta opción si la aplicación no requiere una gran cantidad de configuración especial y si la compatibilidad con OSF no es un problema.</span><span class="sxs-lookup"><span data-stu-id="fcd1b-112">Consider using this option if your application doesn't require a lot of special configuration and if strict OSF compatibility is not an issue.</span></span>

 

 