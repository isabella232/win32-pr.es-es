---
description: Recupera el valor de una propiedad con nombre para un objeto de clave de proveedor del Protocolo de Capa de sockets seguros (SSL).
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Función SslGetKeyProperty (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668351"
---
# <a name="sslgetkeyproperty-function"></a><span data-ttu-id="e1b86-103">SslGetKeyProperty función)</span><span class="sxs-lookup"><span data-stu-id="e1b86-103">SslGetKeyProperty function</span></span>

<span data-ttu-id="e1b86-104">La función **SslGetKeyProperty** recupera el valor de una propiedad con nombre para un objeto de clave de proveedor del [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="e1b86-104">The **SslGetKeyProperty** function retrieves the value of a named property for a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider key object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b86-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1b86-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e1b86-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1b86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b86-107">*hKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1b86-107">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b86-108">Identificador del proveedor SSL.</span><span class="sxs-lookup"><span data-stu-id="e1b86-108">The handle of the SSL provider.</span></span>

</dd> <dt>

<span data-ttu-id="e1b86-109">*pszProperty* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1b86-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b86-110">Puntero a una cadena Unicode terminada en null que contiene el nombre de la propiedad que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="e1b86-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span> <span data-ttu-id="e1b86-111">Puede ser uno de los [**identificadores de propiedad de almacenamiento de claves**](key-storage-property-identifiers.md) predefinidos o un identificador de propiedad personalizado.</span><span class="sxs-lookup"><span data-stu-id="e1b86-111">This can be one of the predefined [**Key Storage Property Identifiers**](key-storage-property-identifiers.md) or a custom property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e1b86-112">*ppbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e1b86-112">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b86-113">Un puntero a un búfer que recibe el valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e1b86-113">A pointer to a buffer that receives the property value.</span></span> <span data-ttu-id="e1b86-114">El autor de la llamada de la función debe liberar este búfer mediante una llamada a la función [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e1b86-114">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e1b86-115">*pcbOutput* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e1b86-115">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b86-116">Tamaño, en bytes, del búfer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="e1b86-116">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e1b86-117">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e1b86-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b86-118">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e1b86-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b86-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1b86-119">Return value</span></span>

<span data-ttu-id="e1b86-120">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e1b86-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="e1b86-121">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="e1b86-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="e1b86-122">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="e1b86-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="e1b86-123">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1b86-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="e1b86-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1b86-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="e1b86-125"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="e1b86-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="e1b86-126">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="e1b86-126">One of the provided handles is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="e1b86-127"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="e1b86-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="e1b86-128">Uno de los parámetros proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="e1b86-128">One of the supplied parameters is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e1b86-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1b86-129">Requirements</span></span>



| <span data-ttu-id="e1b86-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b86-130">Requirement</span></span> | <span data-ttu-id="e1b86-131">Value</span><span class="sxs-lookup"><span data-stu-id="e1b86-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b86-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1b86-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b86-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e1b86-133">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e1b86-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1b86-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b86-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1b86-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e1b86-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1b86-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1b86-137"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b86-137"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="e1b86-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1b86-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1b86-139"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1b86-139"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

