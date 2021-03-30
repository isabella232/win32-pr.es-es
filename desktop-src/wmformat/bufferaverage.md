---
title: BufferAverage
description: El atributo BufferAverage contiene el tamaño de búfer promedio necesario para una secuencia de velocidad de bits variable (VBR).
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- BufferAverage formato de Windows Media
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148946"
---
# <a name="bufferaverage"></a><span data-ttu-id="cd50a-104">BufferAverage</span><span class="sxs-lookup"><span data-stu-id="cd50a-104">BufferAverage</span></span>

<span data-ttu-id="cd50a-105">El atributo **BufferAverage** contiene el tamaño de búfer promedio necesario para una secuencia de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="cd50a-105">The **BufferAverage** attribute contains the average buffer size needed for a variable bit rate (VBR) stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="cd50a-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="cd50a-106">Global Constant</span></span>

<span data-ttu-id="cd50a-107">g \_ wszBufferAverage</span><span class="sxs-lookup"><span data-stu-id="cd50a-107">g\_wszBufferAverage</span></span>

## <a name="data-type"></a><span data-ttu-id="cd50a-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="cd50a-108">Data Type</span></span>

<span data-ttu-id="cd50a-109">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd50a-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="cd50a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd50a-110">Remarks</span></span>

<span data-ttu-id="cd50a-111">Al tener acceso a la interfaz **IWMHeaderInfo3** del objeto escritor, puede Agregar o cambiar este valor.</span><span class="sxs-lookup"><span data-stu-id="cd50a-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="cd50a-112">En otros objetos (editor de metadatos, lector y lector sincrónico), este valor es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cd50a-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="cd50a-113">El escritor escribe automáticamente un valor de **BufferAverage** para cada secuencia VBR.</span><span class="sxs-lookup"><span data-stu-id="cd50a-113">The writer automatically writes a **BufferAverage** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd50a-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd50a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd50a-115">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="cd50a-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




