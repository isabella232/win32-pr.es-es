---
description: Obtiene un objeto descodificador, si existe uno.
ms.assetid: b8a1c7c9-e7ac-4b0e-a342-5b923ab83df3
title: EncodedData. decodificador (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Decoder
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 334895ed683d0c582628b4b623a7343ca561be22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650034"
---
# <a name="encodeddatadecoder-method"></a><span data-ttu-id="89543-103">EncodedData. decodificador (método)</span><span class="sxs-lookup"><span data-stu-id="89543-103">EncodedData.Decoder method</span></span>

<span data-ttu-id="89543-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="89543-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="89543-105">En su lugar, use la [**clase AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="89543-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="89543-106">El método **descodificador** obtiene un objeto descodificador, si existe uno.</span><span class="sxs-lookup"><span data-stu-id="89543-106">The **Decoder** method obtains a decoder object, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="89543-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89543-107">Syntax</span></span>


```VB
EncodedData.Decoder()
```



## <a name="parameters"></a><span data-ttu-id="89543-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89543-108">Parameters</span></span>

<span data-ttu-id="89543-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="89543-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="89543-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89543-110">Remarks</span></span>

<span data-ttu-id="89543-111">Si los datos codificados no tienen un objeto descodificador, se devuelve **null** .</span><span class="sxs-lookup"><span data-stu-id="89543-111">If the encoded data does not have a decoder object, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="89543-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89543-112">Requirements</span></span>



| <span data-ttu-id="89543-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="89543-113">Requirement</span></span> | <span data-ttu-id="89543-114">Value</span><span class="sxs-lookup"><span data-stu-id="89543-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89543-115">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="89543-115">End of client support</span></span><br/> | <span data-ttu-id="89543-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89543-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="89543-117">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="89543-117">End of server support</span></span><br/> | <span data-ttu-id="89543-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89543-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="89543-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="89543-119">Redistributable</span></span><br/>       | <span data-ttu-id="89543-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="89543-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="89543-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89543-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="89543-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89543-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
