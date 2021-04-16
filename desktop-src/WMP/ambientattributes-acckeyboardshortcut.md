---
title: AmbientAttributes.accKeyboardShortcut
description: El atributo accKeyboardShortcut especifica o recupera una descripción del método abreviado de teclado para cualquier elemento.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AmbientAttributes. accKeyboardShortcut Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699547"
---
# <a name="ambientattributesacckeyboardshortcut"></a><span data-ttu-id="30eb7-104">AmbientAttributes.accKeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="30eb7-104">AmbientAttributes.accKeyboardShortcut</span></span>

<span data-ttu-id="30eb7-105">El atributo **accKeyboardShortcut** especifica o recupera una descripción del método abreviado de teclado para cualquier elemento.</span><span class="sxs-lookup"><span data-stu-id="30eb7-105">The **accKeyboardShortcut** attribute specifies or retrieves a keyboard shortcut description for any element.</span></span>

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a><span data-ttu-id="30eb7-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="30eb7-106">Possible Values</span></span>

<span data-ttu-id="30eb7-107">Este atributo es una **cadena** de lectura/escritura con un valor predeterminado de "" (cadena vacía).</span><span class="sxs-lookup"><span data-stu-id="30eb7-107">This attribute is a read/write **String** with a default value of "" (empty string).</span></span> <span data-ttu-id="30eb7-108">En el caso del elemento **Button** , este atributo tiene un valor predeterminado de "barra espaciadora o entrar".</span><span class="sxs-lookup"><span data-stu-id="30eb7-108">For the **BUTTON** element, this attribute has a default value of "Spacebar or Enter".</span></span> <span data-ttu-id="30eb7-109">En el caso del elemento **Slider** , el valor predeterminado es "Right/up Arrow to Increment, Left/Down Arrow to reduce".</span><span class="sxs-lookup"><span data-stu-id="30eb7-109">For the **SLIDER** element, the default value is "Right/Up Arrow to increase, Left/Down Arrow to decrease".</span></span>

## <a name="remarks"></a><span data-ttu-id="30eb7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30eb7-110">Remarks</span></span>

<span data-ttu-id="30eb7-111">Este atributo se usa para fines de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="30eb7-111">This attribute is used for accessibility purposes.</span></span> <span data-ttu-id="30eb7-112">Permite una descripción del método abreviado de teclado para que un programa lector lea en voz alta un elemento.</span><span class="sxs-lookup"><span data-stu-id="30eb7-112">It allows a description of the keyboard shortcut for any element to be read aloud by a reader program.</span></span> <span data-ttu-id="30eb7-113">Este atributo no establece el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="30eb7-113">This attribute does not set the shortcut.</span></span> <span data-ttu-id="30eb7-114">El scripter debe hacer ese trabajo.</span><span class="sxs-lookup"><span data-stu-id="30eb7-114">The scripter must do that work.</span></span>

<span data-ttu-id="30eb7-115">Este atributo también se aplica a los elementos de botón dentro del control de grupo de botones.</span><span class="sxs-lookup"><span data-stu-id="30eb7-115">This attribute also applies to button elements inside the button group control.</span></span>

## <a name="requirements"></a><span data-ttu-id="30eb7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30eb7-116">Requirements</span></span>



| <span data-ttu-id="30eb7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="30eb7-117">Requirement</span></span> | <span data-ttu-id="30eb7-118">Value</span><span class="sxs-lookup"><span data-stu-id="30eb7-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="30eb7-119">Versión</span><span class="sxs-lookup"><span data-stu-id="30eb7-119">Version</span></span><br/> | <span data-ttu-id="30eb7-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="30eb7-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30eb7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="30eb7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30eb7-122">**Atributos de ambiente**</span><span class="sxs-lookup"><span data-stu-id="30eb7-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





