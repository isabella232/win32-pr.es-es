---
title: TLSKeyPackEnumEnd función)
description: Continúa desde una llamada anterior a la función TLSKeyPackEnumBegin y finaliza la enumeración.
ms.assetid: 3434e18d-54c9-46ed-b6a5-bc174b63a152
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSKeyPackEnumEnd
topic_type:
- apiref
api_name:
- TLSKeyPackEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04723318b29adff7a647fe2cab39fb0b16f3f5a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802107"
---
# <a name="tlskeypackenumend-function"></a><span data-ttu-id="2b778-104">TLSKeyPackEnumEnd función)</span><span class="sxs-lookup"><span data-stu-id="2b778-104">TLSKeyPackEnumEnd function</span></span>

<span data-ttu-id="2b778-105">Continúa desde una llamada anterior a la función [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) y finaliza la enumeración.</span><span class="sxs-lookup"><span data-stu-id="2b778-105">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and terminates the enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="2b778-106">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="2b778-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="2b778-107">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="2b778-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2b778-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b778-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="2b778-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b778-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b778-110">*hHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b778-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b778-111">Identificador de un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2b778-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="2b778-112">Especifique un identificador abierto por la función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="2b778-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2b778-113">*pdwErrCode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2b778-113">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b778-114">Puntero a una variable que recibe uno de los siguientes códigos de error en la devolución.</span><span class="sxs-lookup"><span data-stu-id="2b778-114">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="2b778-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="2b778-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2b778-116">La llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="2b778-116">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span data-ttu-id="2b778-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER \_ E \_ \_ identificador no válido** (5005)</span><span class="sxs-lookup"><span data-stu-id="2b778-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER\_E\_INVALID\_HANDLE** (5005)</span></span>


</dt> <dd>

<span data-ttu-id="2b778-118">El identificador no es válido.</span><span class="sxs-lookup"><span data-stu-id="2b778-118">The handle is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b778-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b778-119">Return value</span></span>

<span data-ttu-id="2b778-120">Esta función devuelve los siguientes posibles valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="2b778-120">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="2b778-121">**RPC \_ S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="2b778-121">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="2b778-122">La llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2b778-122">The call succeeded.</span></span> <span data-ttu-id="2b778-123">Compruebe el valor del parámetro *pdwErrCode* para obtener el código de retorno de la llamada.</span><span class="sxs-lookup"><span data-stu-id="2b778-123">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="2b778-124">**\_ \_ argumento no válido de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="2b778-124">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="2b778-125">El argumento no era válido.</span><span class="sxs-lookup"><span data-stu-id="2b778-125">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b778-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b778-126">Requirements</span></span>



| <span data-ttu-id="2b778-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b778-127">Requirement</span></span> | <span data-ttu-id="2b778-128">Value</span><span class="sxs-lookup"><span data-stu-id="2b778-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b778-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b778-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2b778-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b778-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b778-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b778-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2b778-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b778-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b778-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b778-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b778-134"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b778-134"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b778-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b778-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b778-136">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="2b778-136">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="2b778-137">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="2b778-137">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="2b778-138">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="2b778-138">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="2b778-139">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="2b778-139">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> </dl>

 

