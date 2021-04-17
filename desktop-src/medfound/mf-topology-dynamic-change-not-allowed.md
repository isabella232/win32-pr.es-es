---
description: Especifica si la sesión multimedia intenta modificar la topología cuando cambia el formato de una secuencia.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497356"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a>\_Atributo de cambio dinámico de topología MF \_ \_ \_ no \_ permitido

Especifica si la sesión multimedia intenta modificar la topología cuando cambia el formato de una secuencia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Observaciones

Este atributo controla el modo en que la sesión multimedia responde si el formato de una secuencia cambia durante el streaming.

Si el formato cambia y el \_ atributo el cambio dinámico de la topología MF \_ \_ \_ no \_ se permite es **false**, la sesión multimedia podría insertar nuevos nodos en la topología para que coincida con el nuevo formato. Por ejemplo, si cambia el tamaño del vídeo, es posible que la sesión multimedia agregue una Media Foundation transformación (MFT) que cambie el tamaño del vídeo. De lo contrario, si el atributo es **true**, la sesión multimedia no modificará la topología.

El valor predeterminado de este atributo es **false**. El valor recomendado es **false**.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




