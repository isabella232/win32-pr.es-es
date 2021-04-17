---
title: AxWindowsMediaPlayer. launchURL, método
description: El método launchURL envía una dirección URL al explorador predeterminado del usuario que se va a representar. | AxWindowsMediaPlayer. launchURL, método
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- método launchURL de Windows Media Player
- método launchURL de Windows Media Player, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, método launchURL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700164"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a><span data-ttu-id="24df9-107">AxWindowsMediaPlayer. launchURL, método</span><span class="sxs-lookup"><span data-stu-id="24df9-107">AxWindowsMediaPlayer.launchURL method</span></span>

<span data-ttu-id="24df9-108">El método launchURL envía una dirección URL al explorador predeterminado del usuario que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="24df9-108">The launchURL method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="24df9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24df9-109">Syntax</span></span>


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="24df9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24df9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24df9-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="24df9-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="24df9-112">**System. String** que es la dirección URL que se va a iniciar.</span><span class="sxs-lookup"><span data-stu-id="24df9-112">The **System.String** that is the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24df9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24df9-113">Return value</span></span>

<span data-ttu-id="24df9-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="24df9-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24df9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24df9-115">Remarks</span></span>

<span data-ttu-id="24df9-116">Este método solo abre páginas web mediante los protocolos HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="24df9-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

## <a name="examples"></a><span data-ttu-id="24df9-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="24df9-117">Examples</span></span>

<span data-ttu-id="24df9-118">En el ejemplo siguiente se crea un botón que, cuando se hace clic en él, muestra el sitio web de Microsoft en una nueva ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="24df9-118">The following example creates a button that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="24df9-119">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="24df9-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="24df9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24df9-120">Requirements</span></span>



| <span data-ttu-id="24df9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="24df9-121">Requirement</span></span> | <span data-ttu-id="24df9-122">Value</span><span class="sxs-lookup"><span data-stu-id="24df9-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24df9-123">Versión</span><span class="sxs-lookup"><span data-stu-id="24df9-123">Version</span></span><br/>   | <span data-ttu-id="24df9-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="24df9-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="24df9-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24df9-125">Namespace</span></span><br/> | <span data-ttu-id="24df9-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="24df9-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="24df9-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="24df9-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="24df9-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="24df9-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24df9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="24df9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24df9-130">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="24df9-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





