---
description: Contiene un puntero al objeto proxy para el descriptor de presentación de aplicaciones.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: MF_PD_PMPHOST_CONTEXT atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257791"
---
# <a name="mf_pd_pmphost_context-attribute"></a>Atributo \_ MF PD \_ PMPHOST \_ CONTEXT

Contiene un puntero al objeto proxy para el descriptor de presentación de la aplicación.

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Observaciones

El host protected media path (PMP) usa este atributo para almacenar el descriptor de presentación de la aplicación en el descriptor de presentación remoto. El valor del atributo es un puntero a la [**interfaz IMFRemoteProxy.**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




