---
title: AxWindowsMediaPlayer. reproducción, método
description: El método reproducción devuelve una interfaz IWMPPlaylist para una nueva lista de reproducción.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- método reproducción de Windows Media Player
- método reproducción de Windows Media Player, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, método reproducción
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699903"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a><span data-ttu-id="32177-106">AxWindowsMediaPlayer. reproducción, método</span><span class="sxs-lookup"><span data-stu-id="32177-106">AxWindowsMediaPlayer.newPlaylist method</span></span>

<span data-ttu-id="32177-107">El método reproducción devuelve una interfaz IWMPPlaylist para una nueva lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="32177-107">The newPlaylist method returns an IWMPPlaylist interface for a new playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="32177-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32177-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a><span data-ttu-id="32177-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32177-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32177-110">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="32177-110">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="32177-111">**System. String** que es el nombre de la nueva lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="32177-111">The **System.String** that is the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="32177-112">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="32177-112">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="32177-113">**System. String** que es la dirección URL de la lista de reproducción del metarchivo de Windows Media que se usa para inicializar la nueva lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="32177-113">The **System.String** that is the URL of the Windows Media metafile playlist that is used to initialize the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32177-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32177-114">Return value</span></span>

<span data-ttu-id="32177-115">Una interfaz WMPLib. IWMPPlaylist que representa la lista de reproducción recién creada.</span><span class="sxs-lookup"><span data-stu-id="32177-115">A WMPLib.IWMPPlaylist interface that represents the newly created playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="32177-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32177-116">Remarks</span></span>

<span data-ttu-id="32177-117">Si el parámetro *bstrURL* es una cadena null o de longitud cero (""), este método crea una **lista de reproducción** vacía.</span><span class="sxs-lookup"><span data-stu-id="32177-117">If the *bstrURL* parameter is a null or zero-length string (""), this method creates an empty **playlist**.</span></span> <span data-ttu-id="32177-118">Si el parámetro *bstrName* es una cadena de longitud cero (""), este método aplica el nombre del metarchivo actual.</span><span class="sxs-lookup"><span data-stu-id="32177-118">If the *bstrName* parameter is a zero-length string (""), this method applies the current metafile name.</span></span>

<span data-ttu-id="32177-119">La nueva lista de reproducción creada con este método no se agrega a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="32177-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="32177-120">Para agregar una nueva lista de reproducción a la biblioteca, use IWMPPlaylistCollection. **importPlaylist** o IWMPPlaylistCollection. **reproducción**.</span><span class="sxs-lookup"><span data-stu-id="32177-120">To add a new playlist to the library, use IWMPPlaylistCollection.**importPlaylist** or IWMPPlaylistCollection.**newPlaylist**.</span></span> <span data-ttu-id="32177-121">Los espacios iniciales o finales del nombre de la lista de reproducción se quitan automáticamente cuando se agregan a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="32177-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="32177-122">Dado que la biblioteca permite varias listas de reproducción con el mismo nombre, es posible que desee comprobar la presencia de una lista de reproducción con un nombre determinado antes de agregar una nueva.</span><span class="sxs-lookup"><span data-stu-id="32177-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="32177-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32177-123">Requirements</span></span>



| <span data-ttu-id="32177-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="32177-124">Requirement</span></span> | <span data-ttu-id="32177-125">Value</span><span class="sxs-lookup"><span data-stu-id="32177-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32177-126">Versión</span><span class="sxs-lookup"><span data-stu-id="32177-126">Version</span></span><br/>   | <span data-ttu-id="32177-127">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="32177-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="32177-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32177-128">Namespace</span></span><br/> | <span data-ttu-id="32177-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="32177-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="32177-130">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="32177-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="32177-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="32177-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32177-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="32177-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32177-133">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="32177-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="32177-134">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="32177-134">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="32177-135">**IWMPPlaylistCollection. importPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="32177-135">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="32177-136">**IWMPPlaylistCollection. reproducción (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="32177-136">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





