---
description: Las marcas enumeradas en la tabla siguiente especifican el tipo de bus de E/S usado por el adaptador de gráficos.
ms.assetid: 6c8ec020-5f12-453b-bbeb-3baabb1ca213
title: Marcas de tipo de bus de OPM (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4989a91c308a7dc82bb15e9cd577a6facd89a0a6de9a32f0ef95f400917ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973004"
---
# <a name="opm-bus-type-flags"></a>Marcas de tipo de bus OPM

Las marcas enumeradas en la tabla siguiente especifican el tipo de bus de E/S usado por el adaptador de gráficos.



| Constante o valor                                                                                                                                                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_BUS_TYPE_OTHER"></span><span id="opm_bus_type_other"></span><dl> <dt>**OPM \_ TIPO \_ DE \_ BUS OTROS**</dt> <dt>0x00000000</dt> </dl>                                                                                                                                                                      | Indica un tipo de bus distinto de los tipos enumerados aquí.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="OPM_BUS_TYPE_PCI"></span><span id="opm_bus_type_pci"></span><dl> <dt>**OPM \_ TIPO \_ DE \_ BUS PCI**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                                                            | Bus PCI.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_BUS_TYPE_PCIX"></span><span id="opm_bus_type_pcix"></span><dl> <dt>**OPM \_ TIPO \_ DE \_ BUS PCIX**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                                                         | Bus PCI-X.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_BUS_TYPE_PCIEXPRESS"></span><span id="opm_bus_type_pciexpress"></span><dl> <dt>**OPM \_ TIPO \_ DE \_ BUS PCIEXPRESS**</dt> <dt>0x00000003</dt> </dl>                                                                                                                                                       | Bus PCI Express.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_BUS_TYPE_AGP"></span><span id="opm_bus_type_agp"></span><dl> <dt>**OPM \_ TIPO \_ \_ DE BUS AGP**</dt> <dt>0x00000004</dt> </dl>                                                                                                                                                                            | Bus de puerto de gráficos acelerados (AGP).<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="opm_bus_implementation_modifier_inside_of_chipset"></span><dl> <dt>**OPM \_ MODIFICADOR DE \_ IMPLEMENTACIÓN DE BUS DENTRO DEL CONJUNTO DE \_ \_ \_ \_ CHIPS**</dt> <dt>0x00010000</dt> </dl>                                                                      | La implementación del adaptador de gráficos está en un puente norte de una placa base. Esta marca implica que los datos nunca van a través de un bus de expansión (como PCI o AGP) cuando se transfieren de la memoria principal al adaptador de gráficos. <br/>                                                                                                                                     |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_chip"></span><dl> <dt>**OPM \_ SEGUIMIENTOS \_ MODIFICADORES \_ DE IMPLEMENTACIÓN DE BUS EN LA PLACA \_ \_ \_ \_ \_ NODRIZA \_ A CHIP**</dt> <dt>0X00020000</dt> </dl>                            | El adaptador de gráficos está conectado al puente norte de una placa base mediante pistas en la placa base, y todos los chips del adaptador de gráficos (circuitos integrados) se aseron a la placa base. <br/>                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_socket"></span><dl> <dt>**OPM \_ EL MODIFICADOR \_ DE IMPLEMENTACIÓN DE BUS REALIZA UN SEGUIMIENTO EN LA PLACA \_ \_ \_ \_ \_ NODRIZA PARA \_ \_ 0X00030000**</dt> <dt></dt> </dl>                      | El adaptador de gráficos está conectado al puente norte de una placa base mediante pistas en la placa base y todos los chips del adaptador de gráficos se conectan a través de sockets a la placa base.<br/>                                                                                                                                                                               |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="opm_bus_implementation_modifier_daughter_board_connector"></span><dl> <dt>**OPM \_ CONECTOR DE \_ PLACA DEL MODIFICADOR DE IMPLEMENTACIÓN \_ \_ \_ DE \_**</dt> BUS PARA <dt>0X00040000</dt> </dl>                                                 | El adaptador de gráficos está conectado a la placa base a través de un conector de placa de placa.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="opm_bus_implementation_modifier_daughter_board_connector_inside_of_nuae"></span><dl> <dt>**OPM \_ CONECTOR DE \_ PLACA \_ PARA \_ MODIFICADORES DE IMPLEMENTACIÓN DE BUS \_ INSIDE OF \_ \_ \_ \_ NUAE**</dt> <dt>0x00050000</dt> </dl> | El adaptador de gráficos está conectado a la placa base a través de un conector de placa de placa y el adaptador de gráficos está dentro de un gabinete al que no puede acceder el usuario.<br/>                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_NON_STANDARD"></span><span id="opm_bus_implementation_modifier_non_standard"></span><dl> <dt>**OPM \_ MODIFICADOR DE \_ IMPLEMENTACIÓN \_ DE BUS \_ \_ NO**</dt> <dt>ESTÁNDAR 0x80000000</dt> </dl>                                                                                      | Modificador no estándar. (Opcional).<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="OPM_COPP_COMPATIBLE_BUS_TYPE_INTEGRATED"></span><span id="opm_copp_compatible_bus_type_integrated"></span><dl> <dt>**OPM \_ INTEGRACIÓN \_ DE TIPO DE BUS COMPATIBLE \_ \_ \_ CON COPP**</dt> <dt>0x80000000</dt> </dl>                                                                                                     | Bus integrado. Esta marca solo se usa en el modo de emulación copp. Indica que el comando y las señales de estado entre el adaptador de gráficos y otros subsistemas del equipo no están disponibles en un bus de expansión que tenga una especificación pública y un tipo de conector estándar, a menos que sea un bus de memoria. Esta marca se puede combinar con una marca **OPM \_ BUS TYPE \_ \_ Xxx.**<br/> |



## <a name="remarks"></a>Comentarios

Se pueden establecer hasta tres marcas mediante or bit a **bit.** Las marcas del intervalo 0x00 a 0x04 (**OPM \_ BUS TYPE \_ \_ Xxx**) dan el tipo de bus básico. Las marcas del intervalo 0x10000 a 0x50000 (**OPM \_ BUS IMPLEMENTATION MODIFIER \_ \_ \_ Xxx**) modifican la descripción básica. El controlador establece una marca de tipo bus y, opcionalmente, se puede configurar en una marca modificadora. Además, el controlador puede establecer opcionalmente la marca NON STANDARD DEL MODIFICADOR DE IMPLEMENTACIÓN **\_ DE BUS \_ \_ \_ de \_ OPM.**

En el modo de emulación copp, el controlador no usa las marcas modificadoras, pero puede establecer la marca **OPM \_ COPP \_ COMPATIBLE BUS \_ TYPE \_ \_ INTEGRATED.**

Las marcas OPM BUG TYPE Xxxx y \_ OPM COPP COMPATIBLE BUS TYPE INTEGRATED son equivalentes a los valores de la enumeración COPP BusType que se usa en el Protocolo de protección de salida certificado \_ \_ **\_ \_ \_ \_ \_** [**\_**](/windows/win32/api/dxva9typ/ne-dxva9typ-copp_bustype) (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones de OPM](opm-enumerations.md)
</dt> </dl>

 

 
