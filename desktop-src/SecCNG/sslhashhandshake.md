---
description: Devuelve un identificador para el hash del Protocolo de enlace.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Función SslHashHandshake (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002683"
---
# <a name="sslhashhandshake-function"></a><span data-ttu-id="6e823-103">SslHashHandshake función)</span><span class="sxs-lookup"><span data-stu-id="6e823-103">SslHashHandshake function</span></span>

<span data-ttu-id="6e823-104">La función **SslHashHandshake** devuelve un identificador para el hash del Protocolo de enlace.</span><span class="sxs-lookup"><span data-stu-id="6e823-104">The **SslHashHandshake** function returns a handle to the handshake hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e823-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e823-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6e823-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e823-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e823-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e823-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e823-108">Identificador de la instancia del proveedor de protocolo del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="6e823-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="6e823-109">*hHandshakeHash* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6e823-109">*hHandshakeHash* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e823-110">Identificador del objeto hash.</span><span class="sxs-lookup"><span data-stu-id="6e823-110">The handle to the hash object.</span></span>

</dd> <dt>

<span data-ttu-id="6e823-111">*pbInput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6e823-111">*pbInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e823-112">Dirección de un búfer que contiene los datos a los que se va a aplicar un algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="6e823-112">The address of a buffer that contains the data to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="6e823-113">*cbInput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e823-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e823-114">Tamaño, en bytes, del búfer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="6e823-114">The size, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6e823-115">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6e823-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e823-116">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6e823-116">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e823-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e823-117">Return value</span></span>

<span data-ttu-id="6e823-118">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="6e823-118">If the function succeeds, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e823-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e823-119">Remarks</span></span>

<span data-ttu-id="6e823-120">La función **SslHashHandshake** es una de las tres funciones que se usan para generar un hash que se usará durante el protocolo de enlace SSL.</span><span class="sxs-lookup"><span data-stu-id="6e823-120">The **SslHashHandshake** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="6e823-121">Se llama a la función [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) para obtener un identificador hash.</span><span class="sxs-lookup"><span data-stu-id="6e823-121">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="6e823-122">A la función **SslHashHandshake** se le llama cualquier número de veces con el identificador hash para agregar datos al hash.</span><span class="sxs-lookup"><span data-stu-id="6e823-122">The **SslHashHandshake** function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="6e823-123">Se llama a la función [**SslComputeFinishedHash**](sslcomputefinishedhash.md) con el identificador hash para obtener el Resumen de los datos con hash.</span><span class="sxs-lookup"><span data-stu-id="6e823-123">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e823-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e823-124">Requirements</span></span>



| <span data-ttu-id="6e823-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e823-125">Requirement</span></span> | <span data-ttu-id="6e823-126">Value</span><span class="sxs-lookup"><span data-stu-id="6e823-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e823-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e823-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6e823-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6e823-128">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6e823-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e823-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6e823-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e823-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6e823-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e823-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e823-132"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e823-132"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="6e823-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e823-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e823-134"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e823-134"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

