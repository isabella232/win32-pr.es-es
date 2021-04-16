---
title: Propiedad AxWindowsMediaPlayer. URL
description: La propiedad URL obtiene o establece el nombre del elemento multimedia que se va a reproducir.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- Propiedades de URL Media Player de Windows
- Propiedad URL Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad URL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699987"
---
# <a name="axwindowsmediaplayerurl-property"></a><span data-ttu-id="4ef0c-106">Propiedad AxWindowsMediaPlayer. URL</span><span class="sxs-lookup"><span data-stu-id="4ef0c-106">AxWindowsMediaPlayer.URL property</span></span>

<span data-ttu-id="4ef0c-107">La propiedad URL obtiene o establece el nombre del elemento multimedia que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-107">The URL property gets or sets the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ef0c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ef0c-108">Syntax</span></span>


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a><span data-ttu-id="4ef0c-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4ef0c-109">Property value</span></span>

<span data-ttu-id="4ef0c-110">System. String que es la dirección URL del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-110">A System.String that is the URL of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ef0c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ef0c-111">Remarks</span></span>

<span data-ttu-id="4ef0c-112">Esta propiedad solo se puede establecer en una dirección URL en una zona de seguridad que sea igual o menos restrictiva que la zona de seguridad del programa o la página web que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-112">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="4ef0c-113">Las aplicaciones que abren elementos multimedia de detrás de un firewall tendrán un mejor rendimiento si la dirección se especifica mediante el nombre del servidor de nombres de dominio (DNS) en lugar de la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-113">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="4ef0c-114">No llame a este método desde el código del controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-114">Do not call this method from event handler code.</span></span> <span data-ttu-id="4ef0c-115">La llamada a la **dirección URL** desde un controlador de eventos puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-115">Calling **URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="4ef0c-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4ef0c-116">Examples</span></span>

<span data-ttu-id="4ef0c-117">En el ejemplo siguiente se permite al usuario especificar un archivo multimedia escribiendo una ruta de acceso de archivo en un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-117">The following example allows the user to specify a media file by entering a file path in a text box.</span></span> <span data-ttu-id="4ef0c-118">Cuando se hace clic en un botón, la propiedad URL se establece en el archivo especificado y se reproduce el archivo.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-118">When a button is clicked, the URL property is set to the specified file and the file is played.</span></span> <span data-ttu-id="4ef0c-119">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="4ef0c-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4ef0c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ef0c-120">Requirements</span></span>



| <span data-ttu-id="4ef0c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ef0c-121">Requirement</span></span> | <span data-ttu-id="4ef0c-122">Value</span><span class="sxs-lookup"><span data-stu-id="4ef0c-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef0c-123">Versión</span><span class="sxs-lookup"><span data-stu-id="4ef0c-123">Version</span></span><br/>   | <span data-ttu-id="4ef0c-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="4ef0c-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4ef0c-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4ef0c-125">Namespace</span></span><br/> | <span data-ttu-id="4ef0c-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4ef0c-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4ef0c-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="4ef0c-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4ef0c-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4ef0c-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ef0c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ef0c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ef0c-130">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4ef0c-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





