---
title: TLSLicenseEnumEnd función)
description: Continúa desde una llamada anterior a la función TLSLicenseEnumBegin y finaliza la enumeración.
ms.assetid: b9cba03c-0f5a-41e8-ae13-bcdd0ac6dd99
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSLicenseEnumEnd
topic_type:
- apiref
api_name:
- TLSLicenseEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bbd494ec539ee78008fa3df274282da1e9db6c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676921"
---
# <a name="tlslicenseenumend-function"></a><span data-ttu-id="a0d64-104">TLSLicenseEnumEnd función)</span><span class="sxs-lookup"><span data-stu-id="a0d64-104">TLSLicenseEnumEnd function</span></span>

<span data-ttu-id="a0d64-105">Continúa desde una llamada anterior a la función [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) y finaliza la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a0d64-105">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="a0d64-106">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="a0d64-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="a0d64-107">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="a0d64-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a0d64-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0d64-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="a0d64-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0d64-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0d64-110">*hHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0d64-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0d64-111">Identificador de un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="a0d64-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="a0d64-112">Especifique un identificador abierto por la función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="a0d64-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a0d64-113">*pdwErrCode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a0d64-113">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0d64-114">Puntero a una variable que recibe uno de los siguientes códigos de error en la devolución.</span><span class="sxs-lookup"><span data-stu-id="a0d64-114">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="a0d64-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="a0d64-115"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a0d64-116">La llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0d64-116">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span data-ttu-id="a0d64-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER \_ E \_ \_ identificador no válido** (5005)</span><span class="sxs-lookup"><span data-stu-id="a0d64-117"><span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER\_E\_INVALID\_HANDLE** (5005)</span></span>


</dt> <dd>

<span data-ttu-id="a0d64-118">El identificador no es válido.</span><span class="sxs-lookup"><span data-stu-id="a0d64-118">The handle is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0d64-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0d64-119">Return value</span></span>

<span data-ttu-id="a0d64-120">Esta función devuelve los siguientes posibles valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="a0d64-120">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="a0d64-121">**RPC \_ S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="a0d64-121">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="a0d64-122">La llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0d64-122">The call succeeded.</span></span> <span data-ttu-id="a0d64-123">Compruebe el valor del parámetro *pdwErrCode* para obtener el código de retorno de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a0d64-123">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="a0d64-124">**\_ \_ argumento no válido de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="a0d64-124">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="a0d64-125">El argumento no era válido.</span><span class="sxs-lookup"><span data-stu-id="a0d64-125">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0d64-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0d64-126">Requirements</span></span>



| <span data-ttu-id="a0d64-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0d64-127">Requirement</span></span> | <span data-ttu-id="a0d64-128">Value</span><span class="sxs-lookup"><span data-stu-id="a0d64-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d64-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0d64-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a0d64-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0d64-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0d64-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0d64-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a0d64-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0d64-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0d64-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0d64-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0d64-134"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0d64-134"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0d64-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0d64-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d64-136">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="a0d64-136">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="a0d64-137">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="a0d64-137">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="a0d64-138">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="a0d64-138">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="a0d64-139">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="a0d64-139">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> </dl>

 

