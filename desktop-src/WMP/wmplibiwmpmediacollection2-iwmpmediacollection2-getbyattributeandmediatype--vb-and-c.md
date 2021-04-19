---
title: IWMPMediaCollection2 getByAttributeAndMediaType, método
description: El método getByAttributeAndMediaType devuelve una interfaz IWMPPlaylist que proporciona acceso a los elementos multimedia que tienen un atributo y un tipo de medio especificados.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- método getByAttributeAndMediaType de Windows Media Player
- método getByAttributeAndMediaType Windows Media Player, interfaz IWMPMediaCollection2
- Interfaz IWMPMediaCollection2 Windows Media Player, método getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700331"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a><span data-ttu-id="c56d2-106">IWMPMediaCollection2:: getByAttributeAndMediaType (método)</span><span class="sxs-lookup"><span data-stu-id="c56d2-106">IWMPMediaCollection2::getByAttributeAndMediaType method</span></span>

<span data-ttu-id="c56d2-107">El `getByAttributeAndMediaType` método devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia que tienen un atributo y un tipo de medio especificados.</span><span class="sxs-lookup"><span data-stu-id="c56d2-107">The `getByAttributeAndMediaType` method returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c56d2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c56d2-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a><span data-ttu-id="c56d2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c56d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c56d2-110">*bstrAttribute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c56d2-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c56d2-111">**System. String** que es el atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="c56d2-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="c56d2-112">*bstrValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c56d2-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c56d2-113">**System. String** que es el valor especificado para el atributo que se especifica en *bstrAttribute*.</span><span class="sxs-lookup"><span data-stu-id="c56d2-113">The **System.String** that is the specified value for the attribute that is specified in *bstrAttribute*.</span></span>

</dd> <dt>

<span data-ttu-id="c56d2-114">*bstrMediaType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c56d2-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c56d2-115">**System. String** que es el tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="c56d2-115">The **System.String** that is the specified media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c56d2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c56d2-116">Return value</span></span>

<span data-ttu-id="c56d2-117">Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción recuperada.</span><span class="sxs-lookup"><span data-stu-id="c56d2-117">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="c56d2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c56d2-118">Requirements</span></span>



| <span data-ttu-id="c56d2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c56d2-119">Requirement</span></span> | <span data-ttu-id="c56d2-120">Value</span><span class="sxs-lookup"><span data-stu-id="c56d2-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c56d2-121">Versión</span><span class="sxs-lookup"><span data-stu-id="c56d2-121">Version</span></span><br/>   | <span data-ttu-id="c56d2-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="c56d2-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="c56d2-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c56d2-123">Namespace</span></span><br/> | <span data-ttu-id="c56d2-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c56d2-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c56d2-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c56d2-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c56d2-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c56d2-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c56d2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c56d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56d2-128">**Interfaz IWMPMediaCollection2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c56d2-128">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c56d2-129">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c56d2-129">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





