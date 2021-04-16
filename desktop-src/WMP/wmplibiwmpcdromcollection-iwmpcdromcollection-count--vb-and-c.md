---
title: Propiedad de recuento de IWMPCdromCollection
description: La propiedad Count obtiene el número de unidades de CD y DVD disponibles en el sistema.
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- propiedad Count de Windows Media Player
- propiedad Count de Windows Media Player, interfaz IWMPCdromCollection
- Interfaz IWMPCdromCollection Windows Media Player, propiedad Count
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718824"
---
# <a name="iwmpcdromcollectioncount-property"></a><span data-ttu-id="3e312-106">IWMPCdromCollection:: Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3e312-106">IWMPCdromCollection::count property</span></span>

<span data-ttu-id="3e312-107">La propiedad **Count** obtiene el número de unidades de CD y DVD disponibles en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3e312-107">The **count** property gets the number of available CD and DVD drives on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e312-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e312-108">Syntax</span></span>


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="3e312-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3e312-109">Property value</span></span>

<span data-ttu-id="3e312-110">**System. Int32** que es el número de unidades disponibles.</span><span class="sxs-lookup"><span data-stu-id="3e312-110">A **System.Int32** that is the count of available drives.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e312-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e312-111">Remarks</span></span>

<span data-ttu-id="3e312-112">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3e312-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="3e312-113">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3e312-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="3e312-114">Las unidades de DVD se cuentan exactamente como las unidades de CD.</span><span class="sxs-lookup"><span data-stu-id="3e312-114">DVD drives are counted exactly like CD drives.</span></span> <span data-ttu-id="3e312-115">Sin embargo, el control ActiveX de Windows Media Player solo admite la funcionalidad de DVD para Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="3e312-115">However, the Windows Media Player ActiveX control only supports DVD functionality for Windows XP or later.</span></span> <span data-ttu-id="3e312-116">Normalmente, las unidades de DVD pueden reproducir un CD, pero las unidades de CD no pueden reproducir medios de DVD.</span><span class="sxs-lookup"><span data-stu-id="3e312-116">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

## <a name="examples"></a><span data-ttu-id="3e312-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3e312-117">Examples</span></span>

<span data-ttu-id="3e312-118">En el siguiente ejemplo se usa Count para mostrar el número de unidades de CD y DVD disponibles en un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="3e312-118">The following example uses count to display the number of available CD and DVD drives in a message box.</span></span> <span data-ttu-id="3e312-119">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="3e312-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a><span data-ttu-id="3e312-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e312-120">Requirements</span></span>



| <span data-ttu-id="3e312-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e312-121">Requirement</span></span> | <span data-ttu-id="3e312-122">Value</span><span class="sxs-lookup"><span data-stu-id="3e312-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e312-123">Versión</span><span class="sxs-lookup"><span data-stu-id="3e312-123">Version</span></span><br/>   | <span data-ttu-id="3e312-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="3e312-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3e312-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e312-125">Namespace</span></span><br/> | <span data-ttu-id="3e312-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3e312-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3e312-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3e312-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3e312-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3e312-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e312-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e312-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e312-130">**Interfaz IWMPCdromCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3e312-130">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3e312-131">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3e312-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3e312-132">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3e312-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





