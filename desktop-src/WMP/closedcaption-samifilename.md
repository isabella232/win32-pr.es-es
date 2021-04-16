---
title: ClosedCaption.SAMIFileName
description: La propiedad SAMIFileName especifica o recupera el nombre del archivo que contiene la información necesaria para los subtítulos (CC).
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- ClosedCaption. SAMIFileName Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699538"
---
# <a name="closedcaptionsamifilename"></a><span data-ttu-id="4dcb3-104">ClosedCaption.SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="4dcb3-104">ClosedCaption.SAMIFileName</span></span>

<span data-ttu-id="4dcb3-105">La propiedad **SAMIFileName** especifica o recupera el nombre del archivo que contiene la información necesaria para los subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="4dcb3-105">The **SAMIFileName** property specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a><span data-ttu-id="4dcb3-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4dcb3-106">Possible Values</span></span>

<span data-ttu-id="4dcb3-107">Esta propiedad es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="4dcb3-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dcb3-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dcb3-108">Remarks</span></span>

<span data-ttu-id="4dcb3-109">El archivo de intercambio multimedia accesible sincronizado (SAMI) debe utilizar una extensión de nombre de archivo. SMI o. Sami.</span><span class="sxs-lookup"><span data-stu-id="4dcb3-109">The Synchronized Accessible Media Interchange (SAMI) file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="4dcb3-110">Si no especifica un valor para **SAMIFileName**, esta propiedad recupera una cadena que contiene el nombre de archivo o la dirección URL asociada al elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="4dcb3-110">If you don't specify a value for **SAMIFileName**, this property retrieves a string containing the file name or URL associated with the current media item.</span></span> <span data-ttu-id="4dcb3-111">Esta asociación puede producirse cuando se especifica un archivo SAMI mediante el parámetro de dirección URL *Sami* , o de forma automática cuando el archivo Sami tiene el mismo nombre que el archivo multimedia digital (excepto la extensión de nombre de archivo).</span><span class="sxs-lookup"><span data-stu-id="4dcb3-111">This association can occur when a SAMI file is specified using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file name (except for the file name extension).</span></span> <span data-ttu-id="4dcb3-112">Si no hay ningún archivo SAMI asociado al medio actual, esta propiedad recupera una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="4dcb3-112">If there is no SAMI file associated with the current media, this property retrieves an empty string ("").</span></span>

<span data-ttu-id="4dcb3-113">Una vez que se especifica un valor para **SAMIFileName**, ese valor se conserva hasta que se especifique un nuevo valor (o hasta que se abra un nuevo elemento multimedia mediante el parámetro de dirección URL de *Sami* ).</span><span class="sxs-lookup"><span data-stu-id="4dcb3-113">Once you specify a value for **SAMIFileName**, that value persists until you specify a new value (or until a new media item is opened using the *sami* URL parameter).</span></span> <span data-ttu-id="4dcb3-114">Por lo tanto, debe especificar un nuevo valor para esta propiedad antes de reproducir cada nuevo elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4dcb3-114">Therefore, you must specify a new value for this property before you play each new media item.</span></span> <span data-ttu-id="4dcb3-115">De este modo, el nuevo valor de **SAMIFileName** tendrá efecto cuando se abra el siguiente elemento multimedia (o cuando el *reproductor*.\*\*\*\* se llama a Close).</span><span class="sxs-lookup"><span data-stu-id="4dcb3-115">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when *Player*.**close** is called).</span></span> <span data-ttu-id="4dcb3-116">Especificar un nuevo valor para **SAMIFileName** no tiene ningún efecto en el medio actual.</span><span class="sxs-lookup"><span data-stu-id="4dcb3-116">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="4dcb3-117">Para hacer que Windows Media Player vuelva a usar el archivo SAMI asociado a un elemento multimedia determinado, especifique un valor para **SAMIFileName** igual a una cadena vacía ("") antes de reproducir el siguiente elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4dcb3-117">To cause Windows Media Player to return to using the SAMI file associated with a particular media item, specify a value for **SAMIFileName** equal to an empty string ("") before you play the next media item.</span></span>

<span data-ttu-id="4dcb3-118">**Windows Media Player 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="4dcb3-118">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="4dcb3-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4dcb3-119">Examples</span></span>

<span data-ttu-id="4dcb3-120">En los siguientes tres ejemplos de JScript se usa *ClosedCaption*. **SAMIFileName** para especificar el nombre de un archivo de texto de subtítulos.</span><span class="sxs-lookup"><span data-stu-id="4dcb3-120">The following three JScript examples use *ClosedCaption*.**SAMIFileName** to specify the name of a closed caption text file.</span></span> <span data-ttu-id="4dcb3-121">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4dcb3-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a><span data-ttu-id="4dcb3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dcb3-122">Requirements</span></span>



| <span data-ttu-id="4dcb3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dcb3-123">Requirement</span></span> | <span data-ttu-id="4dcb3-124">Value</span><span class="sxs-lookup"><span data-stu-id="4dcb3-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4dcb3-125">Versión</span><span class="sxs-lookup"><span data-stu-id="4dcb3-125">Version</span></span><br/> | <span data-ttu-id="4dcb3-126">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="4dcb3-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4dcb3-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4dcb3-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="4dcb3-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dcb3-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dcb3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dcb3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dcb3-130">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="4dcb3-130">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="4dcb3-131">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="4dcb3-131">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="4dcb3-132">**Player. Close**</span><span class="sxs-lookup"><span data-stu-id="4dcb3-132">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





