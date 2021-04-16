---
description: Devuelve una representación de cadena de los datos codificados.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: EncodedData. Format (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650053"
---
# <a name="encodeddataformat-method"></a><span data-ttu-id="b5ac8-103">EncodedData. Format (método)</span><span class="sxs-lookup"><span data-stu-id="b5ac8-103">EncodedData.Format method</span></span>

<span data-ttu-id="b5ac8-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b5ac8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b5ac8-105">En su lugar, use la [**clase AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="b5ac8-105">Instead, use the [**AsnEncodedData Class**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b5ac8-106">El método **Format** devuelve una representación de cadena de los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="b5ac8-106">The **Format** method returns a string representation of the encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ac8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5ac8-107">Syntax</span></span>


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b5ac8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5ac8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ac8-109">*bMultiLines* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b5ac8-109">*bMultiLines* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b5ac8-110">Valor booleano que indica si la cadena devuelta contiene varias líneas.</span><span class="sxs-lookup"><span data-stu-id="b5ac8-110">Boolean value that indicates whether the returned string contains multiple lines.</span></span> <span data-ttu-id="b5ac8-111">Si **es true**, la cadena devuelta puede contener varias líneas separadas por **vbCrLf**.</span><span class="sxs-lookup"><span data-stu-id="b5ac8-111">If **True**, the returned string may contain multiple lines separated by **vbCrLf**.</span></span> <span data-ttu-id="b5ac8-112">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="b5ac8-112">The default value is **False**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ac8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5ac8-113">Return value</span></span>

<span data-ttu-id="b5ac8-114">Cadena legible que representa los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="b5ac8-114">A human-readable string that represents the encoded data.</span></span> <span data-ttu-id="b5ac8-115">Si CAPICOM no entiende los datos codificados, se devuelve una representación hexadecimal de los datos.</span><span class="sxs-lookup"><span data-stu-id="b5ac8-115">If CAPICOM does not understand the encoded data, a hexadecimal representation of the data is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ac8-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5ac8-116">Remarks</span></span>

<span data-ttu-id="b5ac8-117">El formato de la cadena devuelta puede cambiar entre las distintas versiones de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="b5ac8-117">The format of the returned string may change between different versions of CAPICOM.</span></span> <span data-ttu-id="b5ac8-118">No confíe en ningún formato determinado en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b5ac8-118">Do not rely on any particular format in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ac8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5ac8-119">Requirements</span></span>



| <span data-ttu-id="b5ac8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5ac8-120">Requirement</span></span> | <span data-ttu-id="b5ac8-121">Value</span><span class="sxs-lookup"><span data-stu-id="b5ac8-121">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ac8-122">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b5ac8-122">End of client support</span></span><br/> | <span data-ttu-id="b5ac8-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5ac8-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b5ac8-124">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b5ac8-124">End of server support</span></span><br/> | <span data-ttu-id="b5ac8-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5ac8-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b5ac8-126">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b5ac8-126">Redistributable</span></span><br/>       | <span data-ttu-id="b5ac8-127">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b5ac8-127">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b5ac8-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5ac8-128">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b5ac8-129"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5ac8-129"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ac8-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5ac8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ac8-131">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="b5ac8-131">**EncodedData**</span></span>](encodeddata.md)
</dt> </dl>

 

 
