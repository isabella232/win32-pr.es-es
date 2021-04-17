---
description: Codifica una cadena como Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Utilities. Base64Encode (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690261"
---
# <a name="utilitiesbase64encode-method"></a><span data-ttu-id="d3040-103">Utilities. Base64Encode (método)</span><span class="sxs-lookup"><span data-stu-id="d3040-103">Utilities.Base64Encode method</span></span>

<span data-ttu-id="d3040-104">\[El método **Base64Encode** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="d3040-104">\[The **Base64Encode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="d3040-105">El método **Base64Encode** codifica una cadena como Base64.</span><span class="sxs-lookup"><span data-stu-id="d3040-105">The **Base64Encode** method encodes a string as base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3040-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3040-106">Syntax</span></span>


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a><span data-ttu-id="d3040-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3040-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3040-108">*SrcString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d3040-108">*SrcString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3040-109">Cadena que se va a codificar como Base64.</span><span class="sxs-lookup"><span data-stu-id="d3040-109">The string to encode as base64.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3040-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3040-110">Return value</span></span>

<span data-ttu-id="d3040-111">Cadena codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="d3040-111">The base64-encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3040-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3040-112">Remarks</span></span>

<span data-ttu-id="d3040-113">La codificación Base64 es el esquema que se usa para transmitir datos binarios.</span><span class="sxs-lookup"><span data-stu-id="d3040-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="d3040-114">Base64 procesa los datos como grupos de 24 bits, asignando estos datos a cuatro caracteres codificados.</span><span class="sxs-lookup"><span data-stu-id="d3040-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="d3040-115">La codificación Base64 a veces se conoce como codificación de 3 a 4.</span><span class="sxs-lookup"><span data-stu-id="d3040-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="d3040-116">Cada 6 bits del grupo de 24 bits se utiliza como índice en una tabla de asignación (el alfabeto Base64) para obtener un carácter para los datos codificados.</span><span class="sxs-lookup"><span data-stu-id="d3040-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="d3040-117">Los datos codificados tienen longitudes de línea que están limitadas a 76 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d3040-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3040-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3040-118">Requirements</span></span>



| <span data-ttu-id="d3040-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3040-119">Requirement</span></span> | <span data-ttu-id="d3040-120">Value</span><span class="sxs-lookup"><span data-stu-id="d3040-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3040-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d3040-121">Redistributable</span></span><br/> | <span data-ttu-id="d3040-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="d3040-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d3040-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d3040-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="d3040-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3040-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3040-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3040-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3040-126">**Sectores públicos**</span><span class="sxs-lookup"><span data-stu-id="d3040-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




