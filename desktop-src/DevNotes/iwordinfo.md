---
description: La interfaz IWordInfo es un componente de recurso de idioma específico para japonés. El objeto analiza el texto e identifica las palabras individuales, devolviendo las palabras de la cadena o devuelve las formas de diccionario (raíz) de las palabras en el texto de la cadena.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Interfaz IWordInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538385"
---
# <a name="iwordinfo-interface"></a><span data-ttu-id="f7276-104">Interfaz IWordInfo</span><span class="sxs-lookup"><span data-stu-id="f7276-104">IWordInfo interface</span></span>

<span data-ttu-id="f7276-105">\[Esta interfaz está obsoleta y no se admite en Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="f7276-105">\[This interface is obsolete and is not supported on Windows Vista.\]</span></span>

<span data-ttu-id="f7276-106">La interfaz **IWordInfo** es un componente de recurso de idioma específico para japonés.</span><span class="sxs-lookup"><span data-stu-id="f7276-106">The **IWordInfo** interface is a Japanese-specific language resource component.</span></span> <span data-ttu-id="f7276-107">El objeto analiza el texto e identifica las palabras individuales, devolviendo las palabras de la cadena o devuelve las formas de diccionario (raíz) de las palabras en el texto de la cadena.</span><span class="sxs-lookup"><span data-stu-id="f7276-107">The object parses text and identifies individual words, returning either the words in the string or returns the dictionary (root) forms of the words in the text of the string.</span></span>

## <a name="members"></a><span data-ttu-id="f7276-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f7276-108">Members</span></span>

<span data-ttu-id="f7276-109">La interfaz **IWordInfo** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f7276-109">The **IWordInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f7276-110">**IWordInfo** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f7276-110">**IWordInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="f7276-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f7276-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f7276-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f7276-112">Methods</span></span>

<span data-ttu-id="f7276-113">La interfaz **IWordInfo** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f7276-113">The **IWordInfo** interface has these methods.</span></span>



| <span data-ttu-id="f7276-114">Método</span><span class="sxs-lookup"><span data-stu-id="f7276-114">Method</span></span>        | <span data-ttu-id="f7276-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7276-115">Description</span></span>                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7276-116">**BreakText**</span><span class="sxs-lookup"><span data-stu-id="f7276-116">**BreakText**</span></span> | <span data-ttu-id="f7276-117">Analiza el texto para identificar palabras y proporciona los resultados al objeto [WordSink](/previous-versions//ms691570(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f7276-117">Parses text to identify words and provides the results to the [WordSink](/previous-versions//ms691570(v=vs.85)) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7276-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7276-118">Remarks</span></span>

<span data-ttu-id="f7276-119">Esta interfaz se utiliza para recuperar los saltos de palabra japoneses o los formatos de diccionario para el texto que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="f7276-119">This interface is used to retrieve Japanese word breaks or dictionary forms for the text to be analyzed.</span></span> <span data-ttu-id="f7276-120">La forma de Diccionario de una palabra es la forma no conjugada de la palabra.</span><span class="sxs-lookup"><span data-stu-id="f7276-120">The dictionary form of a word is the uninflected form of the word.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7276-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7276-121">Requirements</span></span>



| <span data-ttu-id="f7276-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7276-122">Requirement</span></span> | <span data-ttu-id="f7276-123">Value</span><span class="sxs-lookup"><span data-stu-id="f7276-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7276-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7276-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f7276-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f7276-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f7276-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7276-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f7276-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7276-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f7276-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f7276-128">End of client support</span></span><br/>    | <span data-ttu-id="f7276-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f7276-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="f7276-130">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f7276-130">End of server support</span></span><br/>    | <span data-ttu-id="f7276-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7276-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="f7276-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f7276-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7276-133"><dt>Msir3jp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7276-133"><dt>Msir3jp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7276-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7276-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7276-135">**WordInfo**</span><span class="sxs-lookup"><span data-stu-id="f7276-135">**WordInfo**</span></span>](wordinfo-coclass.md)
</dt> <dt>

<span data-ttu-id="f7276-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7276-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span></span>
</dt> </dl>

 

 
