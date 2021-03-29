---
title: El archivo UUID de la interfaz
description: El archivo UUID de la interfaz recopila las definiciones de los identificadores de interfaz de todas las interfaces en el archivo IDL procesado.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL y COM MIDL, interfaces, archivos UUID de proxy
- archivo UUID de interfaz MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778991"
---
# <a name="the-interface-uuid-file"></a><span data-ttu-id="06de9-105">El archivo UUID de la interfaz</span><span class="sxs-lookup"><span data-stu-id="06de9-105">The Interface UUID File</span></span>

<span data-ttu-id="06de9-106">El archivo UUID de la interfaz recopila las definiciones de los identificadores de interfaz de todas las interfaces en el archivo IDL procesado.</span><span class="sxs-lookup"><span data-stu-id="06de9-106">The interface UUID file collects the definitions of the interface identifiers from all interfaces in the processed IDL file.</span></span> <span data-ttu-id="06de9-107">Al igual que el archivo de código auxiliar y el archivo de encabezado, el cierre del flujo de entrada se define mediante el archivo IDL actual y los archivos incluidos.</span><span class="sxs-lookup"><span data-stu-id="06de9-107">Similar to the stub file and the header file, the input stream closure is defined by the current IDL file and the included files.</span></span> <span data-ttu-id="06de9-108">Por ejemplo, para la interfaz IFace, el compilador genera un IID de constante \_ IFace y lo inicializa en el UUID de la interfaz especificado en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="06de9-108">For example, for Interface IFace, the compiler generates a constant IID\_IFace and initializes it to the interface's UUID specified in the IDL file.</span></span> <span data-ttu-id="06de9-109">Las aplicaciones cliente y el archivo DLL de proxy usan esta constante para identificar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="06de9-109">Client applications and the proxy DLL use this constant to identify the interface.</span></span>

<span data-ttu-id="06de9-110">El nombre predeterminado de un archivo IID de interfaz generado a partir de un archivo. idl es el archivo \_ i.c.</span><span class="sxs-lookup"><span data-stu-id="06de9-110">The default name for an interface IID file generated from a file.idl is File\_i.c.</span></span> <span data-ttu-id="06de9-111">El modificador de compilador de MIDL [**/IID**](-iid.md) invalida el nombre predeterminado del archivo UUID de interfaz.</span><span class="sxs-lookup"><span data-stu-id="06de9-111">The [**/iid**](-iid.md) MIDL compiler switch overrides the default name of the interface UUID file.</span></span>

 

 




