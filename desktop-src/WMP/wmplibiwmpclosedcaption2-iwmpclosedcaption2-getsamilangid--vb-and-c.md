---
title: IWMPClosedCaption2 getSAMILangID, método
description: El método getSAMILangID devuelve el identificador de configuración regional (LCID) de un idioma admitido por el archivo SAMI actual.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- método getSAMILangID de Windows Media Player
- método getSAMILangID Windows Media Player, interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Windows Media Player, método getSAMILangID
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690903"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a><span data-ttu-id="d704e-106">IWMPClosedCaption2:: getSAMILangID (método)</span><span class="sxs-lookup"><span data-stu-id="d704e-106">IWMPClosedCaption2::getSAMILangID method</span></span>

<span data-ttu-id="d704e-107">El método **getSAMILangID** devuelve el identificador de configuración regional (LCID) de un idioma admitido por el archivo Sami actual.</span><span class="sxs-lookup"><span data-stu-id="d704e-107">The **getSAMILangID** method returns the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d704e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d704e-108">Syntax</span></span>


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a><span data-ttu-id="d704e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d704e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d704e-110">*NINDEX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d704e-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d704e-111">**System. Int32** que es el índice de base cero del LCID que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d704e-111">A **System.Int32** that is the zero-based index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d704e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d704e-112">Return value</span></span>

<span data-ttu-id="d704e-113">**System. Int32** que es el LCID del idioma con el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="d704e-113">A **System.Int32** that is the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="d704e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d704e-114">Remarks</span></span>

<span data-ttu-id="d704e-115">Los idiomas de un archivo SAMI se indizan en el orden mostrado en el archivo, empezando por cero.</span><span class="sxs-lookup"><span data-stu-id="d704e-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="d704e-116">Este método devuelve 0 a menos que haya un archivo multimedia digital abierto (AxWindowsMediaPlayer. openState es igual a 13).</span><span class="sxs-lookup"><span data-stu-id="d704e-116">This method returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="d704e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d704e-117">Requirements</span></span>



| <span data-ttu-id="d704e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d704e-118">Requirement</span></span> | <span data-ttu-id="d704e-119">Value</span><span class="sxs-lookup"><span data-stu-id="d704e-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d704e-120">Versión</span><span class="sxs-lookup"><span data-stu-id="d704e-120">Version</span></span><br/>   | <span data-ttu-id="d704e-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="d704e-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d704e-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d704e-122">Namespace</span></span><br/> | <span data-ttu-id="d704e-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d704e-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d704e-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="d704e-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d704e-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d704e-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d704e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d704e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d704e-127">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="d704e-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="d704e-128">**Interfaz IWMPClosedCaption (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d704e-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d704e-129">**Interfaz IWMPClosedCaption2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d704e-129">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





