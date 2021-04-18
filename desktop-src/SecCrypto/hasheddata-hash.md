---
description: Crea un hash de la cadena especificada.
ms.assetid: 8d3e16e7-7b93-410c-b771-7684d1bf2160
title: HashedData. hash (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Hash
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d36973340a7dbf67f8a8b0d1aa4cd5738ef97d74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670575"
---
# <a name="hasheddatahash-method"></a><span data-ttu-id="fd2bb-103">HashedData. hash (método)</span><span class="sxs-lookup"><span data-stu-id="fd2bb-103">HashedData.Hash method</span></span>

<span data-ttu-id="fd2bb-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fd2bb-105">En su lugar, use la [**clase HashAlgorithm**](/previous-versions/windows/) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="fd2bb-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="fd2bb-106">El método **hash** crea un hash de la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-106">The **Hash** method creates a hash of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd2bb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd2bb-107">Syntax</span></span>


```VB
HashedData.Hash( _
  ByVal newVal _
)
```



## <a name="parameters"></a><span data-ttu-id="fd2bb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd2bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd2bb-109">*newVal*</span><span class="sxs-lookup"><span data-stu-id="fd2bb-109">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="fd2bb-110">Cadena que contiene el valor al que se va a aplicar un algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-110">String that contains the value to hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd2bb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd2bb-111">Return value</span></span>

<span data-ttu-id="fd2bb-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd2bb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd2bb-113">Remarks</span></span>

<span data-ttu-id="fd2bb-114">Para crear el hash de una gran cantidad de datos, llame al método **hash** para cada fragmento de datos.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-114">To create the hash of a large amount of data, call the **Hash** method for each piece of data.</span></span> <span data-ttu-id="fd2bb-115">El hash de cada fragmento de datos se concatena a la propiedad [**Value**](hasheddata-value.md) hasta que se lee la propiedad.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-115">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="fd2bb-116">El contenido de la propiedad **Value** se restablece cuando se lee la propiedad.</span><span class="sxs-lookup"><span data-stu-id="fd2bb-116">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd2bb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd2bb-117">Requirements</span></span>



| <span data-ttu-id="fd2bb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd2bb-118">Requirement</span></span> | <span data-ttu-id="fd2bb-119">Value</span><span class="sxs-lookup"><span data-stu-id="fd2bb-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2bb-120">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fd2bb-120">End of client support</span></span><br/> | <span data-ttu-id="fd2bb-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd2bb-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fd2bb-122">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fd2bb-122">End of server support</span></span><br/> | <span data-ttu-id="fd2bb-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd2bb-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fd2bb-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="fd2bb-124">Redistributable</span></span><br/>       | <span data-ttu-id="fd2bb-125">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="fd2bb-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fd2bb-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd2bb-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fd2bb-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd2bb-127"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
