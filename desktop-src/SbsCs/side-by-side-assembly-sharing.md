---
description: En la ilustración siguiente se muestra cómo dos aplicaciones pueden compartir un ensamblado mediante el método tradicional de uso compartido de ensamblados.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Uso compartido de ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002765"
---
# <a name="side-by-side-assembly-sharing"></a><span data-ttu-id="86899-103">Uso compartido de ensamblados en paralelo</span><span class="sxs-lookup"><span data-stu-id="86899-103">Side-by-side Assembly Sharing</span></span>

<span data-ttu-id="86899-104">En la ilustración siguiente se muestra cómo dos aplicaciones pueden compartir un ensamblado mediante el método tradicional de uso compartido de ensamblados.</span><span class="sxs-lookup"><span data-stu-id="86899-104">The following figure illustrates how two applications might share an assembly using the traditional method of assembly sharing.</span></span> <span data-ttu-id="86899-105">Un problema con el uso compartido de ensamblados tradicional se produce cuando una aplicación instala una versión de un ensamblado, normalmente un archivo DLL, que no es compatible con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="86899-105">A problem with traditional assembly sharing occurs when an application installs a version of an assembly—commonly a DLL—that is not backward compatible.</span></span> <span data-ttu-id="86899-106">La aplicación que acaba de instalar funciona, pero es posible que las aplicaciones que dependen de la versión anterior del archivo DLL dejen de funcionar.</span><span class="sxs-lookup"><span data-stu-id="86899-106">The application just installed works, but applications that depended on the previous DLL version may no longer work.</span></span>

![representación de dos aplicaciones que comparten un ensamblado](images/sxs1.png)

<span data-ttu-id="86899-108">La solución de ensamblados en paralelo y aplicación aislada permite que las distintas versiones del mismo ensamblado Win32 se ejecuten al mismo tiempo en el mismo sistema sin conflictos.</span><span class="sxs-lookup"><span data-stu-id="86899-108">The isolated application and side-by-side assembly solution enables different versions of the same Win32 assembly to run at the same time on the same system without conflict.</span></span> <span data-ttu-id="86899-109">Al especificar la versión de ensamblado en paralelo que debe usar la aplicación, los desarrolladores pueden garantizar que la configuración que prueba se duplicará siempre en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="86899-109">By specifying which side-by-side assembly version the application should use, developers can guarantee that the configuration they test will always be duplicated on the user's computer.</span></span> <span data-ttu-id="86899-110">El uso compartido simultáneo se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="86899-110">Side-by-side sharing is illustrated in the following figure.</span></span>

![implementación de uso compartido de ensamblados en paralelo](images/sxs2.png)

<span data-ttu-id="86899-112">Para obtener más información, vea [acerca de las aplicaciones aisladas y los ensamblados en paralelo](about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="86899-112">For more information, see [About Isolated Applications and Side-by-side Assemblies](about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

 

 



