---
description: Crea un controlador de flujo de bytes para el origen de medios MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: MFCreateMP3ByteStreamPlugin función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659827"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a><span data-ttu-id="f87c6-103">MFCreateMP3ByteStreamPlugin función)</span><span class="sxs-lookup"><span data-stu-id="f87c6-103">MFCreateMP3ByteStreamPlugin function</span></span>

<span data-ttu-id="f87c6-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="f87c6-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f87c6-105">En su lugar, las aplicaciones deben usar la [resolución de origen](source-resolver.md) para crear el origen de medios MP3.\]</span><span class="sxs-lookup"><span data-stu-id="f87c6-105">Instead, applications should use the [Source Resolver](source-resolver.md) to create the MP3 media source.\]</span></span>

<span data-ttu-id="f87c6-106">Crea un controlador de flujo de bytes para el origen de medios MP3.</span><span class="sxs-lookup"><span data-stu-id="f87c6-106">Creates a byte-stream handler for the MP3 media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="f87c6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f87c6-107">Syntax</span></span>


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a><span data-ttu-id="f87c6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f87c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f87c6-109">*riid* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f87c6-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f87c6-110">Identificador de interfaz (IID) de la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="f87c6-110">The interface identifier (IID) of the requested interface.</span></span> <span data-ttu-id="f87c6-111">Establezca este parámetro en **IID \_ IMFByteStreamHandler** para recibir un puntero a la interfaz [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="f87c6-111">Set this parameter to **IID\_IMFByteStreamHandler** to receive a pointer to the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f87c6-112">*ppvHandler* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f87c6-112">*ppvHandler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f87c6-113">Recibe un puntero a la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f87c6-113">Receives a pointer to the interface.</span></span> <span data-ttu-id="f87c6-114">El llamador debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="f87c6-114">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f87c6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f87c6-115">Return value</span></span>

<span data-ttu-id="f87c6-116">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f87c6-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f87c6-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f87c6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f87c6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f87c6-118">Remarks</span></span>

<span data-ttu-id="f87c6-119">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="f87c6-119">This function has no associated import library.</span></span> <span data-ttu-id="f87c6-120">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a mf.dll.</span><span class="sxs-lookup"><span data-stu-id="f87c6-120">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to mf.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f87c6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f87c6-121">Requirements</span></span>



| <span data-ttu-id="f87c6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f87c6-122">Requirement</span></span> | <span data-ttu-id="f87c6-123">Value</span><span class="sxs-lookup"><span data-stu-id="f87c6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f87c6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f87c6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f87c6-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f87c6-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f87c6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f87c6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f87c6-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f87c6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f87c6-128">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f87c6-128">End of client support</span></span><br/>    | <span data-ttu-id="f87c6-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f87c6-129">Windows Vista</span></span><br/>                             |
| <span data-ttu-id="f87c6-130">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f87c6-130">End of server support</span></span><br/>    | <span data-ttu-id="f87c6-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f87c6-131">Windows Server 2008</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="f87c6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f87c6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f87c6-133">Funciones de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f87c6-133">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> <dt>

[<span data-ttu-id="f87c6-134">Controladores de esquema y controladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="f87c6-134">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="f87c6-135">Solucionador de origen</span><span class="sxs-lookup"><span data-stu-id="f87c6-135">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
