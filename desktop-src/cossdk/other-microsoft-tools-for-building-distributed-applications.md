---
description: Otras herramientas de Microsoft para compilar aplicaciones distribuidas
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Otras herramientas de Microsoft para compilar aplicaciones distribuidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714868"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a><span data-ttu-id="3e368-103">Otras herramientas de Microsoft para compilar aplicaciones distribuidas</span><span class="sxs-lookup"><span data-stu-id="3e368-103">Other Microsoft Tools for Building Distributed Applications</span></span>

<span data-ttu-id="3e368-104">Además de las herramientas de COM+, Microsoft proporciona las siguientes herramientas para ayudar al desarrollador a crear aplicaciones distribuidas:</span><span class="sxs-lookup"><span data-stu-id="3e368-104">In addition to the tools in COM+, Microsoft provides the following tools to assist the developer in creating distributed applications:</span></span>

-   <span data-ttu-id="3e368-105">Microsoft Data Access Components (MDAC).</span><span class="sxs-lookup"><span data-stu-id="3e368-105">Microsoft Data Access Components (MDAC).</span></span> <span data-ttu-id="3e368-106">Microsoft proporciona varias vías para recuperar datos de una gran cantidad de orígenes.</span><span class="sxs-lookup"><span data-stu-id="3e368-106">Microsoft provides several avenues for retrieving data from a myriad of sources.</span></span> <span data-ttu-id="3e368-107">Por ejemplo, OLE DB ofrece un conjunto de interfaces COM para compilar componentes de base de datos.</span><span class="sxs-lookup"><span data-stu-id="3e368-107">For example, OLE DB offers a set of COM interfaces for building database components.</span></span> <span data-ttu-id="3e368-108">Las interfaces se definen para que los proveedores de datos puedan implementar distintos niveles de compatibilidad, en función de las capacidades del almacén de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="3e368-108">The interfaces are defined so that data providers can implement different levels of support, based on the capabilities of the underlying data store.</span></span> <span data-ttu-id="3e368-109">Dado que OLE DB se basa en COM, se puede extender fácilmente y las extensiones se implementan como interfaces nuevas.</span><span class="sxs-lookup"><span data-stu-id="3e368-109">Because OLE DB is COM-based, it can easily be extended, and extensions are implemented as new interfaces.</span></span> <span data-ttu-id="3e368-110">OLE DB también incluye una interfaz de programación de nivel de aplicación, denominada Objetos de datos ActiveX (ADO).</span><span class="sxs-lookup"><span data-stu-id="3e368-110">OLE DB also includes an application-level programming interface, called ActiveX Data Objects (ADO).</span></span> <span data-ttu-id="3e368-111">ADO expone interfaces duales, por lo que se puede usar fácilmente desde lenguajes de scripting, así como Microsoft Visual C++, Visual Basic y otras herramientas de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="3e368-111">ADO exposes dual interfaces, so it can easily be used from scripting languages as well as Microsoft Visual C++, Visual Basic, and other developer tools.</span></span>

    > [!Note]  
    > <span data-ttu-id="3e368-112">Los desarrolladores también pueden optar por usar una API genérica, independiente del proveedor, como la interfaz de programación de aplicaciones (API) de Microsoft Open Database Connectivity (ODBC).</span><span class="sxs-lookup"><span data-stu-id="3e368-112">Developers can also choose to use a generic, vendor-neutral API such as the Microsoft Open Database Connectivity (ODBC) application programming interface (API).</span></span> <span data-ttu-id="3e368-113">La API de ODBC es una interfaz de lenguaje C para tener acceso a los datos de un DBMS mediante Lenguaje de consulta estructurado (SQL).</span><span class="sxs-lookup"><span data-stu-id="3e368-113">The ODBC API is a C language interface for accessing data in a DBMS by using Structured Query Language (SQL).</span></span> <span data-ttu-id="3e368-114">Un administrador de controladores ODBC proporciona la interfaz de programación y los componentes en tiempo de ejecución para localizar controladores específicos del DBMS.</span><span class="sxs-lookup"><span data-stu-id="3e368-114">An ODBC driver manager provides the programming interface and run-time components to locate DBMS-specific drivers.</span></span> <span data-ttu-id="3e368-115">Los controladores ODBC, normalmente suministrados por el proveedor de DBMS, traducen las llamadas genéricas del administrador de controladores ODBC en llamadas al método de acceso a datos nativo.</span><span class="sxs-lookup"><span data-stu-id="3e368-115">ODBC drivers, typically supplied by the DBMS vendor, translate generic calls from the ODBC driver manager into calls to the native data access method.</span></span> <span data-ttu-id="3e368-116">La principal ventaja de utilizar la API de ODBC es que necesita aprender solo una API para tener acceso a una amplia gama de DBMS.</span><span class="sxs-lookup"><span data-stu-id="3e368-116">The primary advantage of using the ODBC API is that you need to learn only one API to access a wide range of DBMSs.</span></span>

     

-   <span data-ttu-id="3e368-117">Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3e368-117">Microsoft SQL Server.</span></span> <span data-ttu-id="3e368-118">Además de proporcionar un sistema de base de datos relacional sólido y Eloquent, Microsoft SQL Server puede proporcionar una aplicación distribuida con agrupación de conexiones y seguridad que pueda integrarse con el modelo de seguridad de Windows.</span><span class="sxs-lookup"><span data-stu-id="3e368-118">In addition to providing a robust and eloquent relational database system, Microsoft SQL Server can provide a distributed application with connection pooling and security that can integrate with the Windows security model.</span></span>

-   <span data-ttu-id="3e368-119">Integración de transacciones COM (COMTI).</span><span class="sxs-lookup"><span data-stu-id="3e368-119">COM Transaction Integration (COMTI).</span></span> <span data-ttu-id="3e368-120">COMTI se puede usar para integrar sistemas de gran sistema en sistemas Windows, incluidas las aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="3e368-120">COMTI can be used to integrate mainframe systems into Windows systems, including COM+ applications.</span></span> <span data-ttu-id="3e368-121">COMTI usa protocolos de comunicación estándar (por ejemplo, LU 6,2) para la comunicación entre equipos Windows y mainframe y minicomputers.</span><span class="sxs-lookup"><span data-stu-id="3e368-121">COMTI uses standard communication protocols (for example, LU 6.2) for communicating between Windows computers and mainframe and minicomputers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e368-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3e368-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e368-123">Hipótesis y principios de diseño de COM+</span><span class="sxs-lookup"><span data-stu-id="3e368-123">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="3e368-124">Diseñar la aplicación COM+ mediante UML</span><span class="sxs-lookup"><span data-stu-id="3e368-124">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="3e368-125">Sugerencias de diseño generales para el uso de COM+</span><span class="sxs-lookup"><span data-stu-id="3e368-125">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="3e368-126">Optimizar interacciones con el nivel de lógica de negocios de COM+</span><span class="sxs-lookup"><span data-stu-id="3e368-126">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



