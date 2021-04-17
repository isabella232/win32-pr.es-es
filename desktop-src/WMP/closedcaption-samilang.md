---
title: ClosedCaption.SAMILang
description: La propiedad SAMILang especifica o recupera el idioma que se muestra para los subtítulos (CC).
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- ClosedCaption. SAMILang Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699537"
---
# <a name="closedcaptionsamilang"></a><span data-ttu-id="76f0a-104">ClosedCaption.SAMILang</span><span class="sxs-lookup"><span data-stu-id="76f0a-104">ClosedCaption.SAMILang</span></span>

<span data-ttu-id="76f0a-105">La propiedad **SAMILang** especifica o recupera el idioma que se muestra para los subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="76f0a-105">The **SAMILang** property specifies or retrieves the language displayed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a><span data-ttu-id="76f0a-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="76f0a-106">Possible Values</span></span>

<span data-ttu-id="76f0a-107">Esta propiedad es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="76f0a-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="76f0a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76f0a-108">Remarks</span></span>

<span data-ttu-id="76f0a-109">Un archivo SAMI puede contener texto para uno o varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="76f0a-109">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="76f0a-110">Los idiomas disponibles para subtítulos (CC) se definen entre las etiquetas <STYLE> y </STYLE> del archivo Sami.</span><span class="sxs-lookup"><span data-stu-id="76f0a-110">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="76f0a-111">Un identificador de idioma se especifica con una cadena alfanumérica única precedida de un punto (.).</span><span class="sxs-lookup"><span data-stu-id="76f0a-111">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="76f0a-112">El nombre especificado para un idioma puede ser cualquier cadena.</span><span class="sxs-lookup"><span data-stu-id="76f0a-112">The name specified for a language can be any string.</span></span> <span data-ttu-id="76f0a-113">Por ejemplo, se puede utilizar lo siguiente para definir el Inglés de EE. UU.:</span><span class="sxs-lookup"><span data-stu-id="76f0a-113">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



<span data-ttu-id="76f0a-114">Si no se especifica ningún idioma SAMI, se usa de forma predeterminada el primer idioma definido en el archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="76f0a-114">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="76f0a-115">El valor que se pasa mediante *ClosedCaption*. **SAMILang** debe coincidir con el atributo **Name** del especificador de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="76f0a-115">The value you pass using *ClosedCaption*.**SAMILang** must match the **Name** attribute in the language specifier.</span></span>

<span data-ttu-id="76f0a-116">**Windows Media Player 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="76f0a-116">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="76f0a-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="76f0a-117">Examples</span></span>

<span data-ttu-id="76f0a-118">En el siguiente ejemplo de JScript se usa *ClosedCaption*. **SAMILang** en un elemento Select de HTML para especificar el idioma de la leyenda cerrada.</span><span class="sxs-lookup"><span data-stu-id="76f0a-118">The following JScript example uses *ClosedCaption*.**SAMILang** in an HTML SELECT element to specify the closed caption language.</span></span> <span data-ttu-id="76f0a-119">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="76f0a-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="76f0a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76f0a-120">Requirements</span></span>



| <span data-ttu-id="76f0a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="76f0a-121">Requirement</span></span> | <span data-ttu-id="76f0a-122">Value</span><span class="sxs-lookup"><span data-stu-id="76f0a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76f0a-123">Versión</span><span class="sxs-lookup"><span data-stu-id="76f0a-123">Version</span></span><br/> | <span data-ttu-id="76f0a-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="76f0a-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="76f0a-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="76f0a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="76f0a-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76f0a-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76f0a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="76f0a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f0a-128">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="76f0a-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="76f0a-129">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="76f0a-129">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





