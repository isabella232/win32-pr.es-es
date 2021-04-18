---
title: IWMPSettings setMode, método
description: El método setMode establece el modo de bucle o el modo de orden aleatorio en activo o inactivo.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- método setMode de Windows Media Player
- método setMode Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, método setMode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718633"
---
# <a name="iwmpsettingssetmode-method"></a><span data-ttu-id="c9246-106">IWMPSettings:: setMode (método)</span><span class="sxs-lookup"><span data-stu-id="c9246-106">IWMPSettings::setMode method</span></span>

<span data-ttu-id="c9246-107">El método **setMode** establece el modo de bucle o el modo de orden aleatorio en activo o inactivo.</span><span class="sxs-lookup"><span data-stu-id="c9246-107">The **setMode** method sets the loop mode or shuffle mode to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9246-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9246-108">Syntax</span></span>


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a><span data-ttu-id="c9246-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9246-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9246-110">*bstrMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9246-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9246-111">**System. String** que es el nombre del modo que se va a cambiar, que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c9246-111">A **System.String** that is the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="c9246-112">Value</span><span class="sxs-lookup"><span data-stu-id="c9246-112">Value</span></span>      | <span data-ttu-id="c9246-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9246-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9246-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="c9246-114">autoRewind</span></span> | <span data-ttu-id="c9246-115">Las pistas se reinician desde el principio después de la reproducción hasta el final.</span><span class="sxs-lookup"><span data-stu-id="c9246-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="c9246-116">bucle</span><span class="sxs-lookup"><span data-stu-id="c9246-116">loop</span></span>       | <span data-ttu-id="c9246-117">La secuencia de pistas se repite.</span><span class="sxs-lookup"><span data-stu-id="c9246-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="c9246-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="c9246-118">showFrame</span></span>  | <span data-ttu-id="c9246-119">El fotograma clave más cercano se muestra cuando no se reproduce.</span><span class="sxs-lookup"><span data-stu-id="c9246-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="c9246-120">Este modo no es relevante para las pistas de audio.</span><span class="sxs-lookup"><span data-stu-id="c9246-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="c9246-121">shuffle</span><span class="sxs-lookup"><span data-stu-id="c9246-121">shuffle</span></span>    | <span data-ttu-id="c9246-122">Las pistas se reproducen en orden aleatorio.</span><span class="sxs-lookup"><span data-stu-id="c9246-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> <dt>

<span data-ttu-id="c9246-123">*varfMode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c9246-123">*varfMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9246-124">Un valor **System. Boolean** que especifica si el nuevo modo especificado está activo.</span><span class="sxs-lookup"><span data-stu-id="c9246-124">A **System.Boolean** value specifying whether the new specified mode is active.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9246-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9246-125">Return value</span></span>

<span data-ttu-id="c9246-126">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c9246-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9246-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9246-127">Remarks</span></span>

<span data-ttu-id="c9246-128">Cuando el modo showFrame está activo, Windows Media Player debe tener acceso al contenido de Track para recuperar el fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c9246-128">When the showFrame mode is active, Windows Media Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="c9246-129">Utilice este modo con precaución al reproducir contenido que no sea local.</span><span class="sxs-lookup"><span data-stu-id="c9246-129">Use this mode cautiously when playing content that is not local.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9246-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9246-130">Requirements</span></span>



| <span data-ttu-id="c9246-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9246-131">Requirement</span></span> | <span data-ttu-id="c9246-132">Value</span><span class="sxs-lookup"><span data-stu-id="c9246-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9246-133">Versión</span><span class="sxs-lookup"><span data-stu-id="c9246-133">Version</span></span><br/>   | <span data-ttu-id="c9246-134">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="c9246-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c9246-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c9246-135">Namespace</span></span><br/> | <span data-ttu-id="c9246-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c9246-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c9246-137">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c9246-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c9246-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c9246-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9246-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9246-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9246-140">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c9246-140">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c9246-141">**IWMPSettings. getMode (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c9246-141">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





