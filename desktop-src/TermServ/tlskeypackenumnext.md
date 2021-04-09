---
title: TLSKeyPackEnumNext función)
description: Continúa desde una llamada anterior a la función TLSKeyPackEnumBegin y devuelve el siguiente paquete de claves que está instalado en un servidor de licencias Escritorio remoto que coincida con los criterios de búsqueda.
ms.assetid: 2614eb7a-df57-42a6-ad34-0a3211a6b8c3
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSKeyPackEnumNext
topic_type:
- apiref
api_name:
- TLSKeyPackEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897874f333ed7933ea1616f7f5ba5f1686736d0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078966"
---
# <a name="tlskeypackenumnext-function"></a><span data-ttu-id="f03be-104">TLSKeyPackEnumNext función)</span><span class="sxs-lookup"><span data-stu-id="f03be-104">TLSKeyPackEnumNext function</span></span>

<span data-ttu-id="f03be-105">Continúa desde una llamada anterior a la función [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) y devuelve el siguiente paquete de claves que está instalado en un servidor de licencias escritorio remoto que coincida con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f03be-105">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="f03be-106">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="f03be-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="f03be-107">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="f03be-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f03be-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f03be-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="f03be-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f03be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f03be-110">*hHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f03be-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f03be-111">Identificador de un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f03be-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="f03be-112">Especifique un identificador abierto por la función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="f03be-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f03be-113">*lpKeyPack* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f03be-113">*lpKeyPack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f03be-114">Puntero a una estructura [**LSKeyPack**](lskeypack.md) que recibe el siguiente paquete de claves que coincide con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f03be-114">Pointer to a [**LSKeyPack**](lskeypack.md) structure that receives the next key pack that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="f03be-115">*pdwErrCode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f03be-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f03be-116">Puntero a una variable que recibe uno de los siguientes códigos de error en la devolución.</span><span class="sxs-lookup"><span data-stu-id="f03be-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="f03be-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="f03be-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f03be-118">La llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f03be-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="f03be-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_ \_No he \_ más \_ datos** (4001)</span><span class="sxs-lookup"><span data-stu-id="f03be-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="f03be-120">No hay más paquetes de claves que coincidan con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f03be-120">No more key packs match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="f03be-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ E \_ \_ error interno** (5001)</span><span class="sxs-lookup"><span data-stu-id="f03be-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="f03be-122">Error interno en el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="f03be-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="f03be-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ \_ secuencia no válida** (5006)</span><span class="sxs-lookup"><span data-stu-id="f03be-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="f03be-124">La secuencia de llamada no era válida.</span><span class="sxs-lookup"><span data-stu-id="f03be-124">The calling sequence was not valid.</span></span> <span data-ttu-id="f03be-125">Debe llamar a la función [**TLSKeyPackEnumBegin ()**](tlskeypackenumbegin.md) antes de este.</span><span class="sxs-lookup"><span data-stu-id="f03be-125">Must call the [**TLSKeyPackEnumBegin()**](tlskeypackenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="f03be-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ servidor \_ ocupado** (5007)</span><span class="sxs-lookup"><span data-stu-id="f03be-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="f03be-127">El servidor de licencias está demasiado ocupado para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f03be-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="f03be-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="f03be-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="f03be-129">No se puede procesar la solicitud porque no hay memoria suficiente.</span><span class="sxs-lookup"><span data-stu-id="f03be-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f03be-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f03be-130">Return value</span></span>

<span data-ttu-id="f03be-131">Esta función devuelve los siguientes posibles valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="f03be-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="f03be-132">**RPC \_ S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="f03be-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="f03be-133">La llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f03be-133">The call succeeded.</span></span> <span data-ttu-id="f03be-134">Compruebe el valor del parámetro *pdwErrCode* para obtener el código de retorno de la llamada.</span><span class="sxs-lookup"><span data-stu-id="f03be-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="f03be-135">**\_ \_ argumento no válido de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="f03be-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="f03be-136">El argumento no era válido.</span><span class="sxs-lookup"><span data-stu-id="f03be-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f03be-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f03be-137">Requirements</span></span>



| <span data-ttu-id="f03be-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f03be-138">Requirement</span></span> | <span data-ttu-id="f03be-139">Value</span><span class="sxs-lookup"><span data-stu-id="f03be-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f03be-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f03be-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f03be-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f03be-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f03be-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f03be-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f03be-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f03be-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f03be-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f03be-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f03be-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f03be-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f03be-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="f03be-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f03be-147">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f03be-147">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="f03be-148">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="f03be-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="f03be-149">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="f03be-149">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="f03be-150">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="f03be-150">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

