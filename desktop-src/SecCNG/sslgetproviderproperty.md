---
description: Recupera el valor de una propiedad de proveedor especificada.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Función SslGetProviderProperty (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912285"
---
# <a name="sslgetproviderproperty-function"></a><span data-ttu-id="065a7-103">SslGetProviderProperty función)</span><span class="sxs-lookup"><span data-stu-id="065a7-103">SslGetProviderProperty function</span></span>

<span data-ttu-id="065a7-104">La función **SslGetProviderProperty** recupera el valor de una propiedad de proveedor especificada.</span><span class="sxs-lookup"><span data-stu-id="065a7-104">The **SslGetProviderProperty** function retrieves the value of a specified provider property.</span></span>

## <a name="syntax"></a><span data-ttu-id="065a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="065a7-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="065a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="065a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="065a7-107">*hSslProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="065a7-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="065a7-108">Identificador del proveedor de [*protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL) para el que se va a recuperar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="065a7-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider for which to retrieve the property.</span></span>

</dd> <dt>

<span data-ttu-id="065a7-109">*pszProperty* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="065a7-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="065a7-110">Puntero a una cadena Unicode terminada en null que contiene el nombre de la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="065a7-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="065a7-111">*ppbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="065a7-111">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="065a7-112">Dirección de un búfer que recibe el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="065a7-112">The address of a buffer that receives the property value.</span></span>

<span data-ttu-id="065a7-113">El autor de la llamada de la función debe liberar este búfer mediante una llamada a la función [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="065a7-113">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="065a7-114">*pcbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="065a7-114">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="065a7-115">Tamaño, en bytes, del búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="065a7-115">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="065a7-116">*ppEnumState* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="065a7-116">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="065a7-117">Dirección de un puntero **void** que recibe información de estado de enumeración que se utiliza en las llamadas subsiguientes a esta función.</span><span class="sxs-lookup"><span data-stu-id="065a7-117">The address of a **VOID** pointer that receives enumeration state information that is used in subsequent calls to this function.</span></span> <span data-ttu-id="065a7-118">Esta información solo tiene significado para el proveedor SSL y es opaca para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="065a7-118">This information only has meaning to the SSL provider and is opaque to the caller.</span></span> <span data-ttu-id="065a7-119">El proveedor SSL usa esta información para determinar qué elemento se encuentra a continuación en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="065a7-119">The SSL provider uses this information to determine which item is next in the enumeration.</span></span> <span data-ttu-id="065a7-120">Si la variable a la que apunta este parámetro contiene **null**, la enumeración se inicia desde el principio.</span><span class="sxs-lookup"><span data-stu-id="065a7-120">If the variable pointed to by this parameter contains **NULL**, the enumeration is started from the beginning.</span></span>

<span data-ttu-id="065a7-121">El autor de la llamada de la función debe liberar esta memoria mediante una llamada a la función [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="065a7-121">The caller of the function must free this memory by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="065a7-122">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="065a7-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="065a7-123">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="065a7-123">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="065a7-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="065a7-124">Return value</span></span>

<span data-ttu-id="065a7-125">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="065a7-125">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="065a7-126">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="065a7-126">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="065a7-127">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="065a7-127">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="065a7-128">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="065a7-128">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="065a7-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="065a7-129">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="065a7-130"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="065a7-130"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="065a7-131">No hay suficiente memoria disponible para asignar los búferes necesarios.</span><span class="sxs-lookup"><span data-stu-id="065a7-131">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="065a7-132"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="065a7-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="065a7-133">El identificador de *hSslProvider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="065a7-133">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="065a7-134"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="065a7-134"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="065a7-135">Uno de los parámetros proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="065a7-135">One of the supplied parameters is not valid.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="065a7-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="065a7-136">Requirements</span></span>



| <span data-ttu-id="065a7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="065a7-137">Requirement</span></span> | <span data-ttu-id="065a7-138">Value</span><span class="sxs-lookup"><span data-stu-id="065a7-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="065a7-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="065a7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="065a7-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="065a7-140">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="065a7-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="065a7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="065a7-142">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="065a7-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="065a7-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="065a7-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="065a7-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="065a7-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="065a7-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="065a7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="065a7-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="065a7-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

