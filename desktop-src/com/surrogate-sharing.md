---
title: Uso compartido de suplentes
description: Los servidores DLL compartirán un suplente si tienen identidades de seguridad coincidentes y comparten el mismo valor de AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774959"
---
# <a name="surrogate-sharing"></a><span data-ttu-id="07134-103">Uso compartido de suplentes</span><span class="sxs-lookup"><span data-stu-id="07134-103">Surrogate Sharing</span></span>

<span data-ttu-id="07134-104">Los servidores DLL compartirán un suplente si tienen identidades de seguridad coincidentes y comparten el mismo valor de AppID.</span><span class="sxs-lookup"><span data-stu-id="07134-104">DLL servers will share a surrogate if they have matching security identities and share the same AppID value.</span></span>

<span data-ttu-id="07134-105">Los servidores DLL se cargan, de forma predeterminada, en su propio proceso suplente.</span><span class="sxs-lookup"><span data-stu-id="07134-105">DLL servers are loaded, by default, into their own surrogate process.</span></span> <span data-ttu-id="07134-106">Para cargar otros servidores DLL en un suplente existente para que admita más de un servidor DLL, existen dos requisitos:</span><span class="sxs-lookup"><span data-stu-id="07134-106">To load other DLL servers into an existing surrogate so that it supports more than one DLL server, there are two requirements:</span></span>

-   <span data-ttu-id="07134-107">Los servidores DLL deben tener el mismo valor de AppID.</span><span class="sxs-lookup"><span data-stu-id="07134-107">The DLL servers must have the same AppID value.</span></span>
-   <span data-ttu-id="07134-108">El contexto de seguridad de los servidores DLL debe ser el mismo.</span><span class="sxs-lookup"><span data-stu-id="07134-108">The security context of the DLL servers must be the same.</span></span>

<span data-ttu-id="07134-109">Si se van a iniciar dos servidores DLL con distintas identidades de seguridad, deben estar en distintos suplentes, independientemente de que AppIDs coincidan.</span><span class="sxs-lookup"><span data-stu-id="07134-109">If two DLL servers are to be launched under different security identities, they must be in different surrogates, whether their AppIDs match.</span></span>

<span data-ttu-id="07134-110">A continuación se proporciona un ejemplo de cómo administrar el uso compartido de suplentes con AppIDs:</span><span class="sxs-lookup"><span data-stu-id="07134-110">Following is an example of administering surrogate sharing with AppIDs:</span></span>

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

<span data-ttu-id="07134-111">Los dos CLSID para componentes DLL comp1.dll y comp2.dll se han configurado para compartir un AppID.</span><span class="sxs-lookup"><span data-stu-id="07134-111">The two CLSIDs for DLL components comp1.dll and comp2.dll have been configured to share an AppID.</span></span> <span data-ttu-id="07134-112">La clave [AppID](appid-key.md) especifica que el servidor dll se puede cargar en un suplente especificando el valor de [DllSurrogate](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="07134-112">The [AppID](appid-key.md) key specifies that the DLL server can be loaded in a surrogate by specifying the [DllSurrogate](dllsurrogate.md) value.</span></span> <span data-ttu-id="07134-113">En este ejemplo, el valor de **DllSurrogate** es una cadena vacía, que indica que se debe usar la implementación del sistema predeterminada del suplente de la dll.</span><span class="sxs-lookup"><span data-stu-id="07134-113">In this example, the **DllSurrogate** value is an empty string, indicating that the default system implementation of the DLL surrogate should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07134-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07134-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07134-115">Requisitos del servidor DLL</span><span class="sxs-lookup"><span data-stu-id="07134-115">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="07134-116">Registrando el servidor DLL para la activación de suplentes</span><span class="sxs-lookup"><span data-stu-id="07134-116">Registering the DLL Server for Surrogate Activation</span></span>](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




