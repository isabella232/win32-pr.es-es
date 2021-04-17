---
title: Propiedad SAMILang de IWMPClosedCaption
description: La propiedad SAMILang obtiene o establece el idioma que se muestra para los subtítulos (CC).
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Propiedades de SAMILang Media Player de Windows
- Propiedad SAMILang de Windows Media Player, interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Windows Media Player, propiedad SAMILang
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709196"
---
# <a name="iwmpclosedcaptionsamilang-property"></a><span data-ttu-id="250dc-106">IWMPClosedCaption:: SAMILang (propiedad)</span><span class="sxs-lookup"><span data-stu-id="250dc-106">IWMPClosedCaption::SAMILang property</span></span>

<span data-ttu-id="250dc-107">La propiedad **SAMILang** obtiene o establece el idioma que se muestra para los subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="250dc-107">The **SAMILang** property gets or sets the language displayed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="250dc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="250dc-108">Syntax</span></span>


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a><span data-ttu-id="250dc-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="250dc-109">Property value</span></span>

<span data-ttu-id="250dc-110">**System. String** que es el nombre especificado en el identificador de idioma de un archivo Sami.</span><span class="sxs-lookup"><span data-stu-id="250dc-110">The **System.String** that is the name specified in the language identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="250dc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="250dc-111">Remarks</span></span>

<span data-ttu-id="250dc-112">Un archivo SAMI puede contener texto para uno o varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="250dc-112">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="250dc-113">Los idiomas disponibles para subtítulos (CC) se definen entre las etiquetas <STYLE> y </STYLE> del archivo Sami.</span><span class="sxs-lookup"><span data-stu-id="250dc-113">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="250dc-114">Un identificador de idioma se especifica con una cadena alfanumérica única precedida de un punto (.).</span><span class="sxs-lookup"><span data-stu-id="250dc-114">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="250dc-115">El nombre especificado para un idioma puede ser cualquier cadena.</span><span class="sxs-lookup"><span data-stu-id="250dc-115">The name specified for a language can be any string.</span></span> <span data-ttu-id="250dc-116">Por ejemplo, se puede utilizar lo siguiente para definir el Inglés de EE. UU.:</span><span class="sxs-lookup"><span data-stu-id="250dc-116">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



<span data-ttu-id="250dc-117">Si no se especifica ningún idioma SAMI, se usa de forma predeterminada el primer idioma definido en el archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="250dc-117">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="250dc-118">La cadena que establezca mediante **SAMILang** debe coincidir con el atributo **Name** del especificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="250dc-118">The string you set using **SAMILang** must match the **Name** attribute in the language specifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="250dc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="250dc-119">Requirements</span></span>



| <span data-ttu-id="250dc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="250dc-120">Requirement</span></span> | <span data-ttu-id="250dc-121">Value</span><span class="sxs-lookup"><span data-stu-id="250dc-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="250dc-122">Versión</span><span class="sxs-lookup"><span data-stu-id="250dc-122">Version</span></span><br/>   | <span data-ttu-id="250dc-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="250dc-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="250dc-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="250dc-124">Namespace</span></span><br/> | <span data-ttu-id="250dc-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="250dc-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="250dc-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="250dc-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="250dc-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="250dc-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="250dc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="250dc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="250dc-129">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="250dc-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="250dc-130">**Interfaz IWMPClosedCaption (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="250dc-130">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="250dc-131">**Interfaz IWMPClosedCaption2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="250dc-131">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





