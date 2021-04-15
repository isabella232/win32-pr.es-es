---
title: Enumeración COLORTYPE (Softkbdc. h)
description: Los elementos de la enumeración COLORTYPE se usan para especificar los tipos de colores que están disponibles para un teclado en pantalla.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- Plataforma de servicios de texto de enumeración COLORTYPE
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666043"
---
# <a name="colortype-enumeration"></a><span data-ttu-id="e34a1-104">Enumeración COLORTYPE</span><span class="sxs-lookup"><span data-stu-id="e34a1-104">COLORTYPE enumeration</span></span>

<span data-ttu-id="e34a1-105">Los elementos de la enumeración **COLORTYPE** se usan para especificar los tipos de colores que están disponibles para un teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="e34a1-105">Elements of the **COLORTYPE** enumeration are used to specify types of colors that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="e34a1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e34a1-106">Syntax</span></span>


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a><span data-ttu-id="e34a1-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="e34a1-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e34a1-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span><span class="sxs-lookup"><span data-stu-id="e34a1-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span></span>
</dt> <dd>

<span data-ttu-id="e34a1-109">Color de fondo.</span><span class="sxs-lookup"><span data-stu-id="e34a1-109">Background color.</span></span>

</dd> <dt>

<span data-ttu-id="e34a1-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span><span class="sxs-lookup"><span data-stu-id="e34a1-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="e34a1-111">Color de primer plano no seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e34a1-111">Unselected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="e34a1-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span><span class="sxs-lookup"><span data-stu-id="e34a1-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="e34a1-113">Color de texto no seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e34a1-113">Unselected text color.</span></span>

</dd> <dt>

<span data-ttu-id="e34a1-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span><span class="sxs-lookup"><span data-stu-id="e34a1-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="e34a1-115">Color de primer plano seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e34a1-115">Selected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="e34a1-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span><span class="sxs-lookup"><span data-stu-id="e34a1-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="e34a1-117">Color del texto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e34a1-117">Selected text color.</span></span>

</dd> <dt>

<span data-ttu-id="e34a1-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**\_Tipo de color Max \_**</span><span class="sxs-lookup"><span data-stu-id="e34a1-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Max\_color\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="e34a1-119">Tipo de color máximo.</span><span class="sxs-lookup"><span data-stu-id="e34a1-119">Maximum color type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e34a1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e34a1-120">Requirements</span></span>



| <span data-ttu-id="e34a1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e34a1-121">Requirement</span></span> | <span data-ttu-id="e34a1-122">Value</span><span class="sxs-lookup"><span data-stu-id="e34a1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e34a1-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e34a1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e34a1-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e34a1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e34a1-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e34a1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e34a1-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e34a1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e34a1-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="e34a1-127">Redistributable</span></span><br/>          | <span data-ttu-id="e34a1-128">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e34a1-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="e34a1-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e34a1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e34a1-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="e34a1-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="e34a1-131">IDL</span><span class="sxs-lookup"><span data-stu-id="e34a1-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e34a1-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e34a1-132"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





