---
title: Propiedad AxWindowsMediaPlayer. cdromCollection
description: La propiedad cdromCollection obtiene una interfaz IWMPCdromCollection que proporciona acceso a una colección de unidades de CD o DVD.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- propiedades de cdromCollection Media Player de Windows
- propiedad cdromCollection Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad cdromCollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698480"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a><span data-ttu-id="2b624-106">Propiedad AxWindowsMediaPlayer. cdromCollection</span><span class="sxs-lookup"><span data-stu-id="2b624-106">AxWindowsMediaPlayer.cdromCollection property</span></span>

<span data-ttu-id="2b624-107">La propiedad cdromCollection obtiene una interfaz **IWMPCdromCollection** que proporciona acceso a una colección de unidades de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="2b624-107">The cdromCollection property gets an **IWMPCdromCollection** interface that provides access to a collection of CD or DVD drives.</span></span>

<span data-ttu-id="2b624-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2b624-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b624-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b624-109">Syntax</span></span>


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a><span data-ttu-id="2b624-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2b624-110">Property value</span></span>

<span data-ttu-id="2b624-111">Una interfaz WMPLib. IWMPCdromCollection.</span><span class="sxs-lookup"><span data-stu-id="2b624-111">A WMPLib.IWMPCdromCollection interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b624-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b624-112">Remarks</span></span>

<span data-ttu-id="2b624-113">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2b624-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="2b624-114">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2b624-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b624-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b624-115">Requirements</span></span>



| <span data-ttu-id="2b624-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b624-116">Requirement</span></span> | <span data-ttu-id="2b624-117">Value</span><span class="sxs-lookup"><span data-stu-id="2b624-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b624-118">Versión</span><span class="sxs-lookup"><span data-stu-id="2b624-118">Version</span></span><br/>   | <span data-ttu-id="2b624-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="2b624-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2b624-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2b624-120">Namespace</span></span><br/> | <span data-ttu-id="2b624-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2b624-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2b624-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="2b624-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2b624-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2b624-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b624-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b624-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b624-125">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2b624-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b624-126">**Interfaz IWMPCdromCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2b624-126">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b624-127">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2b624-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2b624-128">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2b624-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





