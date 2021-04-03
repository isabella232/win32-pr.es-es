---
title: Salida del compilador MIDL
description: Con los archivos IDL y ACF como entrada, el compilador MIDL genera hasta cinco archivos de origen en lenguaje C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075356"
---
# <a name="midl-compiler-output"></a><span data-ttu-id="40174-103">Salida del compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="40174-103">MIDL Compiler Output</span></span>

<span data-ttu-id="40174-104">Con los archivos IDL y ACF como entrada, el compilador MIDL genera hasta cinco archivos de origen en lenguaje C.</span><span class="sxs-lookup"><span data-stu-id="40174-104">With the IDL and ACF files as input, the MIDL compiler generates up to five C-language source files.</span></span> <span data-ttu-id="40174-105">De forma predeterminada, el compilador MIDL usa el nombre de archivo base del archivo IDL como parte de los archivos de código auxiliar generados.</span><span class="sxs-lookup"><span data-stu-id="40174-105">By default, the MIDL compiler uses the base file name of the IDL file as part of the generated stub files.</span></span> <span data-ttu-id="40174-106">Si hay más de seis caracteres en el nombre de archivo base, es posible que algunos sistemas de archivos no acepten el nombre completo del código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="40174-106">When more than six characters are present in the base file name, some file systems may not accept the full stub name.</span></span> <span data-ttu-id="40174-107">En la tabla siguiente se muestran las convenciones que se usan para los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="40174-107">The following table shows conventions used for file names.</span></span>



| <span data-ttu-id="40174-108">Archivo</span><span class="sxs-lookup"><span data-stu-id="40174-108">File</span></span>        | <span data-ttu-id="40174-109">Parte predeterminada del nombre del archivo base</span><span class="sxs-lookup"><span data-stu-id="40174-109">Default portion of base file name</span></span> | <span data-ttu-id="40174-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40174-110">Example</span></span>      |
|-------------|-----------------------------------|--------------|
| <span data-ttu-id="40174-111">Archivo IDL</span><span class="sxs-lookup"><span data-stu-id="40174-111">IDL file</span></span>    | ---                               | <span data-ttu-id="40174-112">Abcdefgh. idl</span><span class="sxs-lookup"><span data-stu-id="40174-112">Abcdefgh.idl</span></span> |
| <span data-ttu-id="40174-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40174-113">Header</span></span>      | <span data-ttu-id="40174-114">.h</span><span class="sxs-lookup"><span data-stu-id="40174-114">.h</span></span>                                | <span data-ttu-id="40174-115">Abcdef. h</span><span class="sxs-lookup"><span data-stu-id="40174-115">Abcdef.h</span></span>     |
| <span data-ttu-id="40174-116">Código auxiliar de cliente</span><span class="sxs-lookup"><span data-stu-id="40174-116">Client stub</span></span> | <span data-ttu-id="40174-117">\_c. c</span><span class="sxs-lookup"><span data-stu-id="40174-117">\_c.c</span></span>                             | <span data-ttu-id="40174-118">Abcdef \_ c. c</span><span class="sxs-lookup"><span data-stu-id="40174-118">Abcdef\_c.c</span></span>  |
| <span data-ttu-id="40174-119">Código auxiliar de servidor</span><span class="sxs-lookup"><span data-stu-id="40174-119">Server stub</span></span> | <span data-ttu-id="40174-120">\_s. c</span><span class="sxs-lookup"><span data-stu-id="40174-120">\_s.c</span></span>                             | <span data-ttu-id="40174-121">Abcdef \_ s. c</span><span class="sxs-lookup"><span data-stu-id="40174-121">Abcdef\_s.c</span></span>  |



 

 

 




