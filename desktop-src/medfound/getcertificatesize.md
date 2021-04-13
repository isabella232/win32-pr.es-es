---
description: Obtiene el tamaño de un certificado para un controlador de pantalla.
ms.assetid: fd52e939-127a-4493-8406-31f7767921cd
title: GetCertificateSize función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateSize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bcd1f49ce65978c6a89c89cee1fda38e41434065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360090"
---
# <a name="getcertificatesize-function"></a><span data-ttu-id="e8259-103">GetCertificateSize función)</span><span class="sxs-lookup"><span data-stu-id="e8259-103">GetCertificateSize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8259-104">El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e8259-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="e8259-105">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="e8259-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="e8259-106">Obtiene el tamaño de un certificado para un controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e8259-106">Gets the size of a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8259-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8259-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificateSize(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ ULONG                    *pulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="e8259-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8259-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8259-109">*pstrDeviceName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8259-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8259-110">Puntero a una estructura de [**\_ cadena Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contiene el nombre del dispositivo de pantalla, tal y como lo devuelve la función [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="e8259-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="e8259-111">*ctPVPCertificateType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8259-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8259-112">El tipo de certificado, especificado como miembro de la enumeración del **\_ \_ tipo de certificado DXGKMDT** .</span><span class="sxs-lookup"><span data-stu-id="e8259-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e8259-113">*pulCertificateLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e8259-113">*pulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8259-114">Recibe el tamaño del certificado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e8259-114">Receives the size of the certificate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8259-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8259-115">Return value</span></span>

<span data-ttu-id="e8259-116">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e8259-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="e8259-117">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="e8259-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8259-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8259-118">Remarks</span></span>

<span data-ttu-id="e8259-119">Las aplicaciones deben llamar al método [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) en lugar de esta función.</span><span class="sxs-lookup"><span data-stu-id="e8259-119">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="e8259-120">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="e8259-120">This function has no associated import library.</span></span> <span data-ttu-id="e8259-121">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="e8259-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8259-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8259-122">Requirements</span></span>



| <span data-ttu-id="e8259-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8259-123">Requirement</span></span> | <span data-ttu-id="e8259-124">Value</span><span class="sxs-lookup"><span data-stu-id="e8259-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8259-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8259-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e8259-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e8259-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e8259-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8259-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e8259-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8259-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e8259-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8259-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8259-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8259-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8259-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8259-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8259-132">Funciones de OPM</span><span class="sxs-lookup"><span data-stu-id="e8259-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="e8259-133">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="e8259-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
