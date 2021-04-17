---
description: Genera un número aleatorio seguro mediante el proveedor de servicios criptográficos (CSP) predeterminado.
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Utilities. GetRandom (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690371"
---
# <a name="utilitiesgetrandom-method"></a><span data-ttu-id="8f0d7-103">Utilities. GetRandom (método)</span><span class="sxs-lookup"><span data-stu-id="8f0d7-103">Utilities.GetRandom method</span></span>

<span data-ttu-id="8f0d7-104">\[El método **GetRandom** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]</span><span class="sxs-lookup"><span data-stu-id="8f0d7-104">\[The **GetRandom** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="8f0d7-105">El método **GetRandom** genera un número aleatorio seguro mediante el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-105">The **GetRandom** method generates a secure random number using the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f0d7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f0d7-106">Syntax</span></span>


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8f0d7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f0d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f0d7-108">*Longitud* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8f0d7-108">*Length* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f0d7-109">Longitud, en bytes, del número aleatorio que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-109">The length, in bytes, of the random number to create.</span></span> <span data-ttu-id="8f0d7-110">El valor predeterminado es 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-110">The default value is 8 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8f0d7-111">*EncodingType* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8f0d7-111">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f0d7-112">Un valor de la enumeración de [**\_ \_ tipo de codificación CAPICOM**](capicom-encoding-type.md) que indica el tipo de codificación que se va a utilizar para el número aleatorio generado.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-112">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the type of encoding to use for the generated random number.</span></span> <span data-ttu-id="8f0d7-113">El valor predeterminado es el \_ binario codificado de CAPICOM \_ .</span><span class="sxs-lookup"><span data-stu-id="8f0d7-113">The default value is CAPICOM\_ENCODE\_BINARY.</span></span> <span data-ttu-id="8f0d7-114">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8f0d7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8f0d7-115">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="8f0d7-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8f0d7-116">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="8f0d7-117"><dt>**CAPICOM \_ codificar \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="8f0d7-117"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="8f0d7-118">Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-118">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="8f0d7-119">Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-119">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="8f0d7-120">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-120">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="8f0d7-121"><dt>**CAPICOM, codificación \_ \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="8f0d7-121"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="8f0d7-122">Los datos se guardan como una cadena codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-122">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="8f0d7-123"><dt>**\_código binario de codificación de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8f0d7-123"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="8f0d7-124">Los datos se guardan como una secuencia binaria pura.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-124">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f0d7-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f0d7-125">Return value</span></span>

<span data-ttu-id="8f0d7-126">Una *longitud* de número de bytes generada aleatoriamente, con la codificación especificada.</span><span class="sxs-lookup"><span data-stu-id="8f0d7-126">A randomly generated number *Length* bytes long, with the specified encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f0d7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f0d7-127">Requirements</span></span>



| <span data-ttu-id="8f0d7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f0d7-128">Requirement</span></span> | <span data-ttu-id="8f0d7-129">Value</span><span class="sxs-lookup"><span data-stu-id="8f0d7-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f0d7-130">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="8f0d7-130">Redistributable</span></span><br/> | <span data-ttu-id="8f0d7-131">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f0d7-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8f0d7-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8f0d7-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="8f0d7-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f0d7-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f0d7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f0d7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f0d7-135">**Sectores públicos**</span><span class="sxs-lookup"><span data-stu-id="8f0d7-135">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 
