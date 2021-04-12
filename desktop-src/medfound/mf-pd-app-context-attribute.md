---
description: Contiene un puntero al descriptor de presentación de la ruta de acceso a medios protegidos (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: MF_PD_APP_CONTEXT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278347"
---
# <a name="mf_pd_app_context-attribute"></a>Atributo de contexto de la \_ aplicación MF PD \_ \_

Contiene un puntero al descriptor de presentación de la ruta de acceso a medios protegidos (PMP).

## <a name="data-type"></a>Tipo de datos

**IUnknown \** _

## <a name="remarks"></a>Observaciones

El proxy de origen de medios, que se crea en el proceso de PMP, usa este atributo para almacenar el descriptor de presentación remoto en el descriptor de presentación de la aplicación.

El valor de este atributo es un puntero a la interfaz [_ *IMFPresentationDescriptor* *](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: Setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




