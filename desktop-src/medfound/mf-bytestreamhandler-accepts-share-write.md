---
description: Especifica si un controlador de flujo de bytes puede utilizar un flujo de bytes abierto para que otro subproceso pueda escribir en él.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687216"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a><span data-ttu-id="072d0-103">MF \_ BYTESTREAMHANDLER \_ acepta el \_ atributo de escritura de recurso compartido \_</span><span class="sxs-lookup"><span data-stu-id="072d0-103">MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute</span></span>

<span data-ttu-id="072d0-104">Especifica si un controlador de flujo de bytes puede utilizar un flujo de bytes abierto para que otro subproceso pueda escribir en él.</span><span class="sxs-lookup"><span data-stu-id="072d0-104">Specifies whether a byte-stream handler can use a byte stream that is opened for writing by another thread.</span></span>

## <a name="data-type"></a><span data-ttu-id="072d0-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="072d0-105">Data type</span></span>

<span data-ttu-id="072d0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="072d0-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="072d0-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="072d0-107">Get/set</span></span>

<span data-ttu-id="072d0-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="072d0-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="072d0-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="072d0-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="072d0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="072d0-110">Remarks</span></span>

<span data-ttu-id="072d0-111">Los controladores de secuencias de bytes pueden admitir este atributo.</span><span class="sxs-lookup"><span data-stu-id="072d0-111">Byte-stream handlers can support this attribute.</span></span> <span data-ttu-id="072d0-112">Para obtener o establecer el atributo, primero consulte el controlador de flujo de bytes para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="072d0-112">To get or set the attribute, first query the byte-stream handler for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="072d0-113">Después, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) o [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span><span class="sxs-lookup"><span data-stu-id="072d0-113">Then call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) or [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)</span></span>

<span data-ttu-id="072d0-114">Si este atributo es **true**, significa que el controlador de flujo de bytes puede leer de una secuencia mientras otro subproceso escribe en la misma secuencia.</span><span class="sxs-lookup"><span data-stu-id="072d0-114">If this attribute is **TRUE**, it means that the byte-stream handler can read from a stream while another thread writes to the same stream.</span></span> <span data-ttu-id="072d0-115">Cuando un flujo se abre para escribir en otro subproceso, el método [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) devuelve la marca de **\_ \_ escritura de recurso compartido MFBYTESTREAM** .</span><span class="sxs-lookup"><span data-stu-id="072d0-115">When a stream is opened for writing by another thread, the [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) method returns the **MFBYTESTREAM\_SHARE\_WRITE** flag.</span></span>

<span data-ttu-id="072d0-116">Este atributo afecta a la resolución de código fuente.</span><span class="sxs-lookup"><span data-stu-id="072d0-116">This attribute affects source resolution.</span></span> <span data-ttu-id="072d0-117">Si una secuencia de bytes tiene establecida la marca de **\_ \_ escritura de recurso compartido MFBYTESTREAM** , la [resolución de origen](source-resolver.md) no pasará esa secuencia a un controlador de flujo de bytes a menos que el controlador tenga el \_ atributo MF BYTESTREAMHANDLER acepte el atributo de \_ \_ recurso compartido de \_ escritura establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="072d0-117">If a byte stream has the **MFBYTESTREAM\_SHARE\_WRITE** flag set, the [Source Resolver](source-resolver.md) will not pass that stream to a byte-stream handler unless the handler has the MF\_BYTESTREAMHANDLER\_ACCEPTS\_SHARE\_WRITE attribute set to **TRUE**.</span></span>

<span data-ttu-id="072d0-118">La marca de **\_ \_ escritura de recurso compartido MFBYTESTREAM** es una sugerencia de que la longitud de la secuencia podría cambiar mientras el controlador Lee de ella.</span><span class="sxs-lookup"><span data-stu-id="072d0-118">The **MFBYTESTREAM\_SHARE\_WRITE** flag is a hint that the length of the stream might change while the handler is reading from it.</span></span>

<span data-ttu-id="072d0-119">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="072d0-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="072d0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="072d0-120">Requirements</span></span>



| <span data-ttu-id="072d0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="072d0-121">Requirement</span></span> | <span data-ttu-id="072d0-122">Value</span><span class="sxs-lookup"><span data-stu-id="072d0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="072d0-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="072d0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="072d0-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="072d0-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="072d0-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="072d0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="072d0-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="072d0-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="072d0-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="072d0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="072d0-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="072d0-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="072d0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="072d0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="072d0-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="072d0-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="072d0-131">Controladores de esquema y controladores de Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="072d0-131">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




