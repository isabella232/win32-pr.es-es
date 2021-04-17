---
title: CdromCollection. getByDriveSpecifier, método
description: El método getByDriveSpecifier recupera el objeto CDROM asociado a una letra de unidad concreta.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- método getByDriveSpecifier de Windows Media Player
- método getByDriveSpecifier de Windows Media Player, clase CdromCollection
- Clase CdromCollection Windows Media Player, método getByDriveSpecifier
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700314"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="c63c2-106">CdromCollection. getByDriveSpecifier, método</span><span class="sxs-lookup"><span data-stu-id="c63c2-106">CdromCollection.getByDriveSpecifier method</span></span>

<span data-ttu-id="c63c2-107">El método **getByDriveSpecifier** recupera el objeto **CDROM** asociado a una letra de unidad concreta.</span><span class="sxs-lookup"><span data-stu-id="c63c2-107">The **getByDriveSpecifier** method retrieves the **Cdrom** object associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c63c2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c63c2-108">Syntax</span></span>


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a><span data-ttu-id="c63c2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c63c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c63c2-110">*driveSpecifier* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c63c2-110">*driveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c63c2-111">**Cadena** que contiene la letra de unidad seguida de un carácter de dos puntos (":").</span><span class="sxs-lookup"><span data-stu-id="c63c2-111">**String** containing the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c63c2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c63c2-112">Return value</span></span>

<span data-ttu-id="c63c2-113">Este método devuelve un objeto **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="c63c2-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c63c2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c63c2-114">Remarks</span></span>

<span data-ttu-id="c63c2-115">Las letras de unidad se deben proporcionar con el formato *x*:, donde *x* representa la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="c63c2-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="c63c2-116">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c63c2-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="c63c2-117">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c63c2-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c63c2-118">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="c63c2-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="c63c2-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c63c2-119">Examples</span></span>

<span data-ttu-id="c63c2-120">En el siguiente ejemplo de JScript se usa *CdromCollection*. **getByDriveSpecifier** para recuperar el objeto **CDROM** que corresponde a una letra de unidad proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c63c2-120">The following JScript example uses *CdromCollection*.**getByDriveSpecifier** to retrieve the **Cdrom** object that corresponds to a drive letter provided by the user.</span></span> <span data-ttu-id="c63c2-121">Se creó un elemento de texto HTML, con el nombre = "monotext", para los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c63c2-121">An HTML text element was created, with NAME = "MyText", for user input.</span></span> <span data-ttu-id="c63c2-122">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c63c2-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a><span data-ttu-id="c63c2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c63c2-123">Requirements</span></span>



| <span data-ttu-id="c63c2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c63c2-124">Requirement</span></span> | <span data-ttu-id="c63c2-125">Value</span><span class="sxs-lookup"><span data-stu-id="c63c2-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c63c2-126">Versión</span><span class="sxs-lookup"><span data-stu-id="c63c2-126">Version</span></span><br/> | <span data-ttu-id="c63c2-127">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c63c2-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c63c2-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c63c2-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="c63c2-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c63c2-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c63c2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c63c2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c63c2-131">**CDROM (objeto)**</span><span class="sxs-lookup"><span data-stu-id="c63c2-131">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="c63c2-132">**CDROM. EJECT**</span><span class="sxs-lookup"><span data-stu-id="c63c2-132">**Cdrom.eject**</span></span>](cdrom-eject.md)
</dt> <dt>

[<span data-ttu-id="c63c2-133">**Objeto CdromCollection**</span><span class="sxs-lookup"><span data-stu-id="c63c2-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="c63c2-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c63c2-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c63c2-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c63c2-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





