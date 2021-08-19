---
description: Especifica si la sesión multimedia intenta modificar la topología cuando cambia el formato de una secuencia.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2e984b45abc55246c9b1ae291c535c7fbb00f01f9405d827b7fe833b57a368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875744"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a>Atributo \_ DYNAMIC CHANGE NOT \_ ALLOWED DE LA \_ \_ TOPOLOGÍA \_ DE MF

Especifica si la sesión multimedia intenta modificar la topología cuando cambia el formato de una secuencia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentarios

Este atributo controla cómo responde la sesión multimedia si cambia el formato de una secuencia durante el streaming.

Si el formato cambia y el atributo MF TOPOLOGY DYNAMIC CHANGE NOT ALLOWED es FALSE, la sesión multimedia podría insertar nuevos nodos en la topología para que coincidan \_ \_ con el nuevo \_ \_ \_ formato.  Por ejemplo, si cambia el tamaño del vídeo, la sesión multimedia podría agregar una transformación de Media Foundation (MFT) que cambie el tamaño del vídeo. De lo contrario, si el atributo **es TRUE**, la sesión multimedia no modificará la topología.

El valor predeterminado de este atributo es **FALSE.** El valor recomendado es **FALSE.**

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




