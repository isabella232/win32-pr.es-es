---
description: La interfaz ITMedia es una representación de medios en un protocolo de descriptor de sesión (SDP, vea RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interfaz ITMedia (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfd1cf7dcf8ef294481a4687dbac950f97b4adede6a6871222292127e6255057
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034645"
---
# <a name="itmedia-interface"></a>Interfaz ITMedia

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITMedia** es una representación de medios en un protocolo de descriptor de sesión (SDP, vea RFC 2327). Esta interfaz exporta métodos para obtener y establecer propiedades de medios básicas, como el tipo . Los [**métodos ITMediaCollection::get \_ Item**](itmediacollection-get-item.md) e [**ITMediaCollection::Create**](itmediacollection-create.md) crean la **interfaz ITMedia.**

## <a name="members"></a>Miembros

La **interfaz ITMedia** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITMedia** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITMedia** tiene estos métodos.



| Método                                                          | Descripción                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**get \_ FormatCodes**](itmedia-get-formatcodes.md)             | Obtiene la lista de códigos de formato de carga de medios.<br/>                                          |
| [**get \_ MediaName**](itmedia-get-medianame.md)                 | Obtiene el nombre del medio.<br/>                                                                  |
| [**get \_ MediaTitle**](itmedia-get-mediatitle.md)               | Obtiene el título del medio.<br/>                                                                 |
| [**get \_ NumPorts**](itmedia-get-numports.md)                   | Obtiene el número de puertos necesarios para la sesión.<br/>                                      |
| [**get \_ StartPort**](itmedia-get-startport.md)                 | Obtiene el valor de puerto de 16 bits para el primer puerto.<br/>                                        |
| [**get \_ TransportProtocol**](itmedia-get-transportprotocol.md) | Obtiene el protocolo de transporte.<br/>                                                          |
| [**put \_ FormatCodes**](itmedia-put-formatcodes.md)             | Establece la lista de códigos de formato de carga de medios.<br/>                                          |
| [**put \_ MediaName**](itmedia-put-medianame.md)                 | Establece el nombre del medio.<br/>                                                                  |
| [**put \_ MediaTitle**](itmedia-put-mediatitle.md)               | Establece el título del medio.<br/>                                                                 |
| [**put \_ TransportProtocol**](itmedia-put-transportprotocol.md) | Establece el protocolo de transporte.<br/>                                                          |
| [**SetPortInfo**](itmedia-setportinfo.md)                      | Establece el valor de puerto de 16 bits para el primer puerto y el número de puertos necesarios para la sesión.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
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

 

