---
description: Devuelve una matriz de proveedores de protocolo de protocolo Capa de sockets seguros (SSL) instalados.
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: Función SslEnumProtocolProviders (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 94c8648950af20a97bcc34b614aee0d0f716b043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279311"
---
# <a name="sslenumprotocolproviders-function"></a><span data-ttu-id="96af7-103">SslEnumProtocolProviders función)</span><span class="sxs-lookup"><span data-stu-id="96af7-103">SslEnumProtocolProviders function</span></span>

<span data-ttu-id="96af7-104">La función **SslEnumProtocolProviders** devuelve una matriz de proveedores de protocolos de [*Protocolo capa de sockets seguros*](/windows/desktop/SecGloss/s-gly) (SSL) instalados.</span><span class="sxs-lookup"><span data-stu-id="96af7-104">The **SslEnumProtocolProviders** function returns an array of installed [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol providers.</span></span>

## <a name="syntax"></a><span data-ttu-id="96af7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96af7-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="96af7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96af7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96af7-107">*pdwProviderCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="96af7-107">*pdwProviderCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96af7-108">Un puntero a un valor **DWORD** para recibir el número de proveedores de protocolo devueltos.</span><span class="sxs-lookup"><span data-stu-id="96af7-108">A pointer to a **DWORD** value to receive the number of protocol providers returned.</span></span>

</dd> <dt>

<span data-ttu-id="96af7-109">*ppProviderList* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="96af7-109">*ppProviderList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96af7-110">Un puntero a un búfer que recibe la matriz de estructuras [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) .</span><span class="sxs-lookup"><span data-stu-id="96af7-110">A pointer to a buffer that receives the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures.</span></span>

</dd> <dt>

<span data-ttu-id="96af7-111">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="96af7-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96af7-112">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="96af7-112">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96af7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96af7-113">Return value</span></span>

<span data-ttu-id="96af7-114">Si la función se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="96af7-114">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="96af7-115">Si se produce un error en la función, devuelve un valor de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="96af7-115">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="96af7-116">Los códigos de retorno posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="96af7-116">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="96af7-117">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96af7-117">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="96af7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="96af7-118">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96af7-119"><dt>**NTE \_ \_Marcas no válidas**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="96af7-119"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="96af7-120">El parámetro *dwFlags* no es cero.</span><span class="sxs-lookup"><span data-stu-id="96af7-120">The *dwFlags* parameter is not zero.</span></span><br/>                              |
| <dl> <span data-ttu-id="96af7-121"><dt>**NTE \_ NO hay \_ memoria**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="96af7-121"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="96af7-122">No hay suficiente memoria disponible para asignar los búferes necesarios.</span><span class="sxs-lookup"><span data-stu-id="96af7-122">Not enough memory is available to allocate necessary buffers.</span></span><br/>     |
| <dl> <span data-ttu-id="96af7-123"><dt>**NTE \_ \_Parámetro no válido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="96af7-123"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="96af7-124">El parámetro *pdwProviderCount* o *ppProviderList* es **null**.</span><span class="sxs-lookup"><span data-stu-id="96af7-124">The *pdwProviderCount* or *ppProviderList* parameter is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96af7-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="96af7-125">Remarks</span></span>

<span data-ttu-id="96af7-126">Cuando haya terminado de usar la matriz de estructuras [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) , llame a la función [**SslFreeBuffer**](sslfreebuffer.md) para liberar la matriz.</span><span class="sxs-lookup"><span data-stu-id="96af7-126">When you have finished using the array of [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) structures, call the [**SslFreeBuffer**](sslfreebuffer.md) function to free the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="96af7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96af7-127">Requirements</span></span>



| <span data-ttu-id="96af7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="96af7-128">Requirement</span></span> | <span data-ttu-id="96af7-129">Value</span><span class="sxs-lookup"><span data-stu-id="96af7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96af7-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96af7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="96af7-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="96af7-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="96af7-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96af7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="96af7-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="96af7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="96af7-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96af7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="96af7-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="96af7-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="96af7-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96af7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96af7-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96af7-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

