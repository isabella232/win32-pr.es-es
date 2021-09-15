---
description: Windows Dispositivos portátiles admite las siguientes propiedades de asociación de red.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Propiedades de asociación de red (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360192"
---
# <a name="network-association-properties"></a>Propiedades de asociación de red

Windows Dispositivos portátiles admite las siguientes propiedades de asociación de red.



| Propiedad                                                  | VarType                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IDENTIFICADORES DE \_ RED DE HOST DE \_ \_ \_ ASOCIACIÓN DE REDES \_ WPD** | **VT \_ VECTOR \| VT \_ UI1** | Lista de identificadores de host EUI-64 válidos para esta asociación. Se trata de una matriz de bytes que contiene un número entero de direcciones de red físicas EUI-64. Estos valores EUI-64 son las direcciones de red físicas disponibles en el host en tiempo de asociación de red. Si el host tiene direcciones de red físicas MAC-48 (típicas de las redes IPv4), cada dirección MAC-48 se codificará en la dirección EUI-64 como las dos mitades de la dirección MAC-48 separadas por FF-FF.<br/> |
| **WPD \_ NETWORK \_ ASSOCIATION \_ X509V3SEQUENCE**             | **VT \_ VECTOR \| VT \_ UI1** | Secuencia de certificados X.509 v3 que se va a proporcionar para la autenticación de servidor TLS.                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




