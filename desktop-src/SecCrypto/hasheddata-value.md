---
description: Recupera los datos a los que se ha aplicado un algoritmo hash después de llamar correctamente al método hash.
ms.assetid: 02ba92d2-38eb-4c01-99b9-11676e7d49ff
title: HashedData. Value (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 496bdd76400c746ae3209a2e3c99b6cf4e5bc4b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670574"
---
# <a name="hasheddatavalue-property"></a><span data-ttu-id="3c2ed-103">HashedData. Value (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3c2ed-103">HashedData.Value property</span></span>

<span data-ttu-id="3c2ed-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3c2ed-105">En su lugar, use la [**clase HashAlgorithm**](/previous-versions/windows/) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="3c2ed-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="3c2ed-106">La propiedad **Value** recupera los datos con hash después de las llamadas correctas al método [**hash**](hasheddata-hash.md) .</span><span class="sxs-lookup"><span data-stu-id="3c2ed-106">The **Value** property retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="3c2ed-107">El valor hash se devuelve en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-107">The hash value is returned in hexadecimal format.</span></span> <span data-ttu-id="3c2ed-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2ed-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c2ed-109">Syntax</span></span>


```VB
HashedData.Value As String
```



## <a name="property-value"></a><span data-ttu-id="3c2ed-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3c2ed-110">Property value</span></span>

<span data-ttu-id="3c2ed-111">Cadena que contiene los datos con hash en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-111">A string that contains the hashed data in hexadecimal format.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c2ed-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c2ed-112">Remarks</span></span>

<span data-ttu-id="3c2ed-113">Para crear el hash de una gran cantidad de datos, llame al método [**hash**](hasheddata-hash.md) para cada fragmento de datos.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-113">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="3c2ed-114">El hash de cada fragmento de datos se concatena a la propiedad **Value** hasta que se lee la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-114">The hash of each piece of data is concatenated to the **Value** property until the property is read.</span></span> <span data-ttu-id="3c2ed-115">El contenido de la propiedad **Value** se restablece cuando se lee la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3c2ed-115">The contents of the **Value** property are reset when the property is read.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2ed-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c2ed-116">Requirements</span></span>



| <span data-ttu-id="3c2ed-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c2ed-117">Requirement</span></span> | <span data-ttu-id="3c2ed-118">Value</span><span class="sxs-lookup"><span data-stu-id="3c2ed-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2ed-119">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3c2ed-119">End of client support</span></span><br/> | <span data-ttu-id="3c2ed-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c2ed-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3c2ed-121">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3c2ed-121">End of server support</span></span><br/> | <span data-ttu-id="3c2ed-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c2ed-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3c2ed-123">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3c2ed-123">Redistributable</span></span><br/>       | <span data-ttu-id="3c2ed-124">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c2ed-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3c2ed-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c2ed-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3c2ed-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ed-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c2ed-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c2ed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2ed-128">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="3c2ed-128">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
