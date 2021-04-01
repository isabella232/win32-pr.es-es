---
description: Exporta material de creación de claves según el estándar RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Función SslExportKeyingMaterial (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818499"
---
# <a name="sslexportkeyingmaterial-function"></a><span data-ttu-id="98c2a-103">SslExportKeyingMaterial función)</span><span class="sxs-lookup"><span data-stu-id="98c2a-103">SslExportKeyingMaterial function</span></span>

<span data-ttu-id="98c2a-104">Exporta material de creación de claves según el [estándar RFC 5705](https://tools.ietf.org/html/rfc5705).</span><span class="sxs-lookup"><span data-stu-id="98c2a-104">Exports keying material per the [RFC 5705 standard](https://tools.ietf.org/html/rfc5705).</span></span> <span data-ttu-id="98c2a-105">Esta función usa la función pseudoaleatorios de TLS para generar un búfer de bytes de material de creación de claves.</span><span class="sxs-lookup"><span data-stu-id="98c2a-105">This function uses the TLS pseudorandom function to produce a byte buffer of keying material.</span></span> <span data-ttu-id="98c2a-106">Toma una referencia al secreto principal, la etiqueta ASCII ambigüedad, los valores aleatorios de cliente y servidor y, opcionalmente, los datos de contexto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="98c2a-106">It takes a reference to the master secret, the disambiguating ASCII label, client and server random values, and optionally the application context data.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c2a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98c2a-107">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="98c2a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98c2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c2a-109">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-109">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c2a-110">Identificador de la instancia del proveedor del protocolo TLS.</span><span class="sxs-lookup"><span data-stu-id="98c2a-110">The handle of the TLS protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="98c2a-111">*hMasterKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-111">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c2a-112">Identificador del objeto de clave maestra que se utilizará para crear el material de creación de claves para br exportado.</span><span class="sxs-lookup"><span data-stu-id="98c2a-112">The handle of the master key object that will be used to create the keying material to br exported.</span></span>

</dd> <dt>

<span data-ttu-id="98c2a-113">*sLabel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-113">*sLabel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c2a-114">una cadena de etiqueta ASCII terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="98c2a-114">a NUL-terminated ASCII label string.</span></span> <span data-ttu-id="98c2a-115">Schannel quitará el carácter NUL de terminación antes de pasarlo a la función pseudoaleatorios.</span><span class="sxs-lookup"><span data-stu-id="98c2a-115">Schannel will remove the terminating NUL character before passing it to the pseudorandom function.</span></span>

</dd> <dt>

<span data-ttu-id="98c2a-116">*pbRandoms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-116">*pbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c2a-117">Un puntero a un búfer que contiene una concatenación de los valores aleatorios de *cliente \_* y de *servidor \_* de la conexión TLS.</span><span class="sxs-lookup"><span data-stu-id="98c2a-117">A pointer to a buffer that contains a concatenation of the *client\_random* and *server\_random* values of the TLS connection.</span></span>

</dd> <dt>

<span data-ttu-id="98c2a-118">*cbRandoms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-118">*cbRandoms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c2a-119">La longitud, en bytes, del búfer *pbRandoms* .</span><span class="sxs-lookup"><span data-stu-id="98c2a-119">The length, in bytes, of the *pbRandoms* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="98c2a-120">*pbContextValue* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-120">*pbContextValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="98c2a-121">Un puntero a un búfer que contiene el contexto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="98c2a-121">A pointer to a buffer that contains the application context.</span></span> <span data-ttu-id="98c2a-122">Si *pbContextValue* es **null**, *cbContextValue* debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="98c2a-122">If *pbContextValue* is **NULL**, *cbContextValue* must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="98c2a-123">*cbContextValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-123">*cbContextValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c2a-124">La longitud, en bytes, del búfer *pbContextValue* .</span><span class="sxs-lookup"><span data-stu-id="98c2a-124">The length, in bytes, of the *pbContextValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="98c2a-125">*pbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-125">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98c2a-126">La dirección de un búfer que recibe el material de creación de claves exportado.</span><span class="sxs-lookup"><span data-stu-id="98c2a-126">The address of a buffer that receives the exported keying material.</span></span> <span data-ttu-id="98c2a-127">El parámetro *cbOutput* contiene el tamaño de este búfer.</span><span class="sxs-lookup"><span data-stu-id="98c2a-127">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="98c2a-128">Este valor no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="98c2a-128">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="98c2a-129">*cbOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-129">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c2a-130">La longitud, en bytes, del búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="98c2a-130">The length, in bytes, of the *pbOutput* buffer.</span></span> <span data-ttu-id="98c2a-131">Debe ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="98c2a-131">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="98c2a-132">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98c2a-133">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="98c2a-133">Not used.</span></span> <span data-ttu-id="98c2a-134">Debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="98c2a-134">Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c2a-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98c2a-135">Return value</span></span>

<span data-ttu-id="98c2a-136">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="98c2a-136">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="98c2a-137">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="98c2a-137">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="98c2a-138">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="98c2a-138">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="98c2a-139">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98c2a-139">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="98c2a-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="98c2a-140">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="98c2a-141"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="98c2a-141"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="98c2a-142">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="98c2a-142">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="98c2a-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98c2a-143">Requirements</span></span>



| <span data-ttu-id="98c2a-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c2a-144">Requirement</span></span> | <span data-ttu-id="98c2a-145">Value</span><span class="sxs-lookup"><span data-stu-id="98c2a-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c2a-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98c2a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="98c2a-147">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-147">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="98c2a-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98c2a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="98c2a-149">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="98c2a-149">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="98c2a-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98c2a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c2a-151"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="98c2a-151"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="98c2a-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98c2a-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98c2a-153"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98c2a-153"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




