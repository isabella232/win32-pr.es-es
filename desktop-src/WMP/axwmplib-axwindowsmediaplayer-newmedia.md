---
title: AxWindowsMediaPlayer. newMedia, método
description: El método newMedia devuelve una interfaz IWMPMedia para un nuevo elemento multimedia.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- método newMedia de Windows Media Player
- método newMedia de Windows Media Player, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, método newMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699831"
---
# <a name="axwindowsmediaplayernewmedia-method"></a><span data-ttu-id="d5219-106">AxWindowsMediaPlayer. newMedia, método</span><span class="sxs-lookup"><span data-stu-id="d5219-106">AxWindowsMediaPlayer.newMedia method</span></span>

<span data-ttu-id="d5219-107">El método newMedia devuelve una interfaz IWMPMedia para un nuevo elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="d5219-107">The newMedia method returns an IWMPMedia interface for a new media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5219-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5219-108">Syntax</span></span>


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a><span data-ttu-id="d5219-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5219-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5219-110">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="d5219-110">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="d5219-111">**System. String** que es la dirección URL del archivo multimedia digital que se usa para inicializar el nuevo elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="d5219-111">A **System.String** that is the URL of the digital media file that is used to initialize the new media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5219-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5219-112">Return value</span></span>

<span data-ttu-id="d5219-113">Una interfaz WMPLib. IWMPMedia que representa el elemento multimedia que se acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="d5219-113">A WMPLib.IWMPMedia interface that represents the newly created media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5219-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5219-114">Remarks</span></span>

<span data-ttu-id="d5219-115">El parámetro *bstrURL* no debe ser una cadena de longitud cero ("") o null.</span><span class="sxs-lookup"><span data-stu-id="d5219-115">The *bstrURL* parameter must not be a zero-length string ("") or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5219-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5219-116">Requirements</span></span>



| <span data-ttu-id="d5219-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5219-117">Requirement</span></span> | <span data-ttu-id="d5219-118">Value</span><span class="sxs-lookup"><span data-stu-id="d5219-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5219-119">Versión</span><span class="sxs-lookup"><span data-stu-id="d5219-119">Version</span></span><br/>   | <span data-ttu-id="d5219-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="d5219-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d5219-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5219-121">Namespace</span></span><br/> | <span data-ttu-id="d5219-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d5219-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d5219-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="d5219-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d5219-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5219-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5219-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5219-126">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d5219-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d5219-127">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d5219-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





