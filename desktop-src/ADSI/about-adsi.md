---
title: Acerca de las interfaces de servicio Active Directory
description: Active Directory interfaces de servicio (ADSI) abstrae las capacidades de los servicios de directorio de diferentes proveedores de red de un entorno informático distribuido para presentar un único conjunto de interfaces de servicios de directorio para administrar los recursos de red.
ms.assetid: 6d601af5-7470-42c2-b99e-21174ea008b1
ms.tgt_platform: multiple
keywords:
- Acerca de las interfaces de servicio Active Directory ADSI
- ADSI ADSI, acerca de
- Interfaces de servicio Active Directory ADSI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc083b33a633335da12915257fcddff1174a6858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148745"
---
# <a name="about-active-directory-service-interfaces"></a><span data-ttu-id="a1181-106">Acerca de las interfaces de servicio Active Directory</span><span class="sxs-lookup"><span data-stu-id="a1181-106">About Active Directory Service Interfaces</span></span>

<span data-ttu-id="a1181-107">Active Directory interfaces de servicio (ADSI) abstrae las capacidades de los servicios de directorio de diferentes proveedores de red de un entorno informático distribuido para presentar un único conjunto de interfaces de servicios de directorio para administrar los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="a1181-107">Active Directory Service Interfaces (ADSI) abstracts the capabilities of directory services from different network providers in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="a1181-108">Los administradores y programadores pueden usar los servicios ADSI para enumerar y administrar los recursos de un servicio de directorio, independientemente del entorno de red que contenga el recurso.</span><span class="sxs-lookup"><span data-stu-id="a1181-108">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="a1181-109">ADSI facilita la realización de tareas administrativas comunes, como agregar nuevos usuarios, administrar impresoras y buscar recursos en todo el entorno informático distribuido.</span><span class="sxs-lookup"><span data-stu-id="a1181-109">ADSI makes it easier to perform common administrative tasks, such as adding new users, managing printers, and locating resources throughout the distributed computing environment.</span></span>

<span data-ttu-id="a1181-110">ADSI facilita a los desarrolladores "habilitar en el directorio" sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a1181-110">ADSI makes it easy for developers to "directory enable" their applications.</span></span> <span data-ttu-id="a1181-111">Los administradores y desarrolladores administran un único conjunto de interfaces de servicios de directorio, independientemente de los servicios de directorio que estén instalados.</span><span class="sxs-lookup"><span data-stu-id="a1181-111">Administrators and developers handle a single set of directory service interfaces, regardless of which directory services are installed.</span></span>

<span data-ttu-id="a1181-112">En esta introducción se describen los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a1181-112">The following topics are discussed in this introduction:</span></span>

-   [<span data-ttu-id="a1181-113">Varios servicios de directorio</span><span class="sxs-lookup"><span data-stu-id="a1181-113">Multiple Directory Services</span></span>](multiple-directory-services.md)
-   [<span data-ttu-id="a1181-114">¿Quién usará Active Directory interfaces de servicio?</span><span class="sxs-lookup"><span data-stu-id="a1181-114">Who Will Use Active Directory Service Interfaces?</span></span>](who-will-use-active-directory-service-interfaces.md)
-   [<span data-ttu-id="a1181-115">Servicios de directorio hoy</span><span class="sxs-lookup"><span data-stu-id="a1181-115">Directory Services Today</span></span>](directory-services-today.md)
-   [<span data-ttu-id="a1181-116">Ventajas del uso de interfaces de servicio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="a1181-116">Benefits of Using Active Directory Service Interfaces</span></span>](benefits-of-using-active-directory-service-interfaces.md)
-   [<span data-ttu-id="a1181-117">Arquitectura de interfaces de servicio Active Directory</span><span class="sxs-lookup"><span data-stu-id="a1181-117">Active Directory Service Interfaces Architecture</span></span>](active-directory-service-interfaces-architecture.md)
-   [<span data-ttu-id="a1181-118">Compatibilidad con el lenguaje de programación</span><span class="sxs-lookup"><span data-stu-id="a1181-118">Programming Language Support</span></span>](programming-language-support.md)
-   [<span data-ttu-id="a1181-119">Propiedades y atributos ADSI</span><span class="sxs-lookup"><span data-stu-id="a1181-119">ADSI Properties and Attributes</span></span>](adsi-properties-and-attributes.md)

## <a name="what-you-should-know-before-reading-this-guide"></a><span data-ttu-id="a1181-120">Qué debe saber antes de leer esta guía</span><span class="sxs-lookup"><span data-stu-id="a1181-120">What You Should Know Before Reading This Guide</span></span>

<span data-ttu-id="a1181-121">En esta guía se da por supuesto que está familiarizado con el modelo de objetos componentes (COM) y la automatización, y que ya sabe cómo programar en Visual Basic o en C/C++.</span><span class="sxs-lookup"><span data-stu-id="a1181-121">This guide assumes that you are familiar with the Component Object Model (COM) and Automation, and that you know how to program in either Visual Basic or C/C++.</span></span>

