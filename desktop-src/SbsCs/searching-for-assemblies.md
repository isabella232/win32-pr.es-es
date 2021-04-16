---
description: Hay dos métodos por los que una aplicación de hospedaje puede buscar ensamblados en paralelo.
ms.assetid: f34f8f39-f03c-4adf-afa8-9cb9ed48d149
title: Buscar ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f257b7da8099508fb268623a175d8ebd8e9d8337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649193"
---
# <a name="searching-for-assemblies"></a><span data-ttu-id="d3566-103">Buscar ensamblados</span><span class="sxs-lookup"><span data-stu-id="d3566-103">Searching for Assemblies</span></span>

<span data-ttu-id="d3566-104">Hay dos métodos por los que una aplicación de hospedaje puede buscar ensamblados en paralelo.</span><span class="sxs-lookup"><span data-stu-id="d3566-104">There are two methods by which a hosting application can search for side-by-side assemblies.</span></span>

<span data-ttu-id="d3566-105">Los módulos hospedados pueden registrarse en la aplicación de hospedaje extendiendo parte de la información de configuración compartida.</span><span class="sxs-lookup"><span data-stu-id="d3566-105">Hosted modules can register themselves with the hosting application by extending some shared configuration information.</span></span> <span data-ttu-id="d3566-106">A continuación, la aplicación puede usar esta información de configuración para cargar los ensamblados necesarios para la nueva funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="d3566-106">The application can then use this configuration information to load the assemblies required for the new functionality.</span></span> <span data-ttu-id="d3566-107">Esto se puede hacer llamando a [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) en los manifiestos especificados en los datos de registro, seguido de una llamada a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para entrar en el nuevo módulo.</span><span class="sxs-lookup"><span data-stu-id="d3566-107">This could be done by calling [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) on manifests specified in the registration data, followed by calling [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get into the new module.</span></span> <span data-ttu-id="d3566-108">Tenga en cuenta que, con este método, los nuevos componentes deben actualizar el estado de la aplicación compartida para indicar su presencia.</span><span class="sxs-lookup"><span data-stu-id="d3566-108">Note that with this method, the new components have to update some shared application state to indicate their presence.</span></span>

<span data-ttu-id="d3566-109">La aplicación de hospedaje puede buscar activamente los ensamblados al inicio mediante [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) para buscar archivos dll o manifiestos en una ubicación especificada y, a continuación, usar [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) para tener acceso a la información.</span><span class="sxs-lookup"><span data-stu-id="d3566-109">The hosting application can actively search for the assemblies on startup using [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) to look for DLLs or manifests in a specified location, and then use [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) to access the information.</span></span> <span data-ttu-id="d3566-110">Este método no requiere ningún registro del componente.</span><span class="sxs-lookup"><span data-stu-id="d3566-110">This method requires no registration of the component.</span></span>

 

 
