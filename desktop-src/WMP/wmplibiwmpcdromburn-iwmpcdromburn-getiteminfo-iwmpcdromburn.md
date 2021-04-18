---
title: IWMPCdromBurn getItemInfo, método
description: El método getItemInfo recupera el valor del atributo especificado para el CD.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718831"
---
# <a name="iwmpcdromburngetiteminfo-method"></a><span data-ttu-id="6f5c9-106">IWMPCdromBurn:: getItemInfo (método)</span><span class="sxs-lookup"><span data-stu-id="6f5c9-106">IWMPCdromBurn::getItemInfo method</span></span>

<span data-ttu-id="6f5c9-107">El método **getItemInfo** recupera el valor del atributo especificado para el CD.</span><span class="sxs-lookup"><span data-stu-id="6f5c9-107">The **getItemInfo** method retrieves the value of the specified attribute for the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f5c9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f5c9-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="6f5c9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f5c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f5c9-110">*bstrItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f5c9-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f5c9-111">**System. String** que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6f5c9-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="6f5c9-112">Value</span><span class="sxs-lookup"><span data-stu-id="6f5c9-112">Value</span></span>         | <span data-ttu-id="6f5c9-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f5c9-113">Description</span></span>                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5c9-114">AvailableTime</span><span class="sxs-lookup"><span data-stu-id="6f5c9-114">AvailableTime</span></span> | <span data-ttu-id="6f5c9-115">Recupera la hora disponible en el CD, en segundos.</span><span class="sxs-lookup"><span data-stu-id="6f5c9-115">Retrieves the time available on the CD, in seconds.</span></span>                                          |
| <span data-ttu-id="6f5c9-116">En blanco</span><span class="sxs-lookup"><span data-stu-id="6f5c9-116">Blank</span></span>         | <span data-ttu-id="6f5c9-117">Recupera un **System. Boolean** (representado como una cadena) que indica si el CD está en blanco.</span><span class="sxs-lookup"><span data-stu-id="6f5c9-117">Retrieves a **System.Boolean** (represented as a string) indicating whether the CD is blank.</span></span> |
| <span data-ttu-id="6f5c9-118">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="6f5c9-118">FreeSpace</span></span>     | <span data-ttu-id="6f5c9-119">Recupera el espacio disponible en el CD, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6f5c9-119">Retrieves the free space on the CD, in bytes.</span></span>                                                |
| <span data-ttu-id="6f5c9-120">TotalSpace</span><span class="sxs-lookup"><span data-stu-id="6f5c9-120">TotalSpace</span></span>    | <span data-ttu-id="6f5c9-121">Recupera el espacio total en el CD, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6f5c9-121">Retrieves the total space on the CD, in bytes.</span></span>                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f5c9-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f5c9-122">Return value</span></span>

<span data-ttu-id="6f5c9-123">**System. String** que es el valor del atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="6f5c9-123">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f5c9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f5c9-124">Requirements</span></span>



| <span data-ttu-id="6f5c9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f5c9-125">Requirement</span></span> | <span data-ttu-id="6f5c9-126">Value</span><span class="sxs-lookup"><span data-stu-id="6f5c9-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f5c9-127">Versión</span><span class="sxs-lookup"><span data-stu-id="6f5c9-127">Version</span></span><br/>   | <span data-ttu-id="6f5c9-128">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="6f5c9-128">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="6f5c9-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f5c9-129">Namespace</span></span><br/> | <span data-ttu-id="6f5c9-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6f5c9-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6f5c9-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="6f5c9-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6f5c9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6f5c9-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f5c9-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f5c9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f5c9-134">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6f5c9-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





