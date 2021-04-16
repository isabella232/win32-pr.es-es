---
title: Bibliotecas de tipos de extensiones ADSI
description: Las bibliotecas de tipos para las extensiones no se combinan.
ms.assetid: 33cde2fe-9b90-4f63-a215-cf0c8f8defb1
ms.tgt_platform: multiple
keywords:
- ADSI Extensions de bibliotecas de tipos ADSI
- extensiones ADSI, bibliotecas de tipos de extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7efc89bd491d5ee244c5a2a64dd7df4c84b61ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531863"
---
# <a name="adsi-extension-type-libraries"></a><span data-ttu-id="c476c-105">Bibliotecas de tipos de extensiones ADSI</span><span class="sxs-lookup"><span data-stu-id="c476c-105">ADSI Extension Type Libraries</span></span>

<span data-ttu-id="c476c-106">Las bibliotecas de tipos para las extensiones no se combinan.</span><span class="sxs-lookup"><span data-stu-id="c476c-106">The type libraries for extensions are not merged.</span></span> <span data-ttu-id="c476c-107">Los clientes ADSI deben incluir específicamente la biblioteca de tipos para cada extensión.</span><span class="sxs-lookup"><span data-stu-id="c476c-107">ADSI clients must specifically include the type library for each extension.</span></span> <span data-ttu-id="c476c-108">La biblioteca de tipos es necesaria para que Visual Basic habilite los enlaces iniciales.</span><span class="sxs-lookup"><span data-stu-id="c476c-108">The type library is required for Visual Basic to enable early bindings.</span></span> <span data-ttu-id="c476c-109">Las aplicaciones cliente escritas en C/C++ pueden llamar al método **QueryInterface** en las interfaces de extensión definidas en los archivos de encabezado de la extensión.</span><span class="sxs-lookup"><span data-stu-id="c476c-109">Client applications written in C/C++ can call the **QueryInterface** method on the extension interfaces defined in the extension header files.</span></span>

 

 




