---
title: Establecer el modo de traducción de entidad y contexto
description: La aplicación WinSNMP puede especificar la interpretación y traducción de los parámetros de entidad y contexto mediante el establecimiento de la entidad y el modo de traducción de contexto. La implementación de Microsoft WinSNMP almacena el modo en una base de datos.
ms.assetid: 2550f235-1351-440a-8b4e-f0d30b058229
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50b5ecfb1a4703795f970f5d7c13ceaa3d64980
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075425"
---
# <a name="setting-the-entity-and-context-translation-mode"></a>Establecer el modo de traducción de entidad y contexto

La aplicación WinSNMP puede especificar la interpretación y traducción de los parámetros de entidad y contexto mediante el establecimiento de la entidad y el modo de traducción de contexto. La implementación de Microsoft WinSNMP almacena el modo en una base de datos.

La configuración de la entidad y el modo de traducción de contexto determina la manera en que la función [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) y la función [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) interpretan las cadenas de entrada. La configuración también determina el tipo de cadena de salida que devuelven las funciones [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) y [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) . Para obtener más información, consulte compatibilidad con las [cadenas de direcciones IPX en WinSNMP](support-for-ipx-address-strings-in-winsnmp.md).

La implementación devuelve la entidad predeterminada actual y el modo de traducción de contexto en el parámetro *nTranslateMode* de la función [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) . Para recuperar la entidad actual y el modo de traducción de contexto en vigor para la implementación, una aplicación puede llamar a la función [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) en cualquier momento.

A continuación se indican los modos de traducción de contexto y entidad válidos.

| Mode                      | Significado                                                                                                                                                                                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ traducido       | La implementación utiliza su base de datos para traducir nombres descriptivos para entidades SNMP y objetos administrados. La implementación de los traduce en sus componentes SNMPv1 o SNMPv2C.                                                                                                  |
| SNMPAPI no \_ traducido \_ v1 | La implementación de interpreta los parámetros de entidad SNMP como direcciones de transporte SNMP literales y parámetros de contexto como cadenas de comunidad SNMP literales. En el caso de las entidades de destino de SNMPv2, la implementación crea mensajes SNMP salientes que contienen un valor de cero en el campo versión. |
| SNMPAPI sin \_ traducir \_ V2 | La implementación de interpreta los parámetros de entidad SNMP como direcciones de transporte SNMP y parámetros de contexto como cadenas de comunidad SNMP literales. En el caso de las entidades de destino de SNMPv2, la implementación crea mensajes SNMP salientes que contienen un valor de 1 en el campo versión.            |



 

La implementación intenta asociar los recursos de su base de datos con la dirección de transporte literal de la entidad de administración.

Para cambiar la entidad y el modo de conversión de contexto, la configuración de una aplicación WinSNMP debe llamar a la función [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) . Si el modo de traducción solicitado no es válido, se produce un error en la función y [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) devuelve el código de error snmpapi \_ modo \_ no válido.

 

 




