---
description: Proporciona una instancia de IMFMuxStreamMediaTypeManager que se puede utilizar para obtener los tipos de medios de las subsecuencias de un origen de medios multiplexados, así como para controlar la combinación de subflujos multiplexados por el origen.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: MF_MEDIATYPE_MULTIPLEXED_MANAGER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa96c74bbff8f4858c8467fcd13253cfedf2f5dc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279790"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a>\_Atributo de \_ Administrador multiplexado de MEDIATYPE de MF \_

Proporciona una instancia de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) que se puede utilizar para obtener los tipos de medios de las subsecuencias de un origen de medios multiplexados, así como para controlar la combinación de subflujos multiplexados por el origen.

## <a name="data-type"></a>Tipo de datos

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Observaciones

Pase este valor a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para obtener una instancia de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
