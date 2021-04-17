---
title: TLSGetServerCertificate función)
description: Devuelve el certificado del servidor de licencias de Escritorio remoto.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSGetServerCertificate
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676663"
---
# <a name="tlsgetservercertificate-function"></a><span data-ttu-id="5d896-104">TLSGetServerCertificate función)</span><span class="sxs-lookup"><span data-stu-id="5d896-104">TLSGetServerCertificate function</span></span>

<span data-ttu-id="5d896-105">Devuelve el certificado del servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="5d896-105">Returns the certificate of the Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="5d896-106">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="5d896-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="5d896-107">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="5d896-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5d896-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d896-108">Syntax</span></span>


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="5d896-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d896-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d896-110">*hHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d896-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d896-111">Identificador de un servidor de licencias de Escritorio remoto abierto por una llamada a la función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="5d896-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="5d896-112">*bSignCert* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d896-112">*bSignCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d896-113">**True** si el certificado de firma es **false** si se trata de un certificado de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5d896-113">**TRUE** if signature certificate, **FALSE** if exchange certificate.</span></span>

</dd> <dt>

<span data-ttu-id="5d896-114">*ppbCertBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d896-114">*ppbCertBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d896-115">Puntero a una variable que recibe un puntero a un búfer que contiene el certificado.</span><span class="sxs-lookup"><span data-stu-id="5d896-115">Pointer to a variable that receives a pointer to a buffer that contains the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="5d896-116">*lpdwCertBlobLen* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d896-116">*lpdwCertBlobLen* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d896-117">Puntero a una variable que recibe el tamaño del certificado que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="5d896-117">Pointer to a variable that receives the size of the certificate that is returned.</span></span>

</dd> <dt>

<span data-ttu-id="5d896-118">*pdwErrCode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d896-118">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d896-119">Puntero a una variable que recibe el código de error.</span><span class="sxs-lookup"><span data-stu-id="5d896-119">Pointer to a variable that receives the error code.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="5d896-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="5d896-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5d896-121">La llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="5d896-121">Call is successful.</span></span>

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span data-ttu-id="5d896-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS \_ \_ \_ Certificado W SELFSIGN** (4007)</span><span class="sxs-lookup"><span data-stu-id="5d896-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS\_W\_SELFSIGN\_CERTIFICATE** (4007)</span></span>


</dt> <dd>

<span data-ttu-id="5d896-123">El certificado devuelto es un certificado autofirmado.</span><span class="sxs-lookup"><span data-stu-id="5d896-123">Certificate returned is a self-signed certificate.</span></span>

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span data-ttu-id="5d896-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS \_ W \_ temp \_ SELFSIGN \_ CERT** (4009)</span><span class="sxs-lookup"><span data-stu-id="5d896-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS\_W\_TEMP\_SELFSIGN\_CERT** (4009)</span></span>


</dt> <dd>

<span data-ttu-id="5d896-125">El certificado devuelto es temporal.</span><span class="sxs-lookup"><span data-stu-id="5d896-125">Certificate returned is temporary.</span></span>

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span data-ttu-id="5d896-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS \_ E \_ acceso \_ denegado** (5003)</span><span class="sxs-lookup"><span data-stu-id="5d896-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS\_E\_ACCESS\_DENIED** (5003)</span></span>


</dt> <dd>

<span data-ttu-id="5d896-127">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="5d896-127">Access denied.</span></span>

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span data-ttu-id="5d896-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS \_ E \_ \_ identificador de asignación** (5007)</span><span class="sxs-lookup"><span data-stu-id="5d896-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS\_E\_ALLOCATE\_HANDLE** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="5d896-129">El servidor está demasiado ocupado para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d896-129">Server is too busy to process the request.</span></span>

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span data-ttu-id="5d896-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS \_ E \_ sin \_ certificado** (5022)</span><span class="sxs-lookup"><span data-stu-id="5d896-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS\_E\_NO\_CERTIFICATE** (5022)</span></span>


</dt> <dd>

<span data-ttu-id="5d896-131">No se puede recuperar un certificado.</span><span class="sxs-lookup"><span data-stu-id="5d896-131">Cannot retrieve a certificate.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d896-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d896-132">Return value</span></span>

<span data-ttu-id="5d896-133">Esta función devuelve los siguientes posibles valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="5d896-133">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="5d896-134">**RPC \_ S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="5d896-134">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="5d896-135">La llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5d896-135">The call succeeded.</span></span> <span data-ttu-id="5d896-136">Compruebe el valor del parámetro *pdwErrCode* para obtener el código de retorno de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5d896-136">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="5d896-137">**\_ \_ argumento no válido de RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="5d896-137">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="5d896-138">El argumento no era válido.</span><span class="sxs-lookup"><span data-stu-id="5d896-138">The argument was invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d896-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d896-139">Requirements</span></span>



| <span data-ttu-id="5d896-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d896-140">Requirement</span></span> | <span data-ttu-id="5d896-141">Value</span><span class="sxs-lookup"><span data-stu-id="5d896-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d896-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d896-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5d896-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d896-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d896-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d896-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5d896-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d896-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d896-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d896-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d896-147"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d896-147"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d896-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d896-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d896-149">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="5d896-149">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

