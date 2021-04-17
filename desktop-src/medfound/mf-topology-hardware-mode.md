---
description: Especifica si se van a cargar transformaciones de Microsoft Media Foundation basadas en hardware (MFTs) en la topología.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: MF_TOPOLOGY_HARDWARE_MODE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7933e9a380bbf5e66f4030a214f3f4aa93abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705401"
---
# <a name="mf_topology_hardware_mode-attribute"></a>Atributo de modo de hardware de \_ topología MF \_ \_

Especifica si se van a cargar transformaciones de Microsoft Media Foundation basadas en hardware (MFTs) en la topología.

## <a name="data-type"></a>Tipo de datos

**[**MFTOPOLOGY \_ \_Modo de hardware**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Observaciones

Este atributo es opcional. Establezca el atributo antes de resolver la topología.



| Value                                  | Descripción                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFTOPOLOGY \_ HWMODE \_ uso de \_ hardware**  | El cargador de topología cargará los MFTs basados en hardware, como los descodificadores de hardware, si están disponibles.<br/> El cargador de topología recurre automáticamente a la descodificación de software si no se encuentra ningún descodificador de hardware o si un descodificador de hardware no puede conectarse por algún motivo.<br/> |
| **MFTOPOLOGY \_ HWMODE \_ \_ solo software** | El cargador de topología solo cargará software MFTs, incluidos los descodificadores de software.                                                                                                                                                                                                    |



 

El valor predeterminado es **MFTOPOLOGY \_ HWMODE \_ software \_ Only**, por compatibilidad con las aplicaciones existentes. El valor recomendado es **MFTOPOLOGY \_ HWMODE \_ use \_ hardware**.

Si el cargador de topología inserta un MFT de hardware en la topología, establece el atributo de [ \_ atributo de \_ \_ dirección URL \_ de hardware de enumeración MFT](mft-enum-hardware-url-attribute.md) en el nodo de la topología. Para comprobar si existe un MFT de hardware, enumere los nodos de la topología resuelta y compruebe si este atributo está presente.

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

 

 




