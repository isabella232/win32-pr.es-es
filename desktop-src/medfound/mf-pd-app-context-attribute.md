---
description: Contiene un puntero al descriptor de presentación desde la ruta de acceso multimedia protegida (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: MF_PD_APP_CONTEXT atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360697"
---
# <a name="mf_pd_app_context-attribute"></a>Atributo MF \_ PD \_ APP \_ CONTEXT

Contiene un puntero al descriptor de presentación desde la ruta de acceso multimedia protegida (PMP).

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Observaciones

El proxy de origen multimedia, que se crea en el proceso PMP, usa este atributo para almacenar el descriptor de presentación remoto en el descriptor de presentación de la aplicación.

El valor de este atributo es un puntero a la [**interfaz IMFPresentationDescriptor.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

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

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




