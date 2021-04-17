---
description: La interfaz ITMedia es una representación de los medios en un protocolo de descriptor de sesión (SDP, consulte RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interfaz ITMedia (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680464"
---
# <a name="itmedia-interface"></a>Interfaz ITMedia

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITMedia** es una representación de los medios en un protocolo de descriptor de sesión (SDP, consulte RFC 2327). Esta interfaz exporta métodos para obtener y establecer las propiedades de los elementos multimedia básicos, como el tipo. Los métodos [**ITMediaCollection:: get \_ Item**](itmediacollection-get-item.md) y [**ITMediaCollection:: Create**](itmediacollection-create.md) crean la interfaz **ITMedia** .

## <a name="members"></a>Miembros

La interfaz **ITMedia** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITMedia** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITMedia** tiene estos métodos.



| Método                                                          | Descripción                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**obtener \_ FormatCodes**](itmedia-get-formatcodes.md)             | Obtiene la lista de códigos de formato de carga de medios.<br/>                                          |
| [**obtener \_ MEDIANAME**](itmedia-get-medianame.md)                 | Obtiene el nombre del medio.<br/>                                                                  |
| [**obtener \_ MediaTitle**](itmedia-get-mediatitle.md)               | Obtiene el título del medio.<br/>                                                                 |
| [**obtener \_ NumPorts**](itmedia-get-numports.md)                   | Obtiene el número de puertos necesarios para la sesión.<br/>                                      |
| [**obtener \_ StartPort**](itmedia-get-startport.md)                 | Obtiene el valor del puerto de 16 bits para el primer puerto.<br/>                                        |
| [**obtener \_ TransportProtocol**](itmedia-get-transportprotocol.md) | Obtiene el protocolo de transporte.<br/>                                                          |
| [**Put \_ FormatCodes**](itmedia-put-formatcodes.md)             | Establece la lista de códigos de formato de carga de medios.<br/>                                          |
| [**Put \_ MEDIANAME**](itmedia-put-medianame.md)                 | Establece el nombre del medio.<br/>                                                                  |
| [**Put \_ MediaTitle**](itmedia-put-mediatitle.md)               | Establece el título del medio.<br/>                                                                 |
| [**Put \_ TransportProtocol**](itmedia-put-transportprotocol.md) | Establece el protocolo de transporte.<br/>                                                          |
| [**SetPortInfo**](itmedia-setportinfo.md)                      | Establece el valor del puerto de 16 bits para el primer puerto y el número de puertos necesarios para la sesión.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**ITSDP**](itsdp.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

