---
title: IWMPPlaylist setItemInfo, método
description: El método setItemInfo establece el valor de un atributo de la lista de reproducción actual.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- método setItemInfo de Windows Media Player
- método setItemInfo Windows Media Player, interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Windows Media Player, método setItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce882d050f1ce7839fe3589fced3a87d9052fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709016"
---
# <a name="iwmpplaylistsetiteminfo-method"></a><span data-ttu-id="7eff5-106">IWMPPlaylist:: setItemInfo (método)</span><span class="sxs-lookup"><span data-stu-id="7eff5-106">IWMPPlaylist::setItemInfo method</span></span>

<span data-ttu-id="7eff5-107">El método **setItemInfo** establece el valor de un atributo de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="7eff5-107">The **setItemInfo** method sets the value of an attribute of the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eff5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7eff5-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="7eff5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7eff5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7eff5-110">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7eff5-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eff5-111">**System. String** que es el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="7eff5-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="7eff5-112">*bstrValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7eff5-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7eff5-113">**System. String** que es el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="7eff5-113">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7eff5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7eff5-114">Return value</span></span>

<span data-ttu-id="7eff5-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7eff5-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eff5-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7eff5-116">Remarks</span></span>

<span data-ttu-id="7eff5-117">Antes de llamar a este método, debe tener acceso total a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7eff5-117">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="7eff5-118">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7eff5-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7eff5-119">Vea la propiedad [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para ver el código de ejemplo que usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="7eff5-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eff5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eff5-120">Requirements</span></span>



| <span data-ttu-id="7eff5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eff5-121">Requirement</span></span> | <span data-ttu-id="7eff5-122">Value</span><span class="sxs-lookup"><span data-stu-id="7eff5-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eff5-123">Versión</span><span class="sxs-lookup"><span data-stu-id="7eff5-123">Version</span></span><br/>   | <span data-ttu-id="7eff5-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="7eff5-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7eff5-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7eff5-125">Namespace</span></span><br/> | <span data-ttu-id="7eff5-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7eff5-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7eff5-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="7eff5-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7eff5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7eff5-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7eff5-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eff5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eff5-130">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7eff5-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7eff5-131">**IWMPPlaylist. getItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7eff5-131">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7eff5-132">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7eff5-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7eff5-133">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="7eff5-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





