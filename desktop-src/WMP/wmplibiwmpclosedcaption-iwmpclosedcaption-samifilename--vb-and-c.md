---
title: Propiedad SAMIFileName de IWMPClosedCaption
description: La propiedad SAMIFileName obtiene o establece el nombre de un archivo que contiene la información necesaria para los subtítulos (CC).
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Propiedades de SAMIFileName Media Player de Windows
- Propiedad SAMIFileName de Windows Media Player, interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Windows Media Player, propiedad SAMIFileName
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649909"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a><span data-ttu-id="c5a94-106">IWMPClosedCaption:: SAMIFileName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c5a94-106">IWMPClosedCaption::SAMIFileName property</span></span>

<span data-ttu-id="c5a94-107">La propiedad **SAMIFileName** obtiene o establece el nombre de un archivo que contiene la información necesaria para los subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="c5a94-107">The **SAMIFileName** property gets or sets the name of a file containing the information needed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a94-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5a94-108">Syntax</span></span>


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a><span data-ttu-id="c5a94-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c5a94-109">Property value</span></span>

<span data-ttu-id="c5a94-110">**System. String** que es el nombre del archivo de intercambio multimedia accesible (Sami) sincronizado.</span><span class="sxs-lookup"><span data-stu-id="c5a94-110">The **System.String** that is the name of the Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5a94-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5a94-111">Remarks</span></span>

<span data-ttu-id="c5a94-112">El archivo SAMI debe utilizar una extensión de nombre de archivo. SMI o. Sami.</span><span class="sxs-lookup"><span data-stu-id="c5a94-112">The SAMI file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="c5a94-113">Si no establece un valor mediante **SAMIFileName**, esta propiedad obtiene una **cadena** que contiene el nombre de archivo o la dirección URL predeterminados asociados al elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="c5a94-113">If you do not set a value using **SAMIFileName**, this property gets a **string** containing the default file name or URL associated with the current media item.</span></span> <span data-ttu-id="c5a94-114">Esta asociación puede producirse cuando se especifica un archivo SAMI mediante el parámetro de dirección URL *Sami* , o automáticamente cuando el archivo Sami tiene el mismo nombre que el archivo multimedia digital (excepto la extensión de nombre de archivo).</span><span class="sxs-lookup"><span data-stu-id="c5a94-114">This association can occur when a SAMI file is specified by using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file (except for the file name extension).</span></span> <span data-ttu-id="c5a94-115">Si no hay ningún archivo SAMI predeterminado asociado al medio actual, esta propiedad obtiene una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="c5a94-115">If there is no default SAMI file associated with the current media, this property gets a zero-length string ("").</span></span>

<span data-ttu-id="c5a94-116">Una vez que se establece un valor mediante **SAMIFileName**, ese valor se conserva hasta que se establece un nuevo valor (o hasta que se abre un nuevo elemento multimedia mediante el parámetro de dirección URL de Sami).</span><span class="sxs-lookup"><span data-stu-id="c5a94-116">Once you set a value using **SAMIFileName**, that value persists until you set a new value (or until a new media item is opened using the sami URL parameter).</span></span> <span data-ttu-id="c5a94-117">Por lo tanto, debe establecer un nuevo valor para esta propiedad antes de reproducir cada nuevo elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="c5a94-117">Therefore, you must set a new value for this property before you play each new media item.</span></span> <span data-ttu-id="c5a94-118">De este modo, el nuevo valor de **SAMIFileName** tendrá efecto cuando se abra el siguiente elemento multimedia (o cuando se llame a **AxWindowsMediaPlayer. Close** ).</span><span class="sxs-lookup"><span data-stu-id="c5a94-118">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when **AxWindowsMediaPlayer.close** is called).</span></span> <span data-ttu-id="c5a94-119">Especificar un nuevo valor para **SAMIFileName** no tiene ningún efecto en el medio actual.</span><span class="sxs-lookup"><span data-stu-id="c5a94-119">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="c5a94-120">Para hacer que Windows Media Player use el archivo SAMI predeterminado asociado a un elemento multimedia determinado, establezca **SAMIFileName** en una cadena de longitud cero ("") antes de reproducir el siguiente elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="c5a94-120">To cause Windows Media Player to use the default SAMI file associated with a particular media item, set **SAMIFileName** to a zero-length string ("") before you play the next media item.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5a94-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5a94-121">Requirements</span></span>



| <span data-ttu-id="c5a94-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5a94-122">Requirement</span></span> | <span data-ttu-id="c5a94-123">Value</span><span class="sxs-lookup"><span data-stu-id="c5a94-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5a94-124">Versión</span><span class="sxs-lookup"><span data-stu-id="c5a94-124">Version</span></span><br/>   | <span data-ttu-id="c5a94-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="c5a94-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c5a94-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5a94-126">Namespace</span></span><br/> | <span data-ttu-id="c5a94-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c5a94-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c5a94-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c5a94-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c5a94-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c5a94-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5a94-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5a94-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a94-131">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="c5a94-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="c5a94-132">**AxWindowsMediaPlayer. Close**</span><span class="sxs-lookup"><span data-stu-id="c5a94-132">**AxWindowsMediaPlayer.close**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="c5a94-133">**Interfaz IWMPClosedCaption (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c5a94-133">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c5a94-134">**Interfaz IWMPClosedCaption2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c5a94-134">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





