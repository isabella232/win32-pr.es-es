---
title: Enumeración TITLEBAR_TYPE (Softkbdc. h)
description: Los elementos de la \_ enumeración de tipo TITLEBAR se usan para especificar los tipos de titlebars que están disponibles para una ventana de teclado en pantalla.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- Marco de servicios de texto de enumeración de TITLEBAR_TYPE
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685990"
---
# <a name="titlebar_type-enumeration"></a><span data-ttu-id="b5db0-104">\_Enumeración de tipo TITLEBAR</span><span class="sxs-lookup"><span data-stu-id="b5db0-104">TITLEBAR\_TYPE enumeration</span></span>

<span data-ttu-id="b5db0-105">Los elementos de la enumeración de **\_ tipo TITLEBAR** se usan para especificar los tipos de titlebars que están disponibles para una ventana de teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="b5db0-105">Elements of the **TITLEBAR\_TYPE** enumeration are used to specify types of titlebars that are available for a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5db0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5db0-106">Syntax</span></span>


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="b5db0-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="b5db0-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b5db0-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR \_ None**</span><span class="sxs-lookup"><span data-stu-id="b5db0-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="b5db0-109">La ventana teclado en pantalla no usa ninguna TitleBar.</span><span class="sxs-lookup"><span data-stu-id="b5db0-109">The soft keyboard window uses no titlebar.</span></span>

</dd> <dt>

<span data-ttu-id="b5db0-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**solo el agarrador de la TITLEBAR \_ \_ horiz \_**</span><span class="sxs-lookup"><span data-stu-id="b5db0-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**TITLEBAR\_GRIPPER\_HORIZ\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="b5db0-111">La ventana teclado en pantalla usa solo una barra de redimensionamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="b5db0-111">The soft keyboard window uses a horizontal gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="b5db0-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**\_solo Vert (agarrador de TITLEBAR) \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5db0-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TITLEBAR\_GRIPPER\_VERTI\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="b5db0-113">La ventana teclado en pantalla solo usa una barra de redimensionamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="b5db0-113">The soft keyboard window uses a vertical gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="b5db0-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**botón de sujeción de la TITLEBAR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b5db0-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**TITLEBAR\_GRIPPER\_BUTTON**</span></span>
</dt> <dd>

<span data-ttu-id="b5db0-115">La ventana teclado en pantalla solo usa un botón de agarrador.</span><span class="sxs-lookup"><span data-stu-id="b5db0-115">The soft keyboard window uses a gripper button only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5db0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5db0-116">Requirements</span></span>



| <span data-ttu-id="b5db0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5db0-117">Requirement</span></span> | <span data-ttu-id="b5db0-118">Value</span><span class="sxs-lookup"><span data-stu-id="b5db0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5db0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5db0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b5db0-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b5db0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b5db0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5db0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b5db0-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5db0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b5db0-123">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b5db0-123">Redistributable</span></span><br/>          | <span data-ttu-id="b5db0-124">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b5db0-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="b5db0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5db0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5db0-126"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5db0-126"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="b5db0-127">IDL</span><span class="sxs-lookup"><span data-stu-id="b5db0-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5db0-128"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5db0-128"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





