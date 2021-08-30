---
description: Proporciona una instancia de IMFMuxStreamAttributesManager que administra LOSATTRIBUTE QUE describen las sub secuencias de un origen multimedia multiplexado.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: MF_DEVICESTREAM_MULTIPLEXED_MANAGER atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c022f2bb74756ce1a6afe471c23911c90a208e2940e9919f275df10a78ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956665"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a>Atributo \_ MF DEVICESTREAM \_ MULTIPLEXED \_ MANAGER

Proporciona una instancia [**de IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) que administra [**los ELEMENTOS IMFAttribute que**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) describen las sub secuencias de un origen multimedia multiplexado.

## <a name="data-type"></a>Tipo de datos

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Comentarios

Pase este valor [**aATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para determinar si el origen multimedia proporciona secuencias multiplexadas y, si es así, obtener una instancia de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 
