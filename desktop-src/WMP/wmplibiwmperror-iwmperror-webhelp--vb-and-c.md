---
title: IWMPError WebHelp (método)
description: El método WebHelp inicia la página de ayuda Web de Windows Media Player para mostrar información adicional sobre el primer error en la cola de errores (índice cero). | IWMPError WebHelp (método)
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- método WebHelp Windows Media Player
- método WebHelp Windows Media Player, interfaz IWMPError
- Interfaz IWMPError Windows Media Player, método WebHelp
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709182"
---
# <a name="iwmperrorwebhelp-method"></a><span data-ttu-id="10995-107">IWMPError:: WebHelp (método)</span><span class="sxs-lookup"><span data-stu-id="10995-107">IWMPError::webHelp method</span></span>

<span data-ttu-id="10995-108">El método **WebHelp** inicia la página de ayuda Web de Windows Media Player para mostrar información adicional sobre el primer error en la cola de errores (índice cero).</span><span class="sxs-lookup"><span data-stu-id="10995-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="10995-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10995-109">Syntax</span></span>


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a><span data-ttu-id="10995-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10995-110">Parameters</span></span>

<span data-ttu-id="10995-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="10995-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10995-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10995-112">Return value</span></span>

<span data-ttu-id="10995-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="10995-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10995-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10995-114">Remarks</span></span>

<span data-ttu-id="10995-115">Las páginas de ayuda web siempre contienen la información más reciente y más detallada sobre los errores de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="10995-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="10995-116">Este método transfiere automáticamente la otra información que necesita la ayuda Web, como la versión del sistema operativo que se está usando.</span><span class="sxs-lookup"><span data-stu-id="10995-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="10995-117">Para tener acceso directamente a las páginas de ayuda Web, use el código de error y los vínculos del centro de soporte técnico siguientes:</span><span class="sxs-lookup"><span data-stu-id="10995-117">To access the Web Help pages directly, use the following error code and support center links:</span></span>

-   [<span data-ttu-id="10995-118">Información del código de error de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="10995-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="10995-119">Centro de soluciones de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="10995-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a><span data-ttu-id="10995-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="10995-120">Examples</span></span>

<span data-ttu-id="10995-121">En el ejemplo siguiente se crea un botón que inicia la página de ayuda Web de Microsoft Windows Media Player en el explorador.</span><span class="sxs-lookup"><span data-stu-id="10995-121">The following example creates a button that launches the Microsoft Windows Media Player Web Help page in the browser.</span></span> <span data-ttu-id="10995-122">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="10995-122">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="10995-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10995-123">Requirements</span></span>



| <span data-ttu-id="10995-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="10995-124">Requirement</span></span> | <span data-ttu-id="10995-125">Value</span><span class="sxs-lookup"><span data-stu-id="10995-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10995-126">Versión</span><span class="sxs-lookup"><span data-stu-id="10995-126">Version</span></span><br/>   | <span data-ttu-id="10995-127">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="10995-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="10995-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="10995-128">Namespace</span></span><br/> | <span data-ttu-id="10995-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="10995-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="10995-130">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="10995-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="10995-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="10995-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10995-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="10995-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10995-133">**Interfaz IWMPError (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="10995-133">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





