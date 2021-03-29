---
title: Propiedad currentPositionTimecode de IWMPControls3
description: La propiedad currentPositionTimecode obtiene o establece la posición actual en el elemento multimedia actual mediante un formato de código de tiempo. Esta propiedad admite actualmente código de tiempo SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- propiedades de currentPositionTimecode Media Player de Windows
- propiedad currentPositionTimecode de Windows Media Player, interfaz IWMPControls3
- Interfaz IWMPControls3 Windows Media Player, propiedad currentPositionTimecode
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650140"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a><span data-ttu-id="337a4-107">IWMPControls3:: currentPositionTimecode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="337a4-107">IWMPControls3::currentPositionTimecode property</span></span>

<span data-ttu-id="337a4-108">La propiedad **currentPositionTimecode** obtiene o establece la posición actual en el elemento multimedia actual mediante un formato de código de tiempo.</span><span class="sxs-lookup"><span data-stu-id="337a4-108">The **currentPositionTimecode** property gets or sets the current position in the current media item using a time code format.</span></span> <span data-ttu-id="337a4-109">Esta propiedad admite actualmente código de tiempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="337a4-109">This property currently supports SMPTE time code.</span></span>

## <a name="syntax"></a><span data-ttu-id="337a4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="337a4-110">Syntax</span></span>


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a><span data-ttu-id="337a4-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="337a4-111">Property value</span></span>

<span data-ttu-id="337a4-112">**System. String** que es el código de tiempo de SMPTE.</span><span class="sxs-lookup"><span data-stu-id="337a4-112">A **System.String** that is the SMPTE time code.</span></span>

## <a name="remarks"></a><span data-ttu-id="337a4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="337a4-113">Remarks</span></span>

<span data-ttu-id="337a4-114">El código de tiempo SMPTE proporciona una forma estándar de identificar un fotograma de vídeo individual, que es útil para sincronizar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="337a4-114">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="337a4-115">Si un archivo multimedia digital admite código de tiempo SMPTE, Windows Media Player puede recuperar la información de posición del código de tiempo actual o buscar un fotograma de vídeo identificado por un código de tiempo determinado.</span><span class="sxs-lookup"><span data-stu-id="337a4-115">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code.</span></span>

<span data-ttu-id="337a4-116">El código de tiempo SMPTE identifica un fotograma determinado por el número de horas, minutos, segundos y fotogramas que lo separan de un marco de referencia determinado, el marco designado como tiempo cero.</span><span class="sxs-lookup"><span data-stu-id="337a4-116">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="337a4-117">Normalmente, el marco de cero de tiempo es el inicio del archivo y un valor de código de tiempo de SMPTE determinado representa el tiempo transcurrido desde el inicio del archivo.</span><span class="sxs-lookup"><span data-stu-id="337a4-117">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="337a4-118">El código de tiempo se encuentra en el intervalo de formato \[  \] *HH*:*mm*:*SS*.*FF* donde \[ *Range* \] representa el intervalo, HH representa las horas, *mm* representa los minutos, *SS* representa los segundos y *FF* representa los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="337a4-118">The time code is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, hh represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="337a4-119">Al establecer un valor para **currentPositionTimecode**, debe incluir los ocho dígitos, usando ceros como marcadores de posición.</span><span class="sxs-lookup"><span data-stu-id="337a4-119">When setting a value for **currentPositionTimecode**, you must include all eight digits, using zeros as placeholders.</span></span>

<span data-ttu-id="337a4-120">\[*intervalo* \] de corresponde al miembro **wRange** de la estructura de datos de **la \_ \_ extensión de \_ código de tiempo WMT** del formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="337a4-120">\[*range*\] corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="337a4-121">Para obtener más información acerca de los intervalos de código de tiempo, vea el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="337a4-121">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="337a4-122">La configuración y la obtención de **currentPositionTimecode** solo se admiten para los archivos que contienen información de código de tiempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="337a4-122">Setting and getting **currentPositionTimecode** is supported only for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="337a4-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="337a4-123">Examples</span></span>

<span data-ttu-id="337a4-124">En el ejemplo de código siguiente se especifica **currentPositionTimecode** como 1 hora, cero minutos, 30 segundos y 5 fotogramas.</span><span class="sxs-lookup"><span data-stu-id="337a4-124">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="337a4-125">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="337a4-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a><span data-ttu-id="337a4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="337a4-126">Requirements</span></span>



| <span data-ttu-id="337a4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="337a4-127">Requirement</span></span> | <span data-ttu-id="337a4-128">Value</span><span class="sxs-lookup"><span data-stu-id="337a4-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="337a4-129">Versión</span><span class="sxs-lookup"><span data-stu-id="337a4-129">Version</span></span><br/>   | <span data-ttu-id="337a4-130">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="337a4-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="337a4-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="337a4-131">Namespace</span></span><br/> | <span data-ttu-id="337a4-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="337a4-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="337a4-133">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="337a4-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="337a4-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="337a4-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="337a4-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="337a4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="337a4-136">**Interfaz IWMPControls3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="337a4-136">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





