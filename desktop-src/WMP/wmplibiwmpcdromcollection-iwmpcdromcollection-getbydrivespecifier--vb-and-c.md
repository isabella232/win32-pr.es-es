---
title: IWMPCdromCollection getByDriveSpecifier, método
description: El método getByDriveSpecifier devuelve una interfaz IWMPCdrom asociada a una letra de unidad concreta.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- método getByDriveSpecifier de Windows Media Player
- método getByDriveSpecifier Windows Media Player, interfaz IWMPCdromCollection
- Interfaz IWMPCdromCollection Windows Media Player, método getByDriveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe771fc893d4bf43b82dc825a2d33724926e8151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718809"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="b9310-106">IWMPCdromCollection:: getByDriveSpecifier (método)</span><span class="sxs-lookup"><span data-stu-id="b9310-106">IWMPCdromCollection::getByDriveSpecifier method</span></span>

<span data-ttu-id="b9310-107">El método **getByDriveSpecifier** devuelve una interfaz **IWMPCdrom** asociada a una letra de unidad concreta.</span><span class="sxs-lookup"><span data-stu-id="b9310-107">The **getByDriveSpecifier** method returns an **IWMPCdrom** interface associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9310-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9310-108">Syntax</span></span>


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a><span data-ttu-id="b9310-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9310-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9310-110">*bstrDriveSpecifier* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9310-110">*bstrDriveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9310-111">**System. String** que es la letra de unidad seguida de un carácter de dos puntos (":").</span><span class="sxs-lookup"><span data-stu-id="b9310-111">A **System.String** that is the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9310-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9310-112">Return value</span></span>

<span data-ttu-id="b9310-113">Una interfaz **WMPLib. IWMPCdrom** .</span><span class="sxs-lookup"><span data-stu-id="b9310-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9310-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9310-114">Remarks</span></span>

<span data-ttu-id="b9310-115">Las letras de unidad se deben proporcionar con el formato *x*:, donde *x* representa la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="b9310-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="b9310-116">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b9310-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="b9310-117">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b9310-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b9310-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b9310-118">Examples</span></span>

<span data-ttu-id="b9310-119">En el ejemplo siguiente se usa **getByDriveSpecifier** para obtener la interfaz **IWMPCdrom** que corresponde a una letra de unidad proporcionada por el usuario en un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="b9310-119">The following example uses **getByDriveSpecifier** to get the **IWMPCdrom** interface that corresponds to a drive letter provided by the user in a text box.</span></span> <span data-ttu-id="b9310-120">A continuación, se llama al método **IWMPCdrom. EJECT** para expulsar la unidad especificada.</span><span class="sxs-lookup"><span data-stu-id="b9310-120">The **IWMPCdrom.eject** method is then called to eject the specified drive.</span></span> <span data-ttu-id="b9310-121">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="b9310-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a><span data-ttu-id="b9310-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9310-122">Requirements</span></span>



| <span data-ttu-id="b9310-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9310-123">Requirement</span></span> | <span data-ttu-id="b9310-124">Value</span><span class="sxs-lookup"><span data-stu-id="b9310-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9310-125">Versión</span><span class="sxs-lookup"><span data-stu-id="b9310-125">Version</span></span><br/>   | <span data-ttu-id="b9310-126">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="b9310-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b9310-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9310-127">Namespace</span></span><br/> | <span data-ttu-id="b9310-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b9310-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b9310-129">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="b9310-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b9310-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b9310-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9310-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9310-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9310-132">**Interfaz IWMPCdrom (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b9310-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9310-133">**IWMPCdrom. EJECT (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b9310-133">**IWMPCdrom.eject (VB and C#)**</span></span>](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9310-134">**Interfaz IWMPCdromCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b9310-134">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9310-135">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b9310-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9310-136">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b9310-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