<span data-ttu-id="a1181-122">Algunos de los términos que se usan en esta guía son únicos en ADSI o en el entorno de servicios de directorio.</span><span class="sxs-lookup"><span data-stu-id="a1181-122">Some of the terms used in this guide are unique to either ADSI or the directory services environment.</span></span> <span data-ttu-id="a1181-123">Otros términos resultarán familiares, pero pueden tener significados ligeramente diferentes en estos entornos.</span><span class="sxs-lookup"><span data-stu-id="a1181-123">Other terms will be familiar but may have slightly different meanings in these environments.</span></span>

## <a name="further-reading-about-adsi-and-related-topics"></a><span data-ttu-id="a1181-124">Más información acerca de ADSI y temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1181-124">Further Reading about ADSI and Related Topics</span></span>

<span data-ttu-id="a1181-125">Para obtener más información acerca de las interfaces de servicio de Active Directory y las tecnologías en las que se basan, puede que le resulten útiles los siguientes orígenes.</span><span class="sxs-lookup"><span data-stu-id="a1181-125">For more information about Active Directory Service Interfaces and the technologies on which they are based, you may find the following sources helpful.</span></span>

<span data-ttu-id="a1181-126">Brockschmidt, Kraig.</span><span class="sxs-lookup"><span data-stu-id="a1181-126">Brockschmidt, Kraig.</span></span> <span data-ttu-id="a1181-127">*Inside OLE*, 2ª edición.</span><span class="sxs-lookup"><span data-stu-id="a1181-127">*Inside OLE*, 2nd edition.</span></span> <span data-ttu-id="a1181-128">Redmond, WA: Microsoft Press, 1995.</span><span class="sxs-lookup"><span data-stu-id="a1181-128">Redmond, WA: Microsoft Press, 1995.</span></span>

<span data-ttu-id="a1181-129">Chappell, David.</span><span class="sxs-lookup"><span data-stu-id="a1181-129">Chappell, David.</span></span> <span data-ttu-id="a1181-130">*Descripción de ActiveX y OLE*.</span><span class="sxs-lookup"><span data-stu-id="a1181-130">*Understanding ActiveX and OLE*.</span></span> <span data-ttu-id="a1181-131">Redmond, WA: Microsoft Press, 1996.</span><span class="sxs-lookup"><span data-stu-id="a1181-131">Redmond, WA: Microsoft Press, 1996.</span></span>

<span data-ttu-id="a1181-132">Hahn, Steven.</span><span class="sxs-lookup"><span data-stu-id="a1181-132">Hahn, Steven.</span></span> <span data-ttu-id="a1181-133">*Referencia del programador ASP de ADSI*.</span><span class="sxs-lookup"><span data-stu-id="a1181-133">*ADSI ASP Programmer's Reference*.</span></span> <span data-ttu-id="a1181-134">Wrox Press Ltd., 1998.</span><span class="sxs-lookup"><span data-stu-id="a1181-134">Wrox Press Ltd., 1998.</span></span>

<span data-ttu-id="a1181-135">Harrison, Richard.</span><span class="sxs-lookup"><span data-stu-id="a1181-135">Harrison, Richard.</span></span> <span data-ttu-id="a1181-136">*Asp/mts/seguridad Web de ADSI*.</span><span class="sxs-lookup"><span data-stu-id="a1181-136">*ASP/MTS/ADSI Web Security*.</span></span> <span data-ttu-id="a1181-137">Prentice Hall, 1999.</span><span class="sxs-lookup"><span data-stu-id="a1181-137">Prentice Hall, 1999.</span></span>

<span data-ttu-id="a1181-138">La versión 1,0, 1996, de referencia del programador de OLE DB de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a1181-138">Microsoft's OLE DB Programmer's Reference Version 1.0, 1996.</span></span>

<span data-ttu-id="a1181-139">*Referencia del programador de OLE 2, volumen dos*.</span><span class="sxs-lookup"><span data-stu-id="a1181-139">*OLE 2 Programmer's Reference, Volume Two*.</span></span> <span data-ttu-id="a1181-140">Redmond, WA: Microsoft Press, 1994.</span><span class="sxs-lookup"><span data-stu-id="a1181-140">Redmond, WA: Microsoft Press, 1994.</span></span>

<span data-ttu-id="a1181-141">Rogerson, Dale.</span><span class="sxs-lookup"><span data-stu-id="a1181-141">Rogerson, Dale.</span></span> <span data-ttu-id="a1181-142">*Dentro de com*.</span><span class="sxs-lookup"><span data-stu-id="a1181-142">*Inside COM*.</span></span> <span data-ttu-id="a1181-143">Redmond, WA: Microsoft Press, 1997.</span><span class="sxs-lookup"><span data-stu-id="a1181-143">Redmond, WA: Microsoft Press, 1997.</span></span>

<span data-ttu-id="a1181-144">*La especificación de diseño de servicio Active Directory versión 2,0*.</span><span class="sxs-lookup"><span data-stu-id="a1181-144">*The Active Directory Service Design Specification Version 2.0*.</span></span>

<span data-ttu-id="a1181-145">*Especificación del modelo de objetos componentes*.</span><span class="sxs-lookup"><span data-stu-id="a1181-145">*The Component Object Model Specification*.</span></span>

<span data-ttu-id="a1181-146">(Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones).</span><span class="sxs-lookup"><span data-stu-id="a1181-146">(These resources may not be available in some languages and countries/regions.)</span></span>

 

 




