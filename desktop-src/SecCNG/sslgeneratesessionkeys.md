---
description: Genera un conjunto de claves de sesión de protocolo de Capa de sockets seguros (SSL).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: Función SslGenerateSessionKeys (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cf8e20008d2a77cae3a47728f4e38fff8ae0b09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669988"
---
# <a name="sslgeneratesessionkeys-function"></a><span data-ttu-id="3f64e-103">SslGenerateSessionKeys función)</span><span class="sxs-lookup"><span data-stu-id="3f64e-103">SslGenerateSessionKeys function</span></span>

<span data-ttu-id="3f64e-104">La función **SslGenerateSessionKeys** genera un conjunto de claves de sesión de [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="3f64e-104">The **SslGenerateSessionKeys** function generates a set of [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) session keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f64e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f64e-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3f64e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f64e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f64e-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f64e-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f64e-108">Identificador de la instancia del proveedor del protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="3f64e-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="3f64e-109">*hMasterKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f64e-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f64e-110">Identificador del objeto de [*clave maestra*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="3f64e-110">The handle to the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="3f64e-111">*phReadKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f64e-111">*phReadKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f64e-112">Puntero al identificador de clave de lectura devuelto.</span><span class="sxs-lookup"><span data-stu-id="3f64e-112">A pointer to the returned read key handle.</span></span>

</dd> <dt>

<span data-ttu-id="3f64e-113">*phWriteKey* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3f64e-113">*phWriteKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f64e-114">Puntero al identificador de clave de escritura devuelto.</span><span class="sxs-lookup"><span data-stu-id="3f64e-114">A pointer to the returned write key handle.</span></span>

</dd> <dt>

<span data-ttu-id="3f64e-115">*pParameterList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f64e-115">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f64e-116">Puntero a una matriz de búferes de [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contienen información utilizada como parte de la operación de intercambio de claves.</span><span class="sxs-lookup"><span data-stu-id="3f64e-116">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="3f64e-117">El conjunto preciso de búferes depende del protocolo y el conjunto de cifrado que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3f64e-117">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="3f64e-118">Como mínimo, la lista contendrá búferes que contengan los valores aleatorios proporcionados por el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="3f64e-118">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="3f64e-119">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f64e-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f64e-120">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3f64e-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f64e-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f64e-121">Return value</span></span>

<span data-ttu-id="3f64e-122">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="3f64e-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="3f64e-123">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="3f64e-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="3f64e-124">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="3f64e-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3f64e-125">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f64e-125">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="3f64e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f64e-126">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f64e-127"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="3f64e-127"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="3f64e-128">No hay suficiente memoria disponible para asignar los búferes necesarios.</span><span class="sxs-lookup"><span data-stu-id="3f64e-128">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="3f64e-129"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="3f64e-129"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="3f64e-130">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="3f64e-130">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="3f64e-131"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="3f64e-131"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="3f64e-132">El parámetro *phReadKey* o *phWriteKey* es NULL.</span><span class="sxs-lookup"><span data-stu-id="3f64e-132">The *phReadKey* or *phWriteKey* parameter is null.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="3f64e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f64e-133">Requirements</span></span>



| <span data-ttu-id="3f64e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f64e-134">Requirement</span></span> | <span data-ttu-id="3f64e-135">Value</span><span class="sxs-lookup"><span data-stu-id="3f64e-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f64e-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f64e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3f64e-137">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3f64e-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3f64e-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f64e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3f64e-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f64e-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3f64e-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f64e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f64e-141"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f64e-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="3f64e-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f64e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f64e-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f64e-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

