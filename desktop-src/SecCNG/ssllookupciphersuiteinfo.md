---
description: Recupera la información del conjunto de cifrado para un protocolo, conjunto de cifrado y tipo de clave especificados.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: Función SslLookupCipherSuiteInfo (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7aff6c9e08351ce771669535a98ec817bfc4aaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913634"
---
# <a name="ssllookupciphersuiteinfo-function"></a><span data-ttu-id="4b414-103">SslLookupCipherSuiteInfo función)</span><span class="sxs-lookup"><span data-stu-id="4b414-103">SslLookupCipherSuiteInfo function</span></span>

<span data-ttu-id="4b414-104">La función **SslLookupCipherSuiteInfo** recupera la información del conjunto de cifrado para un protocolo especificado, un conjunto de cifrado y un conjunto de tipos de clave.</span><span class="sxs-lookup"><span data-stu-id="4b414-104">The **SslLookupCipherSuiteInfo** function retrieves the cipher suite information for a specified protocol, cipher suite, and key type set.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b414-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b414-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4b414-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b414-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b414-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b414-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b414-108">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="4b414-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="4b414-109">*dwProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b414-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b414-110">Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b414-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="4b414-111">*dwCipherSuite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b414-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b414-112">Uno de los valores de los [**identificadores del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b414-112">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="4b414-113">*dwKeyType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b414-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b414-114">Uno de los valores de los [**identificadores de tipo de clave del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="4b414-114">One of the [**CNG SSL Provider Key Type Identifiers**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="4b414-115">*pCipherSuite* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4b414-115">*pCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b414-116">Dirección de un búfer que contiene una estructura [**de \_ \_ \_ conjunto de cifrado SSL de NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) en la que se va a escribir la información del conjunto de cifrado.</span><span class="sxs-lookup"><span data-stu-id="4b414-116">The address of a buffer that contains a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure in which to write the cipher suite information.</span></span>

</dd> <dt>

<span data-ttu-id="4b414-117">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b414-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b414-118">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4b414-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b414-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b414-119">Return value</span></span>

<span data-ttu-id="4b414-120">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="4b414-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="4b414-121">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4b414-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="4b414-122">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="4b414-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="4b414-123">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b414-123">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="4b414-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b414-124">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="4b414-125"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="4b414-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="4b414-126">El identificador de *hSslProvider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="4b414-126">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4b414-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b414-127">Requirements</span></span>



| <span data-ttu-id="4b414-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b414-128">Requirement</span></span> | <span data-ttu-id="4b414-129">Value</span><span class="sxs-lookup"><span data-stu-id="4b414-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b414-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b414-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4b414-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4b414-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4b414-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b414-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4b414-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b414-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4b414-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b414-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b414-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b414-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="4b414-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b414-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b414-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b414-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

