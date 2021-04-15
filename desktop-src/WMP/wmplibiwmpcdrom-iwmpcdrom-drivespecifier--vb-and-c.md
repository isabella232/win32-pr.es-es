---
title: Propiedad driveSpecifier de IWMPCdrom
description: La propiedad driveSpecifier obtiene la letra de unidad de CD o DVD.
ms.assetid: 8865232a-08a3-447b-a6d6-2bfda3a689e1
keywords:
- propiedades de driveSpecifier Media Player de Windows
- propiedad driveSpecifier de Windows Media Player, interfaz IWMPCdrom
- Interfaz IWMPCdrom Windows Media Player, propiedad driveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdrom.driveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a6c439523d90824da708700d48274f5a2e5ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708986"
---
# <a name="iwmpcdromdrivespecifier-property"></a><span data-ttu-id="13d60-106">IWMPCdrom::d propiedad riveSpecifier</span><span class="sxs-lookup"><span data-stu-id="13d60-106">IWMPCdrom::driveSpecifier property</span></span>

<span data-ttu-id="13d60-107">La propiedad **driveSpecifier** obtiene la letra de unidad de CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="13d60-107">The **driveSpecifier** property gets the CD or DVD drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d60-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13d60-108">Syntax</span></span>


```CSharp
public System.String driveSpecifier {get; set;}
```


```VB

Public ReadOnly Property driveSpecifier As System.String
```





## <a name="property-value"></a><span data-ttu-id="13d60-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="13d60-109">Property value</span></span>

<span data-ttu-id="13d60-110">**System. String** que es la letra de la unidad.</span><span class="sxs-lookup"><span data-stu-id="13d60-110">A **System.String** that is the drive letter.</span></span>

## <a name="remarks"></a><span data-ttu-id="13d60-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13d60-111">Remarks</span></span>

<span data-ttu-id="13d60-112">Normalmente, las unidades de DVD pueden reproducir un CD, pero las unidades de CD no pueden reproducir medios de DVD.</span><span class="sxs-lookup"><span data-stu-id="13d60-112">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="13d60-113">Esta propiedad obtiene una letra de unidad para un índice de unidad de base cero dentro del intervalo recuperado mediante **IWMPCdromCollection. Count**.</span><span class="sxs-lookup"><span data-stu-id="13d60-113">This property gets a drive letter for a zero-based drive index within the range retrieved using **IWMPCdromCollection.count**.</span></span> <span data-ttu-id="13d60-114">El valor recuperado toma la forma *x*:, donde *X* representa la letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="13d60-114">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="13d60-115">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="13d60-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="13d60-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="13d60-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="13d60-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="13d60-117">Examples</span></span>

<span data-ttu-id="13d60-118">En el ejemplo siguiente se usa **driveSpecifier** para crear una cadena que contiene una lista de unidades de CD y DVD disponibles y muestra esa cadena en un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="13d60-118">The following example uses **driveSpecifier** to build a string that contains a list of available CD and DVD drives and displays that string in a message box.</span></span> <span data-ttu-id="13d60-119">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="13d60-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String that will contain the list of drive specifiers.
string MyDriveSpecifiers = "Drive letters found:  ";

// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives. 
for (int i = 0; i < numDrives; i++)
{
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier;
    MyDriveSpecifiers += " ";
}

// Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers);
```


```VB

'  String that will contain the list of drive specifiers.
Dim MyDriveSpecifiers As String = &quot;Drive letters found:  &quot;

&#39;  Store the number of available drives.
Dim numDrives = player.cdromCollection.count

&#39;  Loop through the available drives. 
For i As Integer = 0 To (numDrives - 1)
    MyDriveSpecifiers += player.cdromCollection.Item(i).driveSpecifier
    MyDriveSpecifiers += &quot; &quot;
Next i

&#39;  Display the list of drive specifiers in a message box.
System.Windows.Forms.MessageBox.Show(MyDriveSpecifiers)
```





## <a name="requirements"></a><span data-ttu-id="13d60-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13d60-120">Requirements</span></span>



| <span data-ttu-id="13d60-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d60-121">Requirement</span></span> | <span data-ttu-id="13d60-122">Value</span><span class="sxs-lookup"><span data-stu-id="13d60-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d60-123">Versión</span><span class="sxs-lookup"><span data-stu-id="13d60-123">Version</span></span><br/>   | <span data-ttu-id="13d60-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="13d60-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="13d60-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13d60-125">Namespace</span></span><br/> | <span data-ttu-id="13d60-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="13d60-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="13d60-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="13d60-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="13d60-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="13d60-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d60-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="13d60-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d60-130">**Interfaz IWMPCdrom (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="13d60-130">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="13d60-131">**IWMPCdromCollection. Count (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="13d60-131">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="13d60-132">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="13d60-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="13d60-133">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="13d60-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





