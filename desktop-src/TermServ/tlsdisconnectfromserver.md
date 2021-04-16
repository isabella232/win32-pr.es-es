---
title: TLSDisconnectFromServer función)
description: Cierra un identificador abierto a un servidor de licencias de Escritorio remoto.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSDisconnectFromServer
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265a6b04186bd640943cf2b348dda7afcf8f712a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686204"
---
# <a name="tlsdisconnectfromserver-function"></a><span data-ttu-id="05abe-104">TLSDisconnectFromServer función)</span><span class="sxs-lookup"><span data-stu-id="05abe-104">TLSDisconnectFromServer function</span></span>

<span data-ttu-id="05abe-105">Cierra un identificador abierto a un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="05abe-105">Closes an open handle to a Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="05abe-106">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="05abe-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="05abe-107">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="05abe-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="05abe-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05abe-108">Syntax</span></span>


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a><span data-ttu-id="05abe-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05abe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05abe-110">*hHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05abe-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05abe-111">Identificador de un servidor de licencias de Escritorio remoto abierto por una llamada a la función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="05abe-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05abe-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05abe-112">Return value</span></span>

<span data-ttu-id="05abe-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="05abe-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05abe-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05abe-114">Remarks</span></span>

<span data-ttu-id="05abe-115">Llame a la función **TLSDisconnectFromServer** como parte de la rutina de limpieza del programa para cerrar todos los identificadores de servidor que se abren mediante llamadas a la función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="05abe-115">Call the **TLSDisconnectFromServer** function as part of your program's clean-up routine to close all the server handles that are opened by calls to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="05abe-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05abe-116">Requirements</span></span>



| <span data-ttu-id="05abe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="05abe-117">Requirement</span></span> | <span data-ttu-id="05abe-118">Value</span><span class="sxs-lookup"><span data-stu-id="05abe-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05abe-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05abe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="05abe-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05abe-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="05abe-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05abe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="05abe-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05abe-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="05abe-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05abe-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05abe-124"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05abe-124"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05abe-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="05abe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05abe-126">**identificador de TLS \_**</span><span class="sxs-lookup"><span data-stu-id="05abe-126">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="05abe-127">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="05abe-127">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

