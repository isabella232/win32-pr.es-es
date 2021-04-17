---
title: TLSConnectToLsServer función)
description: Abre un identificador del servidor de licencias de Escritorio remoto especificado.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la función TLSConnectToLsServer
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422416"
---
# <a name="tlsconnecttolsserver-function"></a><span data-ttu-id="68a0a-104">TLSConnectToLsServer función)</span><span class="sxs-lookup"><span data-stu-id="68a0a-104">TLSConnectToLsServer function</span></span>

<span data-ttu-id="68a0a-105">Abre un identificador del servidor de licencias de Escritorio remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="68a0a-105">Opens a handle to the specified Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="68a0a-106">Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación.</span><span class="sxs-lookup"><span data-stu-id="68a0a-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="68a0a-107">Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="68a0a-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="68a0a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68a0a-108">Syntax</span></span>


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a><span data-ttu-id="68a0a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68a0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68a0a-110">*pszLsServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68a0a-110">*pszLsServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68a0a-111">Puntero a una cadena terminada en **null** que especifica el nombre NetBIOS del servidor de licencias de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="68a0a-111">Pointer to a **null**-terminated string that specifies the NetBIOS name of the Remote Desktop license server.</span></span> <span data-ttu-id="68a0a-112">Si el valor de este parámetro es **null**, el servidor especificado es el equipo local.</span><span class="sxs-lookup"><span data-stu-id="68a0a-112">If the value of this parameter is **NULL**, the specified server is the local computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68a0a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68a0a-113">Return value</span></span>

<span data-ttu-id="68a0a-114">Si la función se ejecuta correctamente, el valor devuelto es un identificador del servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="68a0a-114">If the function succeeds, the return value is a handle to the specified server.</span></span>

<span data-ttu-id="68a0a-115">Si se produce un error en la función, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="68a0a-115">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="68a0a-116">Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="68a0a-116">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="68a0a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68a0a-117">Remarks</span></span>

<span data-ttu-id="68a0a-118">Cuando haya terminado de usar el identificador devuelto por la función **TLSConnectToLsServer** , suéltelo llamando a la función [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) .</span><span class="sxs-lookup"><span data-stu-id="68a0a-118">When you have finished using the handle that is returned by the **TLSConnectToLsServer** function, release it by calling the [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="68a0a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68a0a-119">Requirements</span></span>



| <span data-ttu-id="68a0a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68a0a-120">Requirement</span></span> | <span data-ttu-id="68a0a-121">Value</span><span class="sxs-lookup"><span data-stu-id="68a0a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68a0a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68a0a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68a0a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68a0a-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68a0a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68a0a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68a0a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68a0a-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68a0a-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68a0a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68a0a-127"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68a0a-127"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68a0a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="68a0a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a0a-129">**identificador de TLS \_**</span><span class="sxs-lookup"><span data-stu-id="68a0a-129">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="68a0a-130">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="68a0a-130">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

