---
title: TLSLicenseEnumBegin función)
description: Comienza la enumeración de licencias emitidas por el servidor de licencias de Escritorio remoto basado en criterios de búsqueda.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSLicenseEnumBegin
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803854"
---
# <a name="tlslicenseenumbegin-function"></a><span data-ttu-id="1794d-104">TLSLicenseEnumBegin función)</span><span class="sxs-lookup"><span data-stu-id="1794d-104">TLSLicenseEnumBegin function</span></span>

<span data-ttu-id="1794d-105">Comienza la enumeración de licencias emitidas por el servidor de licencias de Escritorio remoto basado en criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1794d-105">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="1794d-106">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="1794d-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="1794d-107">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="1794d-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1794d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1794d-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="1794d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1794d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1794d-110">*hHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1794d-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1794d-111">Identificador de un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="1794d-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="1794d-112">Especifique un identificador abierto por la función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="1794d-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1794d-113">*dwSearchParm* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1794d-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1794d-114">Especifica los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1794d-114">Specifies the search criteria.</span></span> <span data-ttu-id="1794d-115">El parámetro puede ser uno o una combinación de los valores que se describen en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="1794d-115">The parameter can be one or a combination of the values that are described in the following list.</span></span> <span data-ttu-id="1794d-116">El parámetro especifica el tipo de paquete de claves y el paquete de claves que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="1794d-116">The parameter specifies the type of key pack and which key pack to search.</span></span>

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span data-ttu-id="1794d-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_ BUSCAR \_ LICENSEID** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="1794d-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE\_SEARCH\_LICENSEID** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-118">Busque por identificador de licencia.</span><span class="sxs-lookup"><span data-stu-id="1794d-118">Search by license ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span data-ttu-id="1794d-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_ BUSCAR \_ KEYPACKID** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="1794d-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE\_SEARCH\_KEYPACKID** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-120">Busque por identificador de paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="1794d-120">Search by key pack ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span data-ttu-id="1794d-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_ BUSCAR \_ MACHINENAME** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="1794d-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE\_SEARCH\_MACHINENAME** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-122">Busque por nombre de equipo.</span><span class="sxs-lookup"><span data-stu-id="1794d-122">Search by machine name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span data-ttu-id="1794d-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_ BUSCAR el \_ nombre de usuario** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="1794d-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE\_SEARCH\_USERNAME** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-124">Busque por nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="1794d-124">Search by user name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span data-ttu-id="1794d-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_ BUSCAR \_ ISSUEDATE** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="1794d-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE\_SEARCH\_ISSUEDATE** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-126">Busque por fecha del problema.</span><span class="sxs-lookup"><span data-stu-id="1794d-126">Search by issue date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span data-ttu-id="1794d-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_ BUSCAR \_ EXPIREDATE** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="1794d-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE\_SEARCH\_EXPIREDATE** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-128">Buscar por fecha de expiración.</span><span class="sxs-lookup"><span data-stu-id="1794d-128">Search by expiration date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span data-ttu-id="1794d-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_ BUSCAR \_ NUMLICENSES** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="1794d-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE\_SEARCH\_ NUMLICENSES** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-130">Busque por número de licencias.</span><span class="sxs-lookup"><span data-stu-id="1794d-130">Search by number of licenses.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span data-ttu-id="1794d-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_ \_ \_ Estado** de la entrada de búsqueda (0x20000000)</span><span class="sxs-lookup"><span data-stu-id="1794d-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE\_SEARCH\_ ENTRY\_STATUS** (0x20000000)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-132">Busque por estado de entrada.</span><span class="sxs-lookup"><span data-stu-id="1794d-132">Search by entry status.</span></span>

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span data-ttu-id="1794d-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_ \_Licencia de búsqueda** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="1794d-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE\_EXSEARCH\_LICENSESTATUS** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-134">Busque por estado de licencia.</span><span class="sxs-lookup"><span data-stu-id="1794d-134">Search by license status.</span></span>

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span data-ttu-id="1794d-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_ BUSCAR \_ todo** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="1794d-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK\_SEARCH\_ALL** (0xFFFFFFFF)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-136">Buscar todas las licencias.</span><span class="sxs-lookup"><span data-stu-id="1794d-136">Search all licenses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1794d-137">*bMatchAll* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1794d-137">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1794d-138">Especifica si se deben buscar coincidencias con todos los valores de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1794d-138">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="1794d-139">*lpSearchParm* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1794d-139">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1794d-140">Puntero a una estructura [**LSLicense**](lslicense.md) que especifica los parámetros de búsqueda que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="1794d-140">Pointer to a [**LSLicense**](lslicense.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="1794d-141">*pdwErrCode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1794d-141">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1794d-142">Puntero a una variable que recibe uno de los siguientes códigos de error en la devolución.</span><span class="sxs-lookup"><span data-stu-id="1794d-142">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="1794d-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="1794d-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-144">La llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="1794d-144">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="1794d-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ E \_ \_ error interno** (5001)</span><span class="sxs-lookup"><span data-stu-id="1794d-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-146">Error interno en el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="1794d-146">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="1794d-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ \_ secuencia no válida** (5006)</span><span class="sxs-lookup"><span data-stu-id="1794d-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-148">La secuencia de llamada no era válida.</span><span class="sxs-lookup"><span data-stu-id="1794d-148">The calling sequence was not valid.</span></span> <span data-ttu-id="1794d-149">Lo más probable es que una enumeración anterior no haya finalizado.</span><span class="sxs-lookup"><span data-stu-id="1794d-149">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="1794d-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ servidor \_ ocupado** (5007)</span><span class="sxs-lookup"><span data-stu-id="1794d-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-151">El servidor de licencias está demasiado ocupado para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1794d-151">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="1794d-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="1794d-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-153">No se puede procesar la solicitud porque no hay memoria suficiente.</span><span class="sxs-lookup"><span data-stu-id="1794d-153">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="1794d-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ \_ datos no válidos** (5009)</span><span class="sxs-lookup"><span data-stu-id="1794d-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="1794d-155">Los datos del parámetro de búsqueda no son válidos.</span><span class="sxs-lookup"><span data-stu-id="1794d-155">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1794d-156">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1794d-156">Return value</span></span>

<span data-ttu-id="1794d-157">Esta función devuelve los siguientes posibles valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="1794d-157">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="1794d-158">**RPC \_ S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="1794d-158">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="1794d-159">La llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="1794d-159">The call succeeded.</span></span> <span data-ttu-id="1794d-160">Compruebe el valor del parámetro *pdwErrCode* para obtener el código de retorno de la llamada.</span><span class="sxs-lookup"><span data-stu-id="1794d-160">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="1794d-161">**\_ \_ argumento no válido de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="1794d-161">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="1794d-162">El argumento no era válido.</span><span class="sxs-lookup"><span data-stu-id="1794d-162">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1794d-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1794d-163">Requirements</span></span>



| <span data-ttu-id="1794d-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="1794d-164">Requirement</span></span> | <span data-ttu-id="1794d-165">Value</span><span class="sxs-lookup"><span data-stu-id="1794d-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1794d-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1794d-166">Minimum supported client</span></span><br/> | <span data-ttu-id="1794d-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1794d-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1794d-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1794d-168">Minimum supported server</span></span><br/> | <span data-ttu-id="1794d-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1794d-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1794d-170">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1794d-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1794d-171"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1794d-171"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1794d-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="1794d-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1794d-173">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="1794d-173">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="1794d-174">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="1794d-174">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="1794d-175">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="1794d-175">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="1794d-176">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="1794d-176">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

