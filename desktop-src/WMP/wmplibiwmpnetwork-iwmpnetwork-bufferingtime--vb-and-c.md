---
title: Propiedad bufferingTime de IWMPNetwork
description: La propiedad bufferingTime obtiene o establece la cantidad de tiempo en milisegundos asignados para almacenar en búfer los datos entrantes antes de que empiece la reproducción.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- propiedades de bufferingTime Media Player de Windows
- propiedad bufferingTime de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad bufferingTime
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8594d53797b028dd74a8ef11cb8f2fa64b3654cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698573"
---
# <a name="iwmpnetworkbufferingtime-property"></a><span data-ttu-id="1fc62-106">IWMPNetwork:: bufferingTime (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1fc62-106">IWMPNetwork::bufferingTime property</span></span>

<span data-ttu-id="1fc62-107">La propiedad **bufferingTime** obtiene o establece la cantidad de tiempo en milisegundos asignados para almacenar en búfer los datos entrantes antes de que empiece la reproducción.</span><span class="sxs-lookup"><span data-stu-id="1fc62-107">The **bufferingTime** property gets or sets the amount of time in milliseconds allocated for buffering incoming data before playback begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc62-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fc62-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="1fc62-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1fc62-109">Property value</span></span>

<span data-ttu-id="1fc62-110">**System. Int32** que es el tiempo de almacenamiento en milisegundos, que oscila entre cero y 60.000 con un valor predeterminado de 5.000.</span><span class="sxs-lookup"><span data-stu-id="1fc62-110">A **System.Int32** that is the buffering time in milliseconds, which ranges from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="1fc62-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1fc62-111">Examples</span></span>

<span data-ttu-id="1fc62-112">En el ejemplo de código siguiente se usa **bufferingTime** para especificar el número de segundos asignados para almacenar en búfer los datos entrantes.</span><span class="sxs-lookup"><span data-stu-id="1fc62-112">The following code example uses **bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="1fc62-113">Un cuadro de texto permite al usuario especificar un nuevo valor para **bufferingTime**, y la propiedad se actualiza en respuesta al evento click de un botón.</span><span class="sxs-lookup"><span data-stu-id="1fc62-113">A text box allows the user to enter a new value for **bufferingTime**, and the property is updated in response to the Click event of a button.</span></span> <span data-ttu-id="1fc62-114">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="1fc62-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1fc62-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc62-115">Requirements</span></span>



| <span data-ttu-id="1fc62-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc62-116">Requirement</span></span> | <span data-ttu-id="1fc62-117">Value</span><span class="sxs-lookup"><span data-stu-id="1fc62-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc62-118">Versión</span><span class="sxs-lookup"><span data-stu-id="1fc62-118">Version</span></span><br/>   | <span data-ttu-id="1fc62-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="1fc62-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1fc62-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1fc62-120">Namespace</span></span><br/> | <span data-ttu-id="1fc62-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1fc62-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1fc62-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="1fc62-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1fc62-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1fc62-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fc62-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fc62-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc62-125">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1fc62-125">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





