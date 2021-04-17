---
title: Propiedad AxWindowsMediaPlayer. versionInfo
description: La propiedad versionInfo obtiene un valor que especifica la versión de Windows Media Player.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- propiedades de versionInfo Media Player de Windows
- propiedad versionInfo Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad versionInfo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f759c2aedb19e21c4b7d90f3634141e4c37ec8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699986"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a><span data-ttu-id="50d04-106">Propiedad AxWindowsMediaPlayer. versionInfo</span><span class="sxs-lookup"><span data-stu-id="50d04-106">AxWindowsMediaPlayer.versionInfo property</span></span>

<span data-ttu-id="50d04-107">La propiedad versionInfo obtiene un valor que especifica la versión de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="50d04-107">The versionInfo property gets a value that specifies the version of the Windows Media Player.</span></span>

<span data-ttu-id="50d04-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="50d04-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d04-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50d04-109">Syntax</span></span>


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a><span data-ttu-id="50d04-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="50d04-110">Property value</span></span>

<span data-ttu-id="50d04-111">System. String que es la información de versión con el siguiente formato: "*X*. 0,0. *Yyyy*", donde *X* representa el número de versión principal e *yyyy* representa el número de compilación.</span><span class="sxs-lookup"><span data-stu-id="50d04-111">A System.String that is the version information in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="50d04-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="50d04-112">Examples</span></span>

<span data-ttu-id="50d04-113">En el ejemplo siguiente se crea un botón que, cuando se hace clic en él, muestra un cuadro de mensaje que contiene la información de versión de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="50d04-113">The following example creates a button that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="50d04-114">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="50d04-114">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="50d04-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50d04-115">Requirements</span></span>



| <span data-ttu-id="50d04-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="50d04-116">Requirement</span></span> | <span data-ttu-id="50d04-117">Value</span><span class="sxs-lookup"><span data-stu-id="50d04-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50d04-118">Versión</span><span class="sxs-lookup"><span data-stu-id="50d04-118">Version</span></span><br/>   | <span data-ttu-id="50d04-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="50d04-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="50d04-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="50d04-120">Namespace</span></span><br/> | <span data-ttu-id="50d04-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="50d04-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="50d04-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="50d04-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="50d04-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="50d04-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50d04-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="50d04-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d04-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="50d04-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





