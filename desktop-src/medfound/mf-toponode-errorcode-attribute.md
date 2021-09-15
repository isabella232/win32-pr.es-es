---
description: Contiene el código de error del error de conexión más reciente para este nodo de topología.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: MF_TOPONODE_ERRORCODE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580328"
---
# <a name="mf_toponode_errorcode-attribute"></a>Atributo \_ MF TOPONODE \_ ERRORCODE

Contiene el código de error del error de conexión más reciente para este nodo de topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Ttreat como valor **HRESULT.**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a todos los tipos de nodo.

El valor de este atributo es **un valor HRESULT.**

La sesión multimedia o el cargador de topologías podrían establecer el atributo . Normalmente, las aplicaciones leen este atributo, pero no lo establecen.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**NODETopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




