---
description: Contiene el código de error del error de conexión más reciente de este nodo topología.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: MF_TOPONODE_ERRORCODE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154989"
---
# <a name="mf_toponode_errorcode-attribute"></a>\_TOPONODE el \_ atributo ERRORCODE de MF

Contiene el código de error del error de conexión más reciente de este nodo topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Ttreat como un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Este atributo se aplica a todos los tipos de nodo.

El valor de este atributo es un valor **HRESULT** .

La sesión de medios o el cargador de topología podría establecer el atributo. Las aplicaciones normalmente leen este atributo pero no lo establecen.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




