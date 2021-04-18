---
title: IWMPLibraryServices getCountByType, método
description: El método getCountByType devuelve el número de bibliotecas disponibles de un tipo especificado.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- método getCountByType de Windows Media Player
- método getCountByType Windows Media Player, interfaz IWMPLibraryServices
- Interfaz IWMPLibraryServices Windows Media Player, método getCountByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671595"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a><span data-ttu-id="b2f80-106">IWMPLibraryServices:: getCountByType (método)</span><span class="sxs-lookup"><span data-stu-id="b2f80-106">IWMPLibraryServices::getCountByType method</span></span>

<span data-ttu-id="b2f80-107">El método **getCountByType** devuelve el número de bibliotecas disponibles de un tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="b2f80-107">The **getCountByType** method returns the count of available libraries of a specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f80-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2f80-108">Syntax</span></span>


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a><span data-ttu-id="b2f80-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2f80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2f80-110">*wmplt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2f80-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2f80-111">Un valor de la enumeración **WMPLib. WMPLibraryType** que especifica el tipo de biblioteca que se va a contar.</span><span class="sxs-lookup"><span data-stu-id="b2f80-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2f80-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2f80-112">Return value</span></span>

<span data-ttu-id="b2f80-113">**System. Int32** que es el número de bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="b2f80-113">A **System.Int32** that is the library count.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f80-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2f80-114">Requirements</span></span>



| <span data-ttu-id="b2f80-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f80-115">Requirement</span></span> | <span data-ttu-id="b2f80-116">Value</span><span class="sxs-lookup"><span data-stu-id="b2f80-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f80-117">Versión</span><span class="sxs-lookup"><span data-stu-id="b2f80-117">Version</span></span><br/>   | <span data-ttu-id="b2f80-118">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="b2f80-118">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="b2f80-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b2f80-119">Namespace</span></span><br/> | <span data-ttu-id="b2f80-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b2f80-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b2f80-121">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="b2f80-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b2f80-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b2f80-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f80-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2f80-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f80-124">**Interfaz IWMPLibraryServices (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b2f80-124">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b2f80-125">**WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="b2f80-125">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





