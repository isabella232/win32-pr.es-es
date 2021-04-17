---
title: IWMPClosedCaption2 getSAMILangName, método
description: El método getSAMILangName devuelve el nombre de un idioma admitido por el archivo SAMI actual.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- método getSAMILangName de Windows Media Player
- método getSAMILangName Windows Media Player, interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Windows Media Player, método getSAMILangName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690896"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a><span data-ttu-id="783fd-106">IWMPClosedCaption2:: getSAMILangName (método)</span><span class="sxs-lookup"><span data-stu-id="783fd-106">IWMPClosedCaption2::getSAMILangName method</span></span>

<span data-ttu-id="783fd-107">El método **getSAMILangName** devuelve el nombre de un idioma admitido por el archivo Sami actual.</span><span class="sxs-lookup"><span data-stu-id="783fd-107">The **getSAMILangName** method returns the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="783fd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="783fd-108">Syntax</span></span>


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a><span data-ttu-id="783fd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="783fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="783fd-110">*NINDEX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="783fd-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783fd-111">**System. Int32** que es el índice de base cero del nombre de idioma que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="783fd-111">**A System.Int32** that is the zero-based index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="783fd-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="783fd-112">Return value</span></span>

<span data-ttu-id="783fd-113">**System. String** que es el nombre del idioma tal como se especifica en el archivo Sami.</span><span class="sxs-lookup"><span data-stu-id="783fd-113">A **System.String** that is the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="783fd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="783fd-114">Remarks</span></span>

<span data-ttu-id="783fd-115">Los idiomas de un archivo SAMI se indizan en el orden mostrado en el archivo, empezando por cero.</span><span class="sxs-lookup"><span data-stu-id="783fd-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="783fd-116">Este método devuelve una cadena de longitud cero ("") a menos que haya un archivo multimedia digital abierto (AxWindowsMediaPlayer. openState es igual a 13).</span><span class="sxs-lookup"><span data-stu-id="783fd-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="783fd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="783fd-117">Requirements</span></span>



| <span data-ttu-id="783fd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="783fd-118">Requirement</span></span> | <span data-ttu-id="783fd-119">Value</span><span class="sxs-lookup"><span data-stu-id="783fd-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="783fd-120">Versión</span><span class="sxs-lookup"><span data-stu-id="783fd-120">Version</span></span><br/>   | <span data-ttu-id="783fd-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="783fd-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="783fd-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="783fd-122">Namespace</span></span><br/> | <span data-ttu-id="783fd-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="783fd-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="783fd-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="783fd-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="783fd-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="783fd-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="783fd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="783fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783fd-127">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="783fd-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="783fd-128">**Interfaz IWMPClosedCaption (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="783fd-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="783fd-129">**IWMPClosedCaption. SAMILang (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="783fd-129">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="783fd-130">**Interfaz IWMPClosedCaption2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="783fd-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





