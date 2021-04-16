---
title: Método EJECT de IWMPCdrom
description: El método EJECT expulsa el CD o DVD de la unidad. | Método EJECT de IWMPCdrom
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- método EJECT Media Player de Windows
- método EJECT Media Player de Windows, interfaz IWMPCdrom
- Interfaz IWMPCdrom Windows Media Player, método EJECT
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ca2403b86b648e98861d91a21db80ddb64aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718846"
---
# <a name="iwmpcdromeject-method"></a><span data-ttu-id="72cb2-107">IWMPCdrom:: EJECT (método)</span><span class="sxs-lookup"><span data-stu-id="72cb2-107">IWMPCdrom::eject method</span></span>

<span data-ttu-id="72cb2-108">El método **EJECT** expulsa el CD o DVD de la unidad.</span><span class="sxs-lookup"><span data-stu-id="72cb2-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="72cb2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72cb2-109">Syntax</span></span>


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a><span data-ttu-id="72cb2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72cb2-110">Parameters</span></span>

<span data-ttu-id="72cb2-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="72cb2-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72cb2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72cb2-112">Return value</span></span>

<span data-ttu-id="72cb2-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="72cb2-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72cb2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72cb2-114">Remarks</span></span>

<span data-ttu-id="72cb2-115">Si la puerta de la unidad está abierta, este método cierra la puerta.</span><span class="sxs-lookup"><span data-stu-id="72cb2-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="72cb2-116">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="72cb2-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="72cb2-117">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="72cb2-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="72cb2-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="72cb2-118">Examples</span></span>

<span data-ttu-id="72cb2-119">En el ejemplo siguiente se usa **EJECT** para abrir la puerta de la unidad de CD o DVD que tiene el índice de cero en respuesta al evento click de un botón.</span><span class="sxs-lookup"><span data-stu-id="72cb2-119">The following example uses **eject** to open the door of the CD or DVD drive that has the index of zero in response to the Click event of a button.</span></span> <span data-ttu-id="72cb2-120">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="72cb2-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="72cb2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72cb2-121">Requirements</span></span>



| <span data-ttu-id="72cb2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="72cb2-122">Requirement</span></span> | <span data-ttu-id="72cb2-123">Value</span><span class="sxs-lookup"><span data-stu-id="72cb2-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72cb2-124">Versión</span><span class="sxs-lookup"><span data-stu-id="72cb2-124">Version</span></span><br/>   | <span data-ttu-id="72cb2-125">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="72cb2-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="72cb2-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72cb2-126">Namespace</span></span><br/> | <span data-ttu-id="72cb2-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="72cb2-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="72cb2-128">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="72cb2-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="72cb2-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="72cb2-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72cb2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="72cb2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72cb2-131">**AxWindowsMediaPlayer. playState (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="72cb2-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="72cb2-132">**Interfaz IWMPCdrom (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="72cb2-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="72cb2-133">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="72cb2-133">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="72cb2-134">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="72cb2-134">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





