---
description: Especifica el tipo de bus de E/S utilizado por el adaptador de gráficos.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Enumeración D3DBUSTYPE (D3d9types.h)
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
ms.openlocfilehash: cece215946406bedcca2cbfdd2b64bfdb5df00208b2d84cf2aa90fdb89b516bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828385"
---
# <a name="d3dbustype-enumeration"></a>D3DBUSTYPE (enumeración)

Especifica el tipo de bus de E/S utilizado por el adaptador de gráficos.

## <a name="syntax"></a>Syntax


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

<span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ OTHER**
</dt> <dd>

Indica un tipo de bus distinto de los tipos enumerados aquí.

</dd> <dt>

<span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**
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

Bus de puerto de gráficos acelerados (AGP).

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**MODIFICADOR D3DBUSIMPL \_ DENTRO DEL CONJUNTO DE \_ \_ \_ CHIPS**
</dt> <dd>

La implementación del adaptador de gráficos está en el puente norte de un conjunto de chips de placa base. Esta marca implica que los datos nunca van a través de un bus de expansión (como PCI o AGP) cuando se transfieren de la memoria principal al adaptador de gráficos.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**LAS PISTAS DEL MODIFICADOR D3DBUSIMPL \_ EN LA PLACA DE LA MADRE AL \_ \_ \_ \_ \_ \_ CHIP**
</dt> <dd>

Indica que el adaptador de gráficos está conectado al puente norte de un conjunto de chips de la placa base mediante pistas en la placa base y que todos los chips del adaptador de gráficos se insonda en la placa base. Esta marca implica que los datos nunca van a través de un bus de expansión (como PCI o AGP) cuando se transfieren de la memoria principal al adaptador de gráficos.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**EL MODIFICADOR D3DBUSIMPL \_ REALIZA UN SEGUIMIENTO DE LA PLACA \_ \_ \_ \_ NODRIZA \_ A \_ SOCKET**
</dt> <dd>

El adaptador de gráficos está conectado al puente norte de una placa base mediante pistas en la placa base, y todos los chips del adaptador de gráficos se conectan a través de sockets a la placa base.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**CONECTOR DE PLACA DE PLACA DEL \_ MODIFICADOR \_ D3DBUSIMPL \_ \_**
</dt> <dd>

El adaptador de gráficos está conectado a la placa base a través de un conector de placa de placa.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**CONECTOR DE PLACA DEL MODIFICADOR D3DBUSIMPL \_ \_ EN \_ \_ \_ \_ \_ NUAE**
</dt> <dd>

El adaptador de gráficos está conectado a la placa base a través de un conector de placa de placa y el adaptador de gráficos está dentro de un gabinete al que no puede acceder el usuario.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**MODIFICADOR D3DBUSIMPL \_ \_ NO \_ ESTÁNDAR**
</dt> <dd>

Se establece una de las marcas XXX del MODIFICADOR \_ \_ \_ D3DBUSIMPL.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Se pueden establecer hasta tres marcas. Las marcas del intervalo 0x00 a 0x04 (**D3DBUSTYPE \_ Xxx**) proporcionan el tipo de bus básico. Las marcas del intervalo 0x10000 a 0x50000 (**D3DBUSIMPL \_ MODIFIER \_ Xxx**) modifican la descripción básica. El controlador establece una marca de tipo bus y puede establecer cero o una marca modificadora. Si el controlador establece una marca modificadora, también establece la marca **NON STANDARD DEL MODIFICADOR \_ \_ \_ D3DBUSIMPL.** Las marcas se combinan con un OR bit a **bit.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types.h (incluir D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de vídeo de Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 




