---
title: Estructura FONTGROUPHDR
description: Contiene la información necesaria para que una aplicación tenga acceso a una fuente específica. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Menús de la estructura FONTGROUPHDR y otros recursos
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274540"
---
# <a name="fontgrouphdr-structure"></a><span data-ttu-id="369d3-105">Estructura FONTGROUPHDR</span><span class="sxs-lookup"><span data-stu-id="369d3-105">FONTGROUPHDR structure</span></span>

<span data-ttu-id="369d3-106">Contiene la información necesaria para que una aplicación tenga acceso a una fuente específica.</span><span class="sxs-lookup"><span data-stu-id="369d3-106">Contains the information necessary for an application to access a specific font.</span></span> <span data-ttu-id="369d3-107">La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.</span><span class="sxs-lookup"><span data-stu-id="369d3-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="369d3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="369d3-108">Syntax</span></span>


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a><span data-ttu-id="369d3-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="369d3-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="369d3-110">**NumberOfFonts**</span><span class="sxs-lookup"><span data-stu-id="369d3-110">**NumberOfFonts**</span></span>
</dt> <dd>

<span data-ttu-id="369d3-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="369d3-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="369d3-112">El número de fuentes individuales asociadas a este recurso.</span><span class="sxs-lookup"><span data-stu-id="369d3-112">The number of individual fonts associated with this resource.</span></span>

</dd> <dt>

<span data-ttu-id="369d3-113">**DE**</span><span class="sxs-lookup"><span data-stu-id="369d3-113">**DE**</span></span>
</dt> <dd>

<span data-ttu-id="369d3-114">Tipo: **[ **dirente**](direntry.md)**</span><span class="sxs-lookup"><span data-stu-id="369d3-114">Type: **[**DIRENTRY**](direntry.md)**</span></span>

</dd> <dd>

<span data-ttu-id="369d3-115">Estructura que contiene un identificador ordinal único para cada fuente del recurso.</span><span class="sxs-lookup"><span data-stu-id="369d3-115">A structure that contains a unique ordinal identifier for each font in the resource.</span></span> <span data-ttu-id="369d3-116">El miembro **de** es un marcador de posición para la matriz de longitud variable de estructuras de [**direntary**](direntry.md) .</span><span class="sxs-lookup"><span data-stu-id="369d3-116">The **DE** member is a placeholder for the variable-length array of [**DIRENTRY**](direntry.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="369d3-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="369d3-117">Remarks</span></span>

<span data-ttu-id="369d3-118">La estructura **FONTGROUPHDR** sigue los datos de las fuentes individuales en. Archivo res.</span><span class="sxs-lookup"><span data-stu-id="369d3-118">The **FONTGROUPHDR** structure follows the data for the individual fonts in the .Res file.</span></span> <span data-ttu-id="369d3-119">El compilador de recursos agrega automáticamente la estructura **FONTGROUPHDR** , generalmente como la última entrada del archivo.</span><span class="sxs-lookup"><span data-stu-id="369d3-119">The resource compiler automatically adds the **FONTGROUPHDR** structure, generally as the last entry in the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="369d3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="369d3-120">Requirements</span></span>



| <span data-ttu-id="369d3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="369d3-121">Requirement</span></span> | <span data-ttu-id="369d3-122">Value</span><span class="sxs-lookup"><span data-stu-id="369d3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="369d3-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="369d3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="369d3-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="369d3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="369d3-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="369d3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="369d3-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="369d3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="369d3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="369d3-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="369d3-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="369d3-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="369d3-129">**ARRENDAMIENTO**</span><span class="sxs-lookup"><span data-stu-id="369d3-129">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="369d3-130">**FONTDIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="369d3-130">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

<span data-ttu-id="369d3-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="369d3-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="369d3-132">Recursos</span><span class="sxs-lookup"><span data-stu-id="369d3-132">Resources</span></span>](resources.md)
</dt> </dl>

 

 





