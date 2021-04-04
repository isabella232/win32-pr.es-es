---
title: VBRPeak
description: El atributo VBRPeak contiene la velocidad de bits más alta en una secuencia codificada de velocidad de bits variable (VBR).
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- VBRPeak formato de Windows Media
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076840"
---
# <a name="vbrpeak"></a><span data-ttu-id="16250-104">VBRPeak</span><span class="sxs-lookup"><span data-stu-id="16250-104">VBRPeak</span></span>

<span data-ttu-id="16250-105">El atributo **VBRPeak** contiene la velocidad de bits más alta en una secuencia codificada de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="16250-105">The **VBRPeak** attribute contains the highest momentary bit rate in a variable bit rate (VBR) encoded stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="16250-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="16250-106">Global Constant</span></span>

<span data-ttu-id="16250-107">g \_ wszVBRPeak</span><span class="sxs-lookup"><span data-stu-id="16250-107">g\_wszVBRPeak</span></span>

## <a name="data-type"></a><span data-ttu-id="16250-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="16250-108">Data Type</span></span>

<span data-ttu-id="16250-109">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="16250-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="16250-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16250-110">Remarks</span></span>

<span data-ttu-id="16250-111">Al tener acceso a la interfaz **IWMHeaderInfo3** del objeto escritor, puede Agregar o cambiar este valor.</span><span class="sxs-lookup"><span data-stu-id="16250-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="16250-112">En otros objetos (editor de metadatos, lector y lector sincrónico), este valor es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="16250-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="16250-113">El escritor escribe automáticamente un valor de **VBRPeak** para cada secuencia VBR.</span><span class="sxs-lookup"><span data-stu-id="16250-113">The writer automatically writes a **VBRPeak** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="16250-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="16250-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16250-115">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="16250-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




