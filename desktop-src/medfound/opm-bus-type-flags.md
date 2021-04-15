---
description: Las marcas que aparecen en la siguiente tabla especifican el tipo de bus de e/s que usa el adaptador de gráficos.
ms.assetid: 6c8ec020-5f12-453b-bbeb-3baabb1ca213
title: Marcas de tipo de bus OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae3e6988d6bcd33015b0efc5b12561ef3373a9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543883"
---
# <a name="opm-bus-type-flags"></a>Marcas de tipo de bus OPM

Las marcas que aparecen en la siguiente tabla especifican el tipo de bus de e/s que usa el adaptador de gráficos.



| Constante o valor                                                                                                                                                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_BUS_TYPE_OTHER"></span><span id="opm_bus_type_other"></span><dl> <dt>**OPM \_ Tipo de BUS \_ \_ otro**</dt> <dt>0x00000000</dt> </dl>                                                                                                                                                                      | Indica un tipo de bus distinto de los tipos que se enumeran aquí.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="OPM_BUS_TYPE_PCI"></span><span id="opm_bus_type_pci"></span><dl> <dt>**OPM \_ Tipo de BUS \_ \_ PCI**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                                                            | Bus PCI.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_BUS_TYPE_PCIX"></span><span id="opm_bus_type_pcix"></span><dl> <dt>**OPM \_ Tipo de BUS \_ \_ PCIX**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                                                         | Bus PCI-X.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_BUS_TYPE_PCIEXPRESS"></span><span id="opm_bus_type_pciexpress"></span><dl> <dt>**OPM \_ Tipo de BUS \_ \_ PCIEXPRESS**</dt> <dt>0x00000003</dt> </dl>                                                                                                                                                       | Bus PCI Express.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_BUS_TYPE_AGP"></span><span id="opm_bus_type_agp"></span><dl> <dt>**OPM \_ Tipo de BUS \_ \_ AGP**</dt> <dt>0x00000004</dt> </dl>                                                                                                                                                                            | Bus del puerto de gráficos acelerado (AGP).<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="opm_bus_implementation_modifier_inside_of_chipset"></span><dl> <dt>**OPM \_ \_ \_ Modificador de implementación \_ de bus dentro \_ de 0x00010000 de \_ chipset**</dt> <dt></dt> </dl>                                                                      | La implementación del adaptador de gráficos está en el puente norte del chipset de la placa base. Esta marca implica que los datos nunca atraviesan un bus de expansión (como PCI o AGP) cuando se transfieren de la memoria principal al adaptador de gráficos. <br/>                                                                                                                                     |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_chip"></span><dl> <dt>**OPM \_ \_ \_ \_ Seguimientos del modificador \_ de implementación de bus de la \_ \_ placa madre \_ a \_ chip**</dt> <dt>0x00020000</dt> </dl>                            | El adaptador de gráficos se conecta al puente norte del chipset de la placa base siguiendo las pistas de la placa base, y todos los chips del adaptador de gráficos (circuitos integrados) se soldan a la placa base. <br/>                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_socket"></span><dl> <dt>**OPM \_ \_ \_ Pistas del modificador \_ \_ de implementación de bus de la \_ \_ placa madre a un \_ \_ socket**</dt> <dt>0x00030000</dt> </dl>                      | El adaptador de gráficos se conecta al puente norte del chipset de la placa base siguiendo las pistas de la placa base, y todos los chips del adaptador de gráficos se conectan a través de sockets a la placa base.<br/>                                                                                                                                                                               |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="opm_bus_implementation_modifier_daughter_board_connector"></span><dl> <dt>**OPM \_ Conector de la \_ \_ \_ \_ placa \_ secundaria del modificador de implementación de bus**</dt> <dt>0x00040000</dt> </dl>                                                 | El adaptador de gráficos se conecta a la placa base a través de un conector de daughterboard.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="opm_bus_implementation_modifier_daughter_board_connector_inside_of_nuae"></span><dl> <dt>**OPM \_ \_ \_ \_ \_ Conector de la placa secundaria del modificador de implementación de bus \_ \_ dentro \_ de \_ NUAE**</dt> <dt>0x00050000</dt> </dl> | El adaptador de gráficos se conecta a la placa base a través de un conector de daughterboard y el adaptador de gráficos está dentro de un contenedor que no es accesible para el usuario.<br/>                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_NON_STANDARD"></span><span id="opm_bus_implementation_modifier_non_standard"></span><dl> <dt>**OPM \_ \_Modificador de implementación de bus \_ \_ no \_ estándar**</dt> <dt>0x80000000</dt> </dl>                                                                                      | Modificador no estándar. (Opcional).<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="OPM_COPP_COMPATIBLE_BUS_TYPE_INTEGRATED"></span><span id="opm_copp_compatible_bus_type_integrated"></span><dl> <dt>**OPM \_ \_Tipo de bus compatible con COPP \_ \_ \_ Integrated**</dt> <dt>0x80000000</dt> </dl>                                                                                                     | Bus integrado. Esta marca solo se usa en el modo de emulación de COPP. Indica que las señales de comando y estado entre el adaptador de gráficos y otros subsistemas del equipo no están disponibles en un bus de expansión que tenga una especificación pública y un tipo de conector estándar, a menos que sea un bus de memoria. Esta marca se puede combinar con una marca de **tipo de bus de OPM \_ \_ \_ XXX** .<br/> |



## <a name="remarks"></a>Observaciones

Se pueden establecer hasta tres marcas, mediante **una operación OR** bit a bit. Las marcas en el intervalo de 0x00 a 0x04 (**\_ tipo de bus OPM \_ \_ XXX**) proporcionan el tipo de bus básico. Las marcas en el intervalo de 0x10000 a 0x50000 (**\_ \_ \_ modificador de \_ implementación de bus OPM XXX**) modifican la descripción básica. El controlador establece una marca de tipo bus y puede configurar opcionalmente una marca de modificador. Además, el controlador puede establecer opcionalmente la marca **del \_ modificador de implementación de bus de OPM \_ \_ \_ no \_ estándar** .

En el modo de emulación de COPP, el controlador no usa las marcas de modificador, pero podría establecer la marca **\_ integrada de \_ \_ \_ tipo \_ de bus compatible de COPP de OPM** .

El \_ tipo de error OPM \_ \_ xxxx flags y el marcador de **\_ \_ \_ \_ tipo \_ de bus compatible OPM de OPM** son equivalentes a los valores de la enumeración [**COPP \_ BusType**](/windows/win32/api/dxva9typ/ne-dxva9typ-copp_bustype) usada en el protocolo de protección de la salida certificada (COPP).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de OPM](opm-enumerations.md)
</dt> </dl>

 

 
