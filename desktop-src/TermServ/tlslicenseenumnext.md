---
title: TLSLicenseEnumNext función)
description: Continúa desde una llamada anterior a la función TLSLicenseEnumBegin y devuelve la siguiente licencia que se instala en un servidor de licencias Escritorio remoto que coincide con los criterios de búsqueda.
ms.assetid: 6932289b-b59c-493c-8dbc-03c0662e921e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSLicenseEnumNext
topic_type:
- apiref
api_name:
- TLSLicenseEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c13b0a3137258015fe311c49b2cc9b999e3a13f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422611"
---
# <a name="tlslicenseenumnext-function"></a><span data-ttu-id="b6665-104">TLSLicenseEnumNext función)</span><span class="sxs-lookup"><span data-stu-id="b6665-104">TLSLicenseEnumNext function</span></span>

<span data-ttu-id="b6665-105">Continúa desde una llamada anterior a la función [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) y devuelve la siguiente licencia que se instala en un servidor de licencias escritorio remoto que coincide con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b6665-105">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="b6665-106">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="b6665-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="b6665-107">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="b6665-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b6665-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6665-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LSLicense  *lpLicense,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="b6665-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6665-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6665-110">*hHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6665-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6665-111">Identificador de un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="b6665-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="b6665-112">Especifique un identificador abierto por la función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b6665-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="b6665-113">*lpLicense* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6665-113">*lpLicense* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6665-114">Puntero a una estructura [**LSLicense**](lslicense.md) que recibe la siguiente licencia que coincide con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b6665-114">Pointer to a [**LSLicense**](lslicense.md) structure that receives the next license that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="b6665-115">*pdwErrCode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b6665-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6665-116">Puntero a una variable que recibe uno de los siguientes códigos de error en la devolución.</span><span class="sxs-lookup"><span data-stu-id="b6665-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="b6665-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="b6665-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b6665-118">La llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6665-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="b6665-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_ \_No he \_ más \_ datos** (4001)</span><span class="sxs-lookup"><span data-stu-id="b6665-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="b6665-120">No hay más licencias que coincidan con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b6665-120">No more licenses match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="b6665-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ E \_ \_ error interno** (5001)</span><span class="sxs-lookup"><span data-stu-id="b6665-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="b6665-122">Error interno en el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="b6665-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="b6665-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ \_ secuencia no válida** (5006)</span><span class="sxs-lookup"><span data-stu-id="b6665-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="b6665-124">La secuencia de llamada no era válida.</span><span class="sxs-lookup"><span data-stu-id="b6665-124">The calling sequence was not valid.</span></span> <span data-ttu-id="b6665-125">Debe llamar a la función [**TLSLicenseEnumBegin ()**](tlslicenseenumbegin.md) antes de este.</span><span class="sxs-lookup"><span data-stu-id="b6665-125">Must call the [**TLSLicenseEnumBegin()**](tlslicenseenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="b6665-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ servidor \_ ocupado** (5007)</span><span class="sxs-lookup"><span data-stu-id="b6665-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="b6665-127">El servidor de licencias está demasiado ocupado para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6665-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="b6665-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="b6665-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="b6665-129">No se puede procesar la solicitud porque no hay memoria suficiente.</span><span class="sxs-lookup"><span data-stu-id="b6665-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6665-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6665-130">Return value</span></span>

<span data-ttu-id="b6665-131">Esta función devuelve los siguientes posibles valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="b6665-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="b6665-132">**RPC \_ S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="b6665-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="b6665-133">La llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6665-133">The call succeeded.</span></span> <span data-ttu-id="b6665-134">Compruebe el valor del parámetro *pdwErrCode* para obtener el código de retorno de la llamada.</span><span class="sxs-lookup"><span data-stu-id="b6665-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="b6665-135">**\_ \_ argumento no válido de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="b6665-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="b6665-136">El argumento no era válido.</span><span class="sxs-lookup"><span data-stu-id="b6665-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6665-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6665-137">Requirements</span></span>



| <span data-ttu-id="b6665-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6665-138">Requirement</span></span> | <span data-ttu-id="b6665-139">Value</span><span class="sxs-lookup"><span data-stu-id="b6665-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6665-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6665-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b6665-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6665-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6665-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6665-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b6665-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6665-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6665-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6665-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6665-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6665-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6665-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6665-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6665-147">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="b6665-147">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="b6665-148">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="b6665-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="b6665-149">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="b6665-149">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="b6665-150">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="b6665-150">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

