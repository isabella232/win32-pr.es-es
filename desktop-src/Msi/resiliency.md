---
description: La resistencia es la capacidad de una aplicación para recuperarse correctamente de las situaciones en las que falta un componente vital o se ha reemplazado por una versión incompatible.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resistencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668358"
---
# <a name="resiliency"></a><span data-ttu-id="72e0b-103">Resistencia</span><span class="sxs-lookup"><span data-stu-id="72e0b-103">Resiliency</span></span>

<span data-ttu-id="72e0b-104">La resistencia es la capacidad de una aplicación para recuperarse correctamente de las situaciones en las que falta un componente vital o se ha reemplazado por una versión incompatible.</span><span class="sxs-lookup"><span data-stu-id="72e0b-104">Resiliency is the ability of an application to recover gracefully from situations in which a vital component is missing, or has been replaced by an incompatible version.</span></span> <span data-ttu-id="72e0b-105">Mediante la creación de un paquete de instalación y el uso de las [funciones del instalador](installer-functions.md), los desarrolladores pueden utilizar la Windows Installer para generar aplicaciones resistentes capaces de recuperarse de estas situaciones.</span><span class="sxs-lookup"><span data-stu-id="72e0b-105">By authoring an installation package and using the [Installer Functions](installer-functions.md), developers can use the Windows Installer to produce resilient applications capable of recovering from such situations.</span></span>

-   <span data-ttu-id="72e0b-106">Use la lista de origen del instalador para aumentar la resistencia de las aplicaciones que se basan en los recursos de red.</span><span class="sxs-lookup"><span data-stu-id="72e0b-106">Use the installer's source list to increase the resiliency of applications that rely on network resources.</span></span> <span data-ttu-id="72e0b-107">Para obtener más información, consulte [resistencia del origen](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="72e0b-107">For more information, see [Source Resiliency](source-resiliency.md).</span></span>
-   <span data-ttu-id="72e0b-108">Use la API del instalador para comprobar si hay instalada una versión vital de la característica, el componente, el archivo o el archivo.</span><span class="sxs-lookup"><span data-stu-id="72e0b-108">Use the installer's API to check whether a vital feature, component, file, or file version is installed.</span></span>
-   <span data-ttu-id="72e0b-109">Use la API del instalador para comprobar la ruta de acceso a un componente en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="72e0b-109">Use the installer's API to check the path to a component at run time.</span></span> <span data-ttu-id="72e0b-110">Esto reduce la dependencia de la aplicación en rutas de acceso de archivo estáticas, que suelen diferir entre equipos.</span><span class="sxs-lookup"><span data-stu-id="72e0b-110">This reduces your application's dependency on static file paths, which commonly differ between computers.</span></span>
-   <span data-ttu-id="72e0b-111">Use el instalador para volver a instalar los accesos directos, las entradas del registro y otros componentes dañados sin tener que volver a ejecutar el programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="72e0b-111">Use the installer to reinstall damaged shortcuts, registry entries, and other components without having to rerun setup.</span></span>
-   <span data-ttu-id="72e0b-112">Aumente la resistencia de la instalación del producto manteniendo habilitada la funcionalidad de reversión del instalador.</span><span class="sxs-lookup"><span data-stu-id="72e0b-112">Increase the resiliency of your product's installation by leaving the rollback capability of the installer enabled.</span></span> <span data-ttu-id="72e0b-113">Para obtener más información, consulte [reversión de instalación](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="72e0b-113">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



