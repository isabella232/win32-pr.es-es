---
title: IWMPError. Item (VB y C)
description: La propiedad Item (el \_ método get item en C \) obtiene una interfaz IWMPErrorItem en el índice especificado de la cola de errores.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- IWMPError. Item (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9217ec772512171c828dd0dad06ec8fe3704dba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690497"
---
# <a name="iwmperroritem-vb-and-c"></a><span data-ttu-id="137a7-104">IWMPError. Item (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="137a7-104">IWMPError.Item (VB and C#)</span></span>

<span data-ttu-id="137a7-105">La propiedad **Item** (el método **Get \_ Item** en C#) obtiene una interfaz **IWMPErrorItem** en el índice especificado de la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="137a7-105">The **Item** property (the **get\_Item** method in C#) gets an **IWMPErrorItem** interface at the specified index in the error queue.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="137a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="137a7-106">Parameters</span></span>

<span data-ttu-id="137a7-107">*dwIndex*</span><span class="sxs-lookup"><span data-stu-id="137a7-107">*dwIndex*</span></span>

<span data-ttu-id="137a7-108">**System. Int32** que es el índice de base cero de una interfaz **IWMPErrorItem** en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="137a7-108">A **System.Int32** that is the zero-based index of an **IWMPErrorItem** interface in the error queue.</span></span>

## <a name="property-value"></a><span data-ttu-id="137a7-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="137a7-109">Property Value</span></span>

<span data-ttu-id="137a7-110">Una interfaz **WMPLib. IWMPErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="137a7-110">A **WMPLib.IWMPErrorItem** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="137a7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="137a7-111">Remarks</span></span>

<span data-ttu-id="137a7-112">Windows Media Player puede generar una serie de errores en respuesta a una condición de error.</span><span class="sxs-lookup"><span data-stu-id="137a7-112">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="137a7-113">Esta propiedad obtiene un error específico en la cola mediante un número de índice.</span><span class="sxs-lookup"><span data-stu-id="137a7-113">This property gets a specific error in the queue by using an index number.</span></span> <span data-ttu-id="137a7-114">Los números de índice de la cola de errores comienzan por cero.</span><span class="sxs-lookup"><span data-stu-id="137a7-114">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="137a7-115">Debe establecer **IWMPSettings. enableErrorDialogs** en **false** si elige mostrar mensajes de error personalizados.</span><span class="sxs-lookup"><span data-stu-id="137a7-115">You should set **IWMPSettings.enableErrorDialogs** to **false** if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="137a7-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="137a7-116">Examples</span></span>

<span data-ttu-id="137a7-117">En el ejemplo siguiente se usa la propiedad **Item** (el método **Get \_ Item** en C#) en un controlador de eventos de error para recuperar y Mostrar información sobre el error más reciente en la cola de errores.</span><span class="sxs-lookup"><span data-stu-id="137a7-117">The following example uses the **Item** property (the **get\_Item** method in C#) in an Error event handler to retrieve and display information about the most recent error in the error queue.</span></span> <span data-ttu-id="137a7-118">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="137a7-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="137a7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="137a7-119">Requirements</span></span>



| <span data-ttu-id="137a7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="137a7-120">Requirement</span></span> | <span data-ttu-id="137a7-121">Value</span><span class="sxs-lookup"><span data-stu-id="137a7-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="137a7-122">Versión</span><span class="sxs-lookup"><span data-stu-id="137a7-122">Version</span></span><br/>   | <span data-ttu-id="137a7-123">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="137a7-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="137a7-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="137a7-124">Namespace</span></span><br/> | <span data-ttu-id="137a7-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="137a7-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="137a7-126">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="137a7-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="137a7-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="137a7-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="137a7-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="137a7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="137a7-129">**Interfaz IWMPError (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="137a7-129">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="137a7-130">**Interfaz IWMPErrorItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="137a7-130">**IWMPErrorItem Interface (VB and C#)**</span></span>](iwmperroritem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="137a7-131">**IWMPSettings. enableErrorDialogs (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="137a7-131">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





