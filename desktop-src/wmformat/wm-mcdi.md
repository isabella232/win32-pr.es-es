---
title: WM/MCDI
description: El atributo WM/MCDI contiene el identificador del CD de música. Se trata de un volcado binario de la tabla de contenido del CD que se usa para identificar de forma única el CD.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- Formato de Windows Media WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714297"
---
# <a name="wmmcdi"></a><span data-ttu-id="8cbf8-105">WM/MCDI</span><span class="sxs-lookup"><span data-stu-id="8cbf8-105">WM/MCDI</span></span>

<span data-ttu-id="8cbf8-106">El atributo **WM/MCDI** contiene el identificador del CD de música.</span><span class="sxs-lookup"><span data-stu-id="8cbf8-106">The **WM/MCDI** attribute contains the music CD identifier.</span></span> <span data-ttu-id="8cbf8-107">Se trata de un volcado binario de la tabla de contenido del CD que se usa para identificar de forma única el CD.</span><span class="sxs-lookup"><span data-stu-id="8cbf8-107">This is a binary dump of the table of contents from the CD that is used to uniquely identify the CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="8cbf8-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="8cbf8-108">Global Constant</span></span>

<span data-ttu-id="8cbf8-109">g \_ wszWMMCDI</span><span class="sxs-lookup"><span data-stu-id="8cbf8-109">g\_wszWMMCDI</span></span>

## <a name="data-type"></a><span data-ttu-id="8cbf8-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8cbf8-110">Data Type</span></span>

<span data-ttu-id="8cbf8-111">**tipo de WMT \_ \_ binario**</span><span class="sxs-lookup"><span data-stu-id="8cbf8-111">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="8cbf8-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cbf8-112">Remarks</span></span>

<span data-ttu-id="8cbf8-113">Este atributo es compatible con el marco ID3, MCDI.</span><span class="sxs-lookup"><span data-stu-id="8cbf8-113">This attribute is compatible with the ID3 frame, MCDI.</span></span> <span data-ttu-id="8cbf8-114">La especificación ID3 para el marco MCDI requiere que solo exista uno de estos fotogramas por archivo y que exista un fotograma TRCK válido.</span><span class="sxs-lookup"><span data-stu-id="8cbf8-114">The ID3 specification for the MCDI frame requires that only one such frame exist per file and that a valid TRCK frame exist.</span></span> <span data-ttu-id="8cbf8-115">El editor de metadatos no realiza ninguna validación para estas reglas.</span><span class="sxs-lookup"><span data-stu-id="8cbf8-115">The metadata editor does not perform any validation for these rules.</span></span> <span data-ttu-id="8cbf8-116">Además, el tamaño de WM/MCDI no se limita a 804 bytes, como es el fotograma MCDI ID3.</span><span class="sxs-lookup"><span data-stu-id="8cbf8-116">Also, the size of WM/MCDI is not limited to 804 bytes, as is the MCDI ID3 frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cbf8-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cbf8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cbf8-118">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="8cbf8-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




