---
description: Especifica si los metadatos se escriben en el archivo transcodificado.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: MF_TRANSCODE_SKIP_METADATA_TRANSFER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275685"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a><span data-ttu-id="30c64-103">MF \_ Transcode \_ omitir \_ atributo de transferencia de metadatos \_</span><span class="sxs-lookup"><span data-stu-id="30c64-103">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute</span></span>

<span data-ttu-id="30c64-104">Especifica si los metadatos se escriben en el archivo transcodificado.</span><span class="sxs-lookup"><span data-stu-id="30c64-104">Specifies whether metadata is written to the transcoded file.</span></span> <span data-ttu-id="30c64-105">Este atributo de contenedor se almacena en el perfil de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="30c64-105">This container attribute is stored in the transcode profile.</span></span>

## <a name="data-type"></a><span data-ttu-id="30c64-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="30c64-106">Data type</span></span>

<span data-ttu-id="30c64-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="30c64-107">**UINT32**</span></span>

<span data-ttu-id="30c64-108">\_ \_ \_ \_ En la tabla siguiente se describen los posibles valores para el atributo de transferencia de metadatos del salto de transcodificación de MF.</span><span class="sxs-lookup"><span data-stu-id="30c64-108">Possible values for the MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute are described in the following table.</span></span>



| <span data-ttu-id="30c64-109">Value</span><span class="sxs-lookup"><span data-stu-id="30c64-109">Value</span></span>                                                                        | <span data-ttu-id="30c64-110">Significado</span><span class="sxs-lookup"><span data-stu-id="30c64-110">Meaning</span></span>                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="30c64-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="30c64-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="30c64-112">Transfiere automáticamente los metadatos de nivel de archivo del archivo de código fuente al archivo transcodificado.</span><span class="sxs-lookup"><span data-stu-id="30c64-112">Automatically transfers file-level metadata from the source file to the transcoded file.</span></span><br/> |
| <dl> <span data-ttu-id="30c64-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="30c64-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="30c64-114">Los metadatos del archivo de origen no se escriben en el archivo transcodificado.</span><span class="sxs-lookup"><span data-stu-id="30c64-114">The source file metadata is not written to the transcoded file.</span></span><br/>                          |



 

## <a name="getset"></a><span data-ttu-id="30c64-115">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="30c64-115">Get/set</span></span>

<span data-ttu-id="30c64-116">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="30c64-116">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="30c64-117">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="30c64-117">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="30c64-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30c64-118">Remarks</span></span>

<span data-ttu-id="30c64-119">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="30c64-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="30c64-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30c64-120">Requirements</span></span>



| <span data-ttu-id="30c64-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="30c64-121">Requirement</span></span> | <span data-ttu-id="30c64-122">Value</span><span class="sxs-lookup"><span data-stu-id="30c64-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30c64-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30c64-123">Minimum supported client</span></span><br/> | <span data-ttu-id="30c64-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="30c64-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="30c64-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30c64-125">Minimum supported server</span></span><br/> | <span data-ttu-id="30c64-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="30c64-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="30c64-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30c64-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="30c64-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="30c64-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30c64-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="30c64-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c64-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="30c64-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="30c64-131">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="30c64-131">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="30c64-132">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="30c64-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




