---
title: Serialización de interfaces
description: Serialización de interfaces
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705031"
---
# <a name="interface-marshaling"></a><span data-ttu-id="ef96d-103">Serialización de interfaces</span><span class="sxs-lookup"><span data-stu-id="ef96d-103">Interface Marshaling</span></span>

<span data-ttu-id="ef96d-104">A menos que sepa más allá de la duda de que la interfaz nunca se usará en los límites de apartamento, subproceso o proceso, debe decidir cómo proporcionar compatibilidad de serialización para las interfaces.</span><span class="sxs-lookup"><span data-stu-id="ef96d-104">Unless you know beyond all doubt that your interface will never be used across apartment, thread, or process boundaries, you need to decide how to provide marshaling support for your interfaces.</span></span> <span data-ttu-id="ef96d-105">Hay tres maneras de proporcionar compatibilidad con el cálculo de referencias:</span><span class="sxs-lookup"><span data-stu-id="ef96d-105">There are three ways to provide marshaling support:</span></span>

-   <span data-ttu-id="ef96d-106">Escriba su propio código de proxy o código auxiliar que llama al canal COM, que a su vez llama a las bibliotecas en tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="ef96d-106">Write your own proxy/stub code that calls the COM channel, which in turn calls the RPC run-time libraries.</span></span> <span data-ttu-id="ef96d-107">Teóricamente, es posible hacer esto, pero en la práctica es casi imposible hacerlo sin una cantidad significativa de esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="ef96d-107">Theoretically, it is possible to do this, but in practice it is almost impossible to do without a significant amount of effort.</span></span>
-   <span data-ttu-id="ef96d-108">Describa las interfaces en un archivo de lenguaje de definición de interfaz (IDL) y use el compilador MIDL para generar un archivo DLL de proxy/código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="ef96d-108">Describe your interfaces in an interface definition language (IDL) file and use the MIDL compiler to generate a proxy/stub DLL.</span></span> <span data-ttu-id="ef96d-109">Este método proporciona el mejor rendimiento y la mayor flexibilidad en términos de tipos de datos aceptables.</span><span class="sxs-lookup"><span data-stu-id="ef96d-109">This method provides the best performance and the most flexibility in terms of acceptable data types.</span></span> <span data-ttu-id="ef96d-110">Mediante el uso de código auxiliar de proxy generado por MIDL, puede controlar no solo la administración de memoria, sino también la serialización y la desserialización de tipos de datos complejos en distintas plataformas.</span><span class="sxs-lookup"><span data-stu-id="ef96d-110">Using MIDL-generated proxy stubs, you can control not only memory management but even the marshaling and unmarshaling of complex data types across different platforms.</span></span>
-   <span data-ttu-id="ef96d-111">Use MIDL para generar una biblioteca de tipos que el sistema utiliza para proporcionar compatibilidad de serialización en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ef96d-111">Use MIDL to generate a type library that the system uses to provide marshaling support at run time.</span></span> <span data-ttu-id="ef96d-112">Esta es la manera más sencilla de implementar la compatibilidad con el cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="ef96d-112">This is the easiest way to implement marshaling support.</span></span> <span data-ttu-id="ef96d-113">Todo lo que tiene que hacer es generar una biblioteca de tipos y registrarla.</span><span class="sxs-lookup"><span data-stu-id="ef96d-113">All you have to do is generate a type library and register it.</span></span> <span data-ttu-id="ef96d-114">Las interfaces deben ser compatibles con la automatización (ya sea [**oleautomation**](/windows/desktop/Midl/oleautomation) o [**dual**](/windows/desktop/Midl/dual)), lo que establece algunas restricciones en los tipos de datos que se pueden usar como parámetros de método.</span><span class="sxs-lookup"><span data-stu-id="ef96d-114">Your interfaces must be Automation-compatible (either [**oleautomation**](/windows/desktop/Midl/oleautomation) or [**dual**](/windows/desktop/Midl/dual)), which places some restrictions on the kinds of data types you can use as method parameters.</span></span> <span data-ttu-id="ef96d-115">Sin embargo, en la mayoría de los casos, la ventaja de tener las interfaces accesibles para los programas escritos en otros lenguajes, como Microsoft Visual Basic y Java, supera las limitaciones en los tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="ef96d-115">However, in most cases, the advantage of having your interfaces accessible to programs written in other languages, such as Microsoft Visual Basic and Java, outweighs the limitations on data types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef96d-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef96d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef96d-117">Comunicación entre objetos</span><span class="sxs-lookup"><span data-stu-id="ef96d-117">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> </dl>

 

 