---
title: IWMPSettings baseURL (propiedad)
description: La propiedad baseURL obtiene o establece la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que se incrustan en contenido multimedia digital.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- propiedad baseURL Media Player de Windows
- propiedad baseURL Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad baseURL
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718621"
---
# <a name="iwmpsettingsbaseurl-property"></a><span data-ttu-id="50160-106">IWMPSettings:: baseURL (propiedad)</span><span class="sxs-lookup"><span data-stu-id="50160-106">IWMPSettings::baseURL property</span></span>

<span data-ttu-id="50160-107">La propiedad **baseurl** obtiene o establece la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que se incrustan en contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="50160-107">The **baseURL** property gets or sets the base URL used for relative path resolution with URL script commands that are embedded in digital media content.</span></span>

## <a name="syntax"></a><span data-ttu-id="50160-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50160-108">Syntax</span></span>


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="50160-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="50160-109">Property value</span></span>

<span data-ttu-id="50160-110">**System. String** que es la dirección URL base.</span><span class="sxs-lookup"><span data-stu-id="50160-110">A **System.String** that is the base URL.</span></span>

## <a name="remarks"></a><span data-ttu-id="50160-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50160-111">Remarks</span></span>

<span data-ttu-id="50160-112">Esta propiedad especifica la dirección URL HTTP base que se pasa como parámetro de comando por el evento **\_ \_ ScriptCommandEvent de WMPOCXEvents de AxWindowsMediaPlayer** .</span><span class="sxs-lookup"><span data-stu-id="50160-112">This property specifies the base HTTP URL that is passed as the command parameter by the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span> <span data-ttu-id="50160-113">La dirección URL base se concatena con la dirección URL relativa como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="50160-113">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="50160-114">Se agrega una barra diagonal final (/) al valor recuperado por la propiedad **baseurl** .</span><span class="sxs-lookup"><span data-stu-id="50160-114">A trailing forward slash (/) is added to the value retrieved by the **baseURL** property.</span></span>
2.  <span data-ttu-id="50160-115">Un punto inicial, una barra diagonal inversa o un carácter de barra diagonal (., \\ , y/) se eliminan de la dirección URL relativa.</span><span class="sxs-lookup"><span data-stu-id="50160-115">A leading period, backward slash, or forward slash character (., \\, and /) is deleted from the relative URL.</span></span>
3.  <span data-ttu-id="50160-116">La dirección URL relativa se agrega al final de la dirección URL base.</span><span class="sxs-lookup"><span data-stu-id="50160-116">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="50160-117">Todos los caracteres de barra diagonal en la dirección URL completa resultante se señalan en la misma dirección (convertida en barras diagonales o hacia atrás) en función de la dirección del primer carácter de barra diagonal que se encuentre en la nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="50160-117">All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="50160-118">**Note**</span><span class="sxs-lookup"><span data-stu-id="50160-118">**Note**</span></span>

<span data-ttu-id="50160-119">El control Media Player de Windows no admite el uso de dos puntos (..) en la dirección URL relativa para indicar el elemento primario de la ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="50160-119">The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

## <a name="requirements"></a><span data-ttu-id="50160-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50160-120">Requirements</span></span>



| <span data-ttu-id="50160-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="50160-121">Requirement</span></span> | <span data-ttu-id="50160-122">Value</span><span class="sxs-lookup"><span data-stu-id="50160-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50160-123">Versión</span><span class="sxs-lookup"><span data-stu-id="50160-123">Version</span></span><br/>   | <span data-ttu-id="50160-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="50160-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="50160-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="50160-125">Namespace</span></span><br/> | <span data-ttu-id="50160-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="50160-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="50160-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="50160-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="50160-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="50160-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50160-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="50160-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50160-130">**Evento AxWindowsMediaPlayer. comando (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="50160-130">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="50160-131">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="50160-131">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





