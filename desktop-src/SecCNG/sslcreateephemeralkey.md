---
description: Crea una clave efímera para su uso durante la autenticación que se produce durante el protocolo de enlace del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Función SslCreateEphemeralKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648317"
---
# <a name="sslcreateephemeralkey-function"></a><span data-ttu-id="8c703-103">SslCreateEphemeralKey función)</span><span class="sxs-lookup"><span data-stu-id="8c703-103">SslCreateEphemeralKey function</span></span>

<span data-ttu-id="8c703-104">La función **SslCreateEphemeralKey** crea una clave efímera para su uso durante la autenticación que se produce durante el protocolo de enlace del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="8c703-104">The **SslCreateEphemeralKey** function creates an ephemeral key for use during the authentication that occurs during the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c703-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c703-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8c703-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c703-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c703-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c703-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c703-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="8c703-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="8c703-109">*phEphemeralKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8c703-109">*phEphemeralKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c703-110">Identificador de la clave efímera.</span><span class="sxs-lookup"><span data-stu-id="8c703-110">The handle of the ephemeral key.</span></span>

</dd> <dt>

<span data-ttu-id="8c703-111">*dwProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c703-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c703-112">Uno de los valores del [**identificador de protocolo del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="8c703-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="8c703-113">*dwCipherSuite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c703-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c703-114">Uno de los valores del [**identificador del conjunto de cifrado del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="8c703-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="8c703-115">*dwKeyType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c703-115">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c703-116">Uno de los valores del [**identificador de tipo de clave del proveedor de SSL de CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="8c703-116">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="8c703-117">Establezca este parámetro en cero para los tipos de clave que no son [*criptografía de curva elíptica*](/windows/desktop/SecGloss/e-gly) (ECC).</span><span class="sxs-lookup"><span data-stu-id="8c703-117">Set this parameter to zero for key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="8c703-118">*dwKeyBitLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c703-118">*dwKeyBitLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c703-119">Longitud, en bits, de la clave.</span><span class="sxs-lookup"><span data-stu-id="8c703-119">The length, in bits, of the key.</span></span>

</dd> <dt>

<span data-ttu-id="8c703-120">*pbParams* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c703-120">*pbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c703-121">Un puntero a un búfer para contener los parámetros de la clave que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="8c703-121">A pointer to a buffer to contain parameters for the key that is to be created.</span></span> <span data-ttu-id="8c703-122">Si no se utiliza un conjunto de cifrado del [*algoritmo de intercambio de claves (DHE) de Diffie-Hellman (efímero)*](/windows/desktop/SecGloss/d-gly) , establezca el parámetro *pbParams* en **null** y el parámetro *cbParams* en cero.</span><span class="sxs-lookup"><span data-stu-id="8c703-122">If a [*Diffie-Hellman (ephemeral) key-exchange algorithm*](/windows/desktop/SecGloss/d-gly) (DHE) cipher suite is not used, set the *pbParams* parameter to **NULL** and the *cbParams* parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="8c703-123">*cbParams* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c703-123">*cbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c703-124">La longitud, en bytes, de los datos en el búfer de *pbParams* .</span><span class="sxs-lookup"><span data-stu-id="8c703-124">The length, in bytes, of the data in the *pbParams* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8c703-125">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c703-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c703-126">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="8c703-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c703-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c703-127">Return value</span></span>

<span data-ttu-id="8c703-128">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="8c703-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="8c703-129">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8c703-129">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="8c703-130">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c703-130">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="8c703-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c703-131">Description</span></span>                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8c703-132"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="8c703-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="8c703-133">No hay memoria suficiente para asignar el búfer.</span><span class="sxs-lookup"><span data-stu-id="8c703-133">There is insufficient memory to allocate the buffer.</span></span><br/> |
| <dl> <span data-ttu-id="8c703-134"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="8c703-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="8c703-135">El identificador de *hSslProvider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="8c703-135">The *hSslProvider* handle is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="8c703-136"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="8c703-136"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="8c703-137">Uno de los parámetros proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="8c703-137">One of the supplied parameters is not valid.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="8c703-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c703-138">Remarks</span></span>

<span data-ttu-id="8c703-139">Cuando se usa un conjunto de cifrado de DHE, la implementación de SSL interna pasa los parámetros de servidor *p* y *g* a la función **SslCreateEphemeralKey** en los parámetros *pbParams* y *cbParams* .</span><span class="sxs-lookup"><span data-stu-id="8c703-139">When using a DHE cipher suite, the internal SSL implementation passes server *p* and *g* parameters to the **SslCreateEphemeralKey** function in the *pbParams* and *cbParams* parameters.</span></span>

<span data-ttu-id="8c703-140">El formato de los datos en el búfer *pbParams* es el mismo que el que se usa al establecer la propiedad [**bcrypt \_ DH \_ Parameters**](cng-property-identifiers.md) , y se inicia con una estructura de [**\_ \_ \_ encabezado de parámetro DH de bcrypt**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="8c703-140">The format of the data in the *pbParams* buffer is the same as that used when setting the [**BCRYPT\_DH\_PARAMETERS**](cng-property-identifiers.md) property, and it starts with a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c703-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c703-141">Requirements</span></span>



| <span data-ttu-id="8c703-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c703-142">Requirement</span></span> | <span data-ttu-id="8c703-143">Value</span><span class="sxs-lookup"><span data-stu-id="8c703-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c703-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c703-144">Minimum supported client</span></span><br/> | <span data-ttu-id="8c703-145">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8c703-145">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8c703-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c703-146">Minimum supported server</span></span><br/> | <span data-ttu-id="8c703-147">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c703-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8c703-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c703-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c703-149"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c703-149"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="8c703-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c703-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c703-151"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c703-151"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

