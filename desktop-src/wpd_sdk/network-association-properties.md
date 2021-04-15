---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de Asociación de red.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Propiedades de la Asociación de red (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708910"
---
# <a name="network-association-properties"></a>Propiedades de la Asociación de red

Los dispositivos portátiles de Windows admiten las siguientes propiedades de Asociación de red.



| Propiedad                                                  | VarType                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ \_ identificadores de red de host de Asociación de red de WPD \_** | **VT \_ Vector \| VT \_ UI1** | Lista de identificadores de host EUI-64 válidos para esta asociación. Se trata de una matriz de bytes que contiene un número entero de direcciones de red física EUI-64. Estos valores EUI-64 son las direcciones de red física disponibles en el host en el momento de la Asociación de red. Si el host tiene direcciones de red física de MAC-48 (típico de redes IPv4), cada dirección MAC-48 se codificará en la dirección EUI-64 como las dos mitades de la dirección MAC-48 separadas por FF-FF.<br/> |
| **\_X509V3SEQUENCE de \_ Asociación de red de WPD \_**             | **VT \_ Vector \| VT \_ UI1** | Secuencia de certificados X. 509 V3 que se va a proporcionar para la autenticación del servidor TLS.                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




