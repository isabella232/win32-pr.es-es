---
title: IWMPClosedCaption2 getSAMIStyleName, método
description: El método getSAMIStyleName devuelve el nombre de un estilo compatible con el archivo SAMI actual.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- método getSAMIStyleName de Windows Media Player
- método getSAMIStyleName Windows Media Player, interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Windows Media Player, método getSAMIStyleName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690895"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a><span data-ttu-id="4812d-106">IWMPClosedCaption2:: getSAMIStyleName (método)</span><span class="sxs-lookup"><span data-stu-id="4812d-106">IWMPClosedCaption2::getSAMIStyleName method</span></span>

<span data-ttu-id="4812d-107">El método **getSAMIStyleName** devuelve el nombre de un estilo compatible con el archivo Sami actual.</span><span class="sxs-lookup"><span data-stu-id="4812d-107">The **getSAMIStyleName** method returns the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4812d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4812d-108">Syntax</span></span>


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a><span data-ttu-id="4812d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4812d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4812d-110">*NINDEX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4812d-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4812d-111">**System. Int32** que es el índice de base cero del nombre de estilo que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="4812d-111">A **System.Int32** that is the zero-based index of the style name to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4812d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4812d-112">Return value</span></span>

<span data-ttu-id="4812d-113">**System. String** que es el nombre del estilo tal y como se especifica en el archivo Sami.</span><span class="sxs-lookup"><span data-stu-id="4812d-113">A **System.String** that is the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="4812d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4812d-114">Remarks</span></span>

<span data-ttu-id="4812d-115">Los estilos de un archivo SAMI se indizan en el orden mostrado en el archivo, empezando por cero.</span><span class="sxs-lookup"><span data-stu-id="4812d-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="4812d-116">Este método devuelve una cadena de longitud cero ("") a menos que haya un archivo multimedia digital abierto (AxWindowsMediaPlayer. openState es igual a 13).</span><span class="sxs-lookup"><span data-stu-id="4812d-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="4812d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4812d-117">Requirements</span></span>



| <span data-ttu-id="4812d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4812d-118">Requirement</span></span> | <span data-ttu-id="4812d-119">Value</span><span class="sxs-lookup"><span data-stu-id="4812d-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4812d-120">Versión</span><span class="sxs-lookup"><span data-stu-id="4812d-120">Version</span></span><br/>   | <span data-ttu-id="4812d-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="4812d-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4812d-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4812d-122">Namespace</span></span><br/> | <span data-ttu-id="4812d-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4812d-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4812d-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="4812d-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4812d-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4812d-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4812d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4812d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4812d-127">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="4812d-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="4812d-128">**Interfaz IWMPClosedCaption (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4812d-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4812d-129">**IWMPClosedCaption. SAMIStyle (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4812d-129">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4812d-130">**Interfaz IWMPClosedCaption2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4812d-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





