---
title: IWMPLibrary isIdentical, método
description: El método isIdentical devuelve un valor que indica si el objeto proporcionado es igual que el actual.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- método isIdentical de Windows Media Player
- método isIdentical Windows Media Player, interfaz IWMPLibrary
- Interfaz IWMPLibrary Windows Media Player, método isIdentical
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709175"
---
# <a name="iwmplibraryisidentical-method"></a><span data-ttu-id="bcda4-106">IWMPLibrary:: isIdentical (método)</span><span class="sxs-lookup"><span data-stu-id="bcda4-106">IWMPLibrary::isIdentical method</span></span>

<span data-ttu-id="bcda4-107">El método **isIdentical** devuelve un valor que indica si el objeto proporcionado es igual que el actual.</span><span class="sxs-lookup"><span data-stu-id="bcda4-107">The **isIdentical** method returns a value that indicates whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcda4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcda4-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="bcda4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcda4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcda4-110">*pIWMPLibrary* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcda4-110">*pIWMPLibrary* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcda4-111">Una interfaz **WMPLib. IWMPLibrary** que representa el objeto que se va a comparar con el actual.</span><span class="sxs-lookup"><span data-stu-id="bcda4-111">A **WMPLib.IWMPLibrary** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcda4-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcda4-112">Return value</span></span>

<span data-ttu-id="bcda4-113">**System. Boolean** que es el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="bcda4-113">A **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="bcda4-114">El valor **true** indica que los objetos son iguales.</span><span class="sxs-lookup"><span data-stu-id="bcda4-114">The value **true** indicates that the objects are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcda4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcda4-115">Requirements</span></span>



| <span data-ttu-id="bcda4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcda4-116">Requirement</span></span> | <span data-ttu-id="bcda4-117">Value</span><span class="sxs-lookup"><span data-stu-id="bcda4-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcda4-118">Versión</span><span class="sxs-lookup"><span data-stu-id="bcda4-118">Version</span></span><br/>   | <span data-ttu-id="bcda4-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="bcda4-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="bcda4-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bcda4-120">Namespace</span></span><br/> | <span data-ttu-id="bcda4-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bcda4-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bcda4-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="bcda4-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bcda4-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bcda4-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcda4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcda4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcda4-125">**Interfaz IWMPLibrary (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="bcda4-125">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





