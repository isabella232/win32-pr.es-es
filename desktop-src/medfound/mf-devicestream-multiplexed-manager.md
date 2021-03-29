---
description: Proporciona una instancia de IMFMuxStreamAttributesManager que administra el IMFAttributes que describe las subsecuencias de un origen de medios multiplexado.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: MF_DEVICESTREAM_MULTIPLEXED_MANAGER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648262"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a>MF \_ DEVICESTREAM \_ atributo de \_ Administrador multiplexado

Proporciona una instancia de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) que administra el [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) que describe las subsecuencias de un origen de medios multiplexado.

## <a name="data-type"></a>Tipo de datos

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Observaciones

Pase este valor a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para determinar si el origen multimedia proporciona secuencias multiplexadas y, si es así, obtener una instancia de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
