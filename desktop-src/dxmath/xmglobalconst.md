---
description: Declara un objeto para que sea una constante de selección, para evitar recargas redundantes de ese objeto si se usa (y se declara) en varios lugares de la biblioteca de DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: XMGLOBALCONST (macro)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715569"
---
# <a name="xmglobalconst-macro"></a><span data-ttu-id="45d95-103">XMGLOBALCONST (macro)</span><span class="sxs-lookup"><span data-stu-id="45d95-103">XMGLOBALCONST macro</span></span>

<span data-ttu-id="45d95-104">Declara un objeto para que sea una constante *de selección* , para evitar recargas redundantes de ese objeto si se usa (y se declara) en varios lugares de la biblioteca de DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="45d95-104">Declares an object to be a *pick-any* constant, to avoid redundant reloads of that object if it is used (and declared) in multiple places in the DirectXMath Library.</span></span>

## <a name="syntax"></a><span data-ttu-id="45d95-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45d95-105">Syntax</span></span>

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a><span data-ttu-id="45d95-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45d95-106">Remarks</span></span>

<span data-ttu-id="45d95-107">El uso de XMGLOBALCONST permite la especificación de constantes globales.</span><span class="sxs-lookup"><span data-stu-id="45d95-107">Using XMGLOBALCONST permits the specification of global constants.</span></span> <span data-ttu-id="45d95-108">Esto ayuda a reducir el tamaño del segmento de datos de una aplicación, evitar la creación y destrucción de objetos redundantes, y reducir las operaciones de carga y almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="45d95-108">This helps to reduce the size of an application's data segment, avoid redundant object creation and destruction, and reduce load and store operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="45d95-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45d95-109">Requirements</span></span>

<span data-ttu-id="45d95-110">**Encabezado:** Declarado en DirectXMath. h.</span><span class="sxs-lookup"><span data-stu-id="45d95-110">**Header:** Declared in DirectXMath.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45d95-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45d95-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45d95-112">Macros de biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="45d95-112">DirectXMath Library Macros</span></span>](ovw-xnamath-reference-macros.md)
</dt> <dt>

[<span data-ttu-id="45d95-113">Constantes globales en la biblioteca de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="45d95-113">Global Constants in the DirectXMath Library</span></span>](pg-xnamath-internals.md)
</dt> <dt>

<span data-ttu-id="45d95-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="45d95-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span></span>
</dt> <dt>

<span data-ttu-id="45d95-115">[modificado](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="45d95-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span></span>
</dt> </dl>

 

 
