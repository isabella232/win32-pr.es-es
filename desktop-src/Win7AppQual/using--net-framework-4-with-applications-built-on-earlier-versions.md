---
description: Usar .NET Framework 4 con aplicaciones creadas en versiones anteriores
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Usar .NET Framework 4 con aplicaciones creadas en versiones anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30eb8f4be1c50904b8d5760f456f3fe20bdd3da
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314948"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a><span data-ttu-id="76c9d-103">Usar .NET Framework 4 con aplicaciones creadas en versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="76c9d-103">Using .NET Framework 4 with Applications Built on Earlier Versions</span></span>

## <a name="platform"></a><span data-ttu-id="76c9d-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="76c9d-104">Platform</span></span>

 <span data-ttu-id="76c9d-105">**Clientes** : Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="76c9d-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="76c9d-106">**Servidores** : windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76c9d-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="76c9d-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="76c9d-107">Feature Impact</span></span>

 <span data-ttu-id="76c9d-108">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="76c9d-108">**Severity** - Low</span></span>  
<span data-ttu-id="76c9d-109">**Frecuencia** : alta</span><span class="sxs-lookup"><span data-stu-id="76c9d-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="76c9d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="76c9d-110">Description</span></span>

<span data-ttu-id="76c9d-111">El .NET Framework 4 es muy compatible con las aplicaciones compiladas con versiones anteriores de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="76c9d-111">The .NET Framework 4 is highly compatible with applications that are built by using earlier .NET Framework versions.</span></span> <span data-ttu-id="76c9d-112">Los principales cambios en .NET Framework 4 son para mejorar la seguridad, el cumplimiento de estándares, la corrección, la confiabilidad y el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="76c9d-112">The primary changes in .NET Framework 4 are to improve security, standards compliance, correctness, reliability, and performance.</span></span>

<span data-ttu-id="76c9d-113">Sin embargo, .NET Framework 4 no utiliza automáticamente su versión de Common Language Runtime (CLR) para ejecutar aplicaciones compiladas con versiones anteriores de la .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="76c9d-113">However, .NET Framework 4 does not automatically use its version of the common language runtime (CLR) to run applications that are built by using earlier versions of the .NET Framework.</span></span>

## <a name="manifestation"></a><span data-ttu-id="76c9d-114">Manifestación</span><span class="sxs-lookup"><span data-stu-id="76c9d-114">Manifestation</span></span>

<span data-ttu-id="76c9d-115">Si ha creado una aplicación con una .NET Framework anterior y un usuario abre la aplicación en un equipo que tiene .NET Framework 4 y la versión anterior del .NET Framework instalado, la aplicación usa la versión anterior de CLR.</span><span class="sxs-lookup"><span data-stu-id="76c9d-115">If you built an application by using an earlier .NET Framework and a user opens that application on a computer that has both .NET Framework 4 and the earlier version of the .NET Framework installed, the application uses the earlier CLR version.</span></span>

<span data-ttu-id="76c9d-116">Sin embargo, si el .NET Framework 4 es la única versión en tiempo de ejecución instalada en el equipo, la aplicación produce una excepción y pide al usuario que instale la versión de tiempo de ejecución con la que compiló la aplicación.</span><span class="sxs-lookup"><span data-stu-id="76c9d-116">However, if the .NET Framework 4 is the only runtime version that is installed on the computer, the application throws an exception and asks the user to install the runtime version that you built the application against.</span></span>

## <a name="solution"></a><span data-ttu-id="76c9d-117">Solución</span><span class="sxs-lookup"><span data-stu-id="76c9d-117">Solution</span></span>

<span data-ttu-id="76c9d-118">Para ejecutar aplicaciones que se compilan con versiones anteriores de .NET Framework con .NET Framework 4, debe compilar la aplicación para que tenga como destino la versión de .NET Framework 4 Si la especifica en las propiedades del proyecto en Microsoft Visual Studio, o puede especificar .NET Framework 4 en el [**<supportedRuntime> elemento**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) de un archivo de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="76c9d-118">To run applications that are built with earlier .NET Framework versions with .NET Framework 4, you must compile your application to target the .NET Framework 4 version by specifying it in the properties for your project in Microsoft Visual Studio, or you can specify .NET Framework 4 in the [**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in an application configuration file.</span></span>

<span data-ttu-id="76c9d-119">Para obtener más información sobre cómo migrar a la .NET Framework 4, vea [Guía de migración para la compatibilidad con .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) y [versiones en el .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="76c9d-119">For more information about how to migrate to the .NET Framework 4, see [Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) and [Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="76c9d-120">Pruebas de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="76c9d-120">Compatibility Tests</span></span>

<span data-ttu-id="76c9d-121">Después de realizar los cambios, pruebe la aplicación para asegurarse de que se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="76c9d-121">After you make the changes, test your application to make sure that it runs correctly.</span></span> <span data-ttu-id="76c9d-122">Puede probar la compatibilidad como se describe en el tema de [compatibilidad de aplicaciones de .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="76c9d-122">You can test compatibility as described in the [.NET Framework 4 Application Compatibility](/previous-versions/dd889541(v=msdn.10)) topic.</span></span>

<span data-ttu-id="76c9d-123">Si su aplicación o componente no funciona después de instalar .NET Framework 4, envíe un error a través del sitio web de [Microsoft Connect](https://connect.microsoft.com/visualstudio) .</span><span class="sxs-lookup"><span data-stu-id="76c9d-123">If your application or component does not work after .NET Framework 4 is installed, submit a bug through the [Microsoft Connect](https://connect.microsoft.com/visualstudio) website.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="76c9d-124">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="76c9d-124">Links to Other Resources</span></span>

-   <span data-ttu-id="76c9d-125">[**<supportedRuntime> Element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="76c9d-125">[**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span></span>
-   <span data-ttu-id="76c9d-126">[Guía de migración para .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="76c9d-126">[Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span></span>
-   <span data-ttu-id="76c9d-127">[Compatibilidad de versiones en .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="76c9d-127">[Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span></span>
-   <span data-ttu-id="76c9d-128">**Tutorial de compatibilidad de aplicaciones de .NET Framework 4 RTM:**<https://msdn.microsoft.com/library/dd889541.aspx></span><span class="sxs-lookup"><span data-stu-id="76c9d-128">**.NET Framework 4 RTM Application Compatibility Walkthrough:**<https://msdn.microsoft.com/library/dd889541.aspx></span></span>
-   [<span data-ttu-id="76c9d-129">Microsoft Connect</span><span class="sxs-lookup"><span data-stu-id="76c9d-129">Microsoft Connect</span></span>](https://connect.microsoft.com/)

 

 
