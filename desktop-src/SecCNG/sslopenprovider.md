---
description: Abre un identificador para el proveedor de protocolo de protocolo de Capa de sockets seguros (SSL) especificado.
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Función SslOpenProvider (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275323"
---
# <a name="sslopenprovider-function"></a><span data-ttu-id="723ba-103">SslOpenProvider función)</span><span class="sxs-lookup"><span data-stu-id="723ba-103">SslOpenProvider function</span></span>

<span data-ttu-id="723ba-104">La función **SslOpenProvider** abre un identificador para el proveedor de protocolo de [*Protocolo de capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL) especificado.</span><span class="sxs-lookup"><span data-stu-id="723ba-104">The **SslOpenProvider** function opens a handle to the specified [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="723ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="723ba-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="723ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="723ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="723ba-107">*phSslProvider* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="723ba-107">*phSslProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="723ba-108">Dirección de un **identificador de \_ Prov \_ de NCRYPT** en el que se va a escribir el identificador del proveedor.</span><span class="sxs-lookup"><span data-stu-id="723ba-108">The address of an **NCRYPT\_PROV\_HANDLE** in which to write the provider handle.</span></span>

<span data-ttu-id="723ba-109">Cuando haya terminado de usar el identificador, debe liberarlo llamando a la función [**SslFreeObject**](sslfreeobject.md) .</span><span class="sxs-lookup"><span data-stu-id="723ba-109">When you have finished using the handle, you should free it by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="723ba-110">*pszProviderName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="723ba-110">*pszProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="723ba-111">Puntero a una cadena Unicode que contiene el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="723ba-111">A pointer to a Unicode string that contains the provider name.</span></span> <span data-ttu-id="723ba-112">Si el valor de este parámetro es **null**, se devuelve un identificador **al \_ \_ proveedor de MS Schannel** .</span><span class="sxs-lookup"><span data-stu-id="723ba-112">If the value of this parameter is **NULL**, a handle to the **MS\_SCHANNEL\_PROVIDER** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="723ba-113">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="723ba-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="723ba-114">Este parámetro está reservado para un uso futuro y debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="723ba-114">This parameter is reserved for future use, and it must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="723ba-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="723ba-115">Return value</span></span>

<span data-ttu-id="723ba-116">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="723ba-116">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="723ba-117">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="723ba-117">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="723ba-118">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="723ba-118">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="723ba-119">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="723ba-119">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="723ba-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="723ba-120">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="723ba-121"><dt>**NTE \_ \_Identificador no válido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="723ba-121"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="723ba-122">Uno de los identificadores proporcionados no es válido.</span><span class="sxs-lookup"><span data-stu-id="723ba-122">One of the provided handles is not valid.</span></span><br/>                      |
| <dl> <span data-ttu-id="723ba-123"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="723ba-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="723ba-124">El parámetro *phSslProvider* o *ppProviderList* es **null**.</span><span class="sxs-lookup"><span data-stu-id="723ba-124">The *phSslProvider* or *ppProviderList* parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="723ba-125"><dt>**Estado \_ de NO hay \_ memoria**</dt> <dt>0xC0000017L</dt></span><span class="sxs-lookup"><span data-stu-id="723ba-125"><dt>**STATUS\_NO\_MEMORY**</dt> <dt>0xC0000017L</dt></span></span> </dl>      | <span data-ttu-id="723ba-126">No hay suficiente memoria disponible para asignar los búferes necesarios.</span><span class="sxs-lookup"><span data-stu-id="723ba-126">Not enough memory is available to allocate necessary buffers.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="723ba-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="723ba-127">Requirements</span></span>



| <span data-ttu-id="723ba-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="723ba-128">Requirement</span></span> | <span data-ttu-id="723ba-129">Value</span><span class="sxs-lookup"><span data-stu-id="723ba-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="723ba-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="723ba-130">Minimum supported client</span></span><br/> | <span data-ttu-id="723ba-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="723ba-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="723ba-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="723ba-132">Minimum supported server</span></span><br/> | <span data-ttu-id="723ba-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="723ba-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="723ba-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="723ba-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="723ba-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="723ba-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="723ba-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="723ba-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="723ba-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="723ba-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

