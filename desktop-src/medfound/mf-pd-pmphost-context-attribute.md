---
description: Contiene un puntero al objeto de proxy para el descriptor de presentación de aplicaciones.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: MF_PD_PMPHOST_CONTEXT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423972"
---
# <a name="mf_pd_pmphost_context-attribute"></a>\_Atributo de contexto MF PD \_ PMPHOST \_

Contiene un puntero al objeto de proxy para el descriptor de presentación de la aplicación.

## <a name="data-type"></a>Tipo de datos

**IUnknown \** _

## <a name="remarks"></a>Observaciones

El host de la ruta de acceso a medios protegidos (PMP) usa este atributo para almacenar el descriptor de presentación de la aplicación en el descriptor de presentación remoto. El valor del atributo es un puntero a la interfaz [_ *IMFRemoteProxy* *](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) .

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

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos de descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




