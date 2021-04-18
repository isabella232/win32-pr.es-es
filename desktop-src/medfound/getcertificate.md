---
description: Obtiene un certificado para un controlador de pantalla.
ms.assetid: eceaf151-1dae-4ff0-9139-7f1789f6c682
title: GetCertificate función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificate
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 30cb17345177b552e51120afd00758a3f6886584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705403"
---
# <a name="getcertificate-function"></a><span data-ttu-id="20ef8-103">GetCertificate función)</span><span class="sxs-lookup"><span data-stu-id="20ef8-103">GetCertificate function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20ef8-104">El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="20ef8-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="20ef8-105">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="20ef8-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="20ef8-106">Obtiene un certificado para un controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="20ef8-106">Gets a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ef8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20ef8-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificate(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ BYTE                     *pbCertificate,
  _Out_ ULONG                    ulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="20ef8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20ef8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20ef8-109">*pstrDeviceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20ef8-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ef8-110">Puntero a una estructura de [**\_ cadena Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo de pantalla, tal y como lo devuelve la función [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="20ef8-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="20ef8-111">*ctPVPCertificateType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20ef8-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ef8-112">El tipo de certificado, especificado como miembro de la enumeración del **\_ \_ tipo de certificado DXGKMDT** .</span><span class="sxs-lookup"><span data-stu-id="20ef8-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="20ef8-113">*pbCertificate* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="20ef8-113">*pbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20ef8-114">Un puntero a un búfer que recibe el certificado.</span><span class="sxs-lookup"><span data-stu-id="20ef8-114">A pointer to a buffer that receives the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="20ef8-115">*ulCertificateLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="20ef8-115">*ulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20ef8-116">Tamaño del búfer de *pbCertificate* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="20ef8-116">The size of the *pbCertificate* buffer, in bytes.</span></span> <span data-ttu-id="20ef8-117">Para obtener el tamaño del certificado, llame a [**GetCertificateSize**](getcertificatesize.md).</span><span class="sxs-lookup"><span data-stu-id="20ef8-117">To get the size of the certificate, call [**GetCertificateSize**](getcertificatesize.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20ef8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20ef8-118">Return value</span></span>

<span data-ttu-id="20ef8-119">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="20ef8-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="20ef8-120">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="20ef8-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="20ef8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20ef8-121">Remarks</span></span>

<span data-ttu-id="20ef8-122">Las aplicaciones deben llamar al método [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) en lugar de esta función.</span><span class="sxs-lookup"><span data-stu-id="20ef8-122">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="20ef8-123">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="20ef8-123">This function has no associated import library.</span></span> <span data-ttu-id="20ef8-124">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="20ef8-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ef8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20ef8-125">Requirements</span></span>



| <span data-ttu-id="20ef8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="20ef8-126">Requirement</span></span> | <span data-ttu-id="20ef8-127">Value</span><span class="sxs-lookup"><span data-stu-id="20ef8-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="20ef8-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20ef8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="20ef8-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="20ef8-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="20ef8-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20ef8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="20ef8-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="20ef8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="20ef8-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="20ef8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20ef8-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20ef8-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20ef8-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="20ef8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ef8-135">Funciones de OPM</span><span class="sxs-lookup"><span data-stu-id="20ef8-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="20ef8-136">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="20ef8-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
