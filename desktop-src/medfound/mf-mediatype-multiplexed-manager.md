---
description: Proporciona una instancia de IMFMuxStreamMediaTypeManager que se puede usar para obtener los tipos de medios de las sub secuencias de un origen multimedia multiplexado, así como para controlar la combinación de substreams multiplexadas por el origen.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: MF_MEDIATYPE_MULTIPLEXED_MANAGER atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa96c74bbff8f4858c8467fcd13253cfedf2f5dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474171"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a>Atributo MF \_ MEDIATYPE \_ MULTIPLEXED \_ MANAGER

Proporciona una instancia de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) que se puede usar para obtener los tipos de medios de las sub secuencias de un origen multimedia multiplexado, así como para controlar la combinación de substreams multiplexadas por el origen.

## <a name="data-type"></a>Tipo de datos

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Observaciones

Pase este valor [**aATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para obtener una instancia de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1703 \[ solo para aplicaciones de escritorio\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 
