---
title: External. download (método)
description: Tenga en cuenta que en este tema se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método download inicia la descarga de un conjunto de elementos multimedia.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- método de descarga de Windows Media Player
- método de descarga de Windows Media Player, clase externa
- Clase externa Windows Media Player, método download
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698597"
---
# <a name="externaldownload-method"></a><span data-ttu-id="4de75-108">External. download (método)</span><span class="sxs-lookup"><span data-stu-id="4de75-108">External.download method</span></span>

> [!Note]  
> <span data-ttu-id="4de75-109">En este tema se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="4de75-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="4de75-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="4de75-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="4de75-111">El método **download** inicia la descarga de un conjunto de elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="4de75-111">The **download** method initiates the download of a set of media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="4de75-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4de75-112">Syntax</span></span>


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a><span data-ttu-id="4de75-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4de75-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4de75-114">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4de75-114">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de75-115">Una [constante de ubicación de biblioteca](library-location-constants.md) que especifica el tipo de elemento que se va a descargar.</span><span class="sxs-lookup"><span data-stu-id="4de75-115">A [library location constant](library-location-constants.md) that specifies the type of item to be downloaded.</span></span> <span data-ttu-id="4de75-116">Por ejemplo, CPTrackID especifica que se van a descargar una o más pistas.</span><span class="sxs-lookup"><span data-stu-id="4de75-116">For example, CPTrackID specifies that one or more tracks are to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="4de75-117">*Identificadores* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4de75-117">*IDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4de75-118">**Cadena** que contiene los identificadores, delimitados por punto y coma, de los elementos multimedia que se van a descargar.</span><span class="sxs-lookup"><span data-stu-id="4de75-118">**String** containing the IDs, delimited by semicolons, of the media items to be downloaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4de75-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4de75-119">Return value</span></span>

<span data-ttu-id="4de75-120">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4de75-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4de75-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4de75-121">Requirements</span></span>



| <span data-ttu-id="4de75-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4de75-122">Requirement</span></span> | <span data-ttu-id="4de75-123">Value</span><span class="sxs-lookup"><span data-stu-id="4de75-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4de75-124">Versión</span><span class="sxs-lookup"><span data-stu-id="4de75-124">Version</span></span><br/> | <span data-ttu-id="4de75-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="4de75-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="4de75-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4de75-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="4de75-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de75-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de75-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4de75-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de75-129">**Descargar contenido multimedia**</span><span class="sxs-lookup"><span data-stu-id="4de75-129">**Downloading Media Content**</span></span>](downloading-media-content.md)
</dt> <dt>

[<span data-ttu-id="4de75-130">**Objeto externo para las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="4de75-130">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4de75-131">**External. Buy**</span><span class="sxs-lookup"><span data-stu-id="4de75-131">**External.buy**</span></span>](external-buy.md)
</dt> <dt>

[<span data-ttu-id="4de75-132">**IWMPContentPartner::D scargar**</span><span class="sxs-lookup"><span data-stu-id="4de75-132">**IWMPContentPartner::Download**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





