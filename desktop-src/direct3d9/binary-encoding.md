---
description: En esta sección se detallan las versiones binarias del formato de archivo de DirectX (. x) que se introdujeron con la versión de DirectX 3,0.
ms.assetid: d1b6698f-72bd-40a4-a501-c2093cd940f6
title: Codificación binaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56937b54be82e36d6ff18aab2a2349be6d59cc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714784"
---
# <a name="binary-encoding"></a><span data-ttu-id="7391c-103">Codificación binaria</span><span class="sxs-lookup"><span data-stu-id="7391c-103">Binary Encoding</span></span>

<span data-ttu-id="7391c-104">En esta sección se detallan las versiones binarias del formato de archivo de DirectX (. x) que se introdujeron con la versión de DirectX 3,0.</span><span class="sxs-lookup"><span data-stu-id="7391c-104">This section details the binary version of the DirectX (.x) file format as introduced with the release of DirectX 3.0.</span></span>

<span data-ttu-id="7391c-105">El formato binario es una representación con tokens del formato de texto.</span><span class="sxs-lookup"><span data-stu-id="7391c-105">The binary format is a tokenized representation of the text format.</span></span> <span data-ttu-id="7391c-106">Los tokens pueden ser independientes o acompañados de registros de datos primitivos.</span><span class="sxs-lookup"><span data-stu-id="7391c-106">Tokens can be stand-alone or accompanied by primitive data records.</span></span> <span data-ttu-id="7391c-107">Los tokens independientes proporcionan una estructura gramatical y los tokens del cojinete de registros proporcionan los datos necesarios.</span><span class="sxs-lookup"><span data-stu-id="7391c-107">Stand-alone tokens give grammatical structure, and record-bearing tokens supply the necessary data.</span></span>

<span data-ttu-id="7391c-108">Tenga en cuenta que todos los datos se almacenan en formato Little-Endian.</span><span class="sxs-lookup"><span data-stu-id="7391c-108">Note that all data is stored in little-endian format.</span></span> <span data-ttu-id="7391c-109">Un flujo de datos binario válido está formado por un encabezado seguido por plantillas u objetos de datos.</span><span class="sxs-lookup"><span data-stu-id="7391c-109">A valid binary data stream consists of a header followed by templates and/or data objects.</span></span>

<span data-ttu-id="7391c-110">En esta sección se describen los siguientes componentes del formato de archivo binario y se proporciona una plantilla de ejemplo y un objeto de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="7391c-110">This section discusses the following components of the binary file format and provides an example template and binary data object.</span></span>

-   [<span data-ttu-id="7391c-111">Header</span><span class="sxs-lookup"><span data-stu-id="7391c-111">Header</span></span>](header.md)
-   [<span data-ttu-id="7391c-112">Tokens</span><span class="sxs-lookup"><span data-stu-id="7391c-112">Tokens</span></span>](tokens.md)
-   [<span data-ttu-id="7391c-113">Registros de token</span><span class="sxs-lookup"><span data-stu-id="7391c-113">Token Records</span></span>](token-records.md)
-   <span data-ttu-id="7391c-114">[Templates](dx9-graphics-reference-x-file-binaryencoding-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="7391c-114">[Templates](dx9-graphics-reference-x-file-binaryencoding-templates.md)</span></span>
-   [<span data-ttu-id="7391c-115">Data</span><span class="sxs-lookup"><span data-stu-id="7391c-115">Data</span></span>](dx9-graphics-reference-x-file-binaryencoding-data.md)
-   [<span data-ttu-id="7391c-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7391c-116">Examples</span></span>](examples.md)

## <a name="related-topics"></a><span data-ttu-id="7391c-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7391c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7391c-118">Referencia de formato de archivo X</span><span class="sxs-lookup"><span data-stu-id="7391c-118">X File Format Reference</span></span>](dx9-graphics-reference-x-file-format.md)
</dt> </dl>

 

 



