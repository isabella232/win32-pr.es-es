---
description: Especifica el tipo de bus de e/s utilizado por el adaptador de gráficos.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Enumeración D3DBUSTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714921"
---
# <a name="d3dbustype-enumeration"></a>Enumeración D3DBUSTYPE

Especifica el tipo de bus de e/s utilizado por el adaptador de gráficos.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ otro**
</dt> <dd>

Indica un tipo de bus distinto de los tipos que se enumeran aquí.

</dd> <dt>

<span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**\_PCI D3DBUSTYPE**
</dt> <dd>

Bus PCI.

</dd> <dt>

<span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIX**
</dt> <dd>

Bus PCI-X.

</dd> <dt>

<span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIEXPRESS**
</dt> <dd>

Bus PCI Express.

</dd> <dt>

<span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**
</dt> <dd>

Bus del puerto de gráficos acelerado (AGP).

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL \_ modificador \_ dentro \_ del \_ chipset**
</dt> <dd>

La implementación del adaptador de gráficos está en el puente norte del chipset de la placa base. Esta marca implica que los datos nunca atraviesan un bus de expansión (como PCI o AGP) cuando se transfieren de la memoria principal al adaptador de gráficos.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL el \_ modificador \_ realiza un seguimiento \_ de la \_ placa madre en \_ \_ \_ chip**
</dt> <dd>

Indica que el adaptador de gráficos está conectado al puente norte del chipset de la placa base mediante el seguimiento de la placa base y que todos los chips del adaptador gráfico están soldados a la placa base. Esta marca implica que los datos nunca atraviesan un bus de expansión (como PCI o AGP) cuando se transfieren de la memoria principal al adaptador de gráficos.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL el \_ modificador \_ realiza un seguimiento \_ de la \_ placa madre \_ \_ \_ en el socket**
</dt> <dd>

El adaptador de gráficos se conecta al puente norte del chipset de la placa base siguiendo las pistas de la placa base, y todos los chips del adaptador de gráficos se conectan a través de sockets a la placa base.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_Conector de la \_ \_ placa secundaria del modificador D3DBUSIMPL \_**
</dt> <dd>

El adaptador de gráficos se conecta a la placa base a través de un conector de daughterboard.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_ \_ Conector de la placa secundaria del modificador D3DBUSIMPL \_ \_ \_ dentro \_ de \_ NUAE**
</dt> <dd>

El adaptador de gráficos se conecta a la placa base a través de un conector de daughterboard y el adaptador de gráficos está dentro de un contenedor que no es accesible para el usuario.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_Modificador D3DBUSIMPL \_ no \_ estándar**
</dt> <dd>

Se establece una de las marcas de modificador XXX del modificador D3DBUSIMPL \_ \_ \_ .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se pueden establecer tres marcas como máximo. Las marcas en el intervalo de 0x00 a 0x04 (**D3DBUSTYPE \_ XXX**) proporcionan el tipo de bus básico. Las marcas en el intervalo de 0x10000 a 0x50000 (**D3DBUSIMPL \_ modificador \_ XXX**) modifican la descripción básica. El controlador establece una marca de tipo bus y puede establecer cero o un marcador de modificador. Si el controlador establece una marca de modificador, también establece la marca del **\_ modificador D3DBUSIMPL \_ no \_ estándar** . Las marcas se combinan con una **operación OR** bit a bit.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>D3d9types. h (incluye d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de vídeo de Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 




