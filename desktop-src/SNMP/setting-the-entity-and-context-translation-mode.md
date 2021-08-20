---
title: Establecer el modo de traducción de entidades y contexto
description: La aplicación WinSNMP puede especificar la interpretación y traducción de parámetros de entidad y contexto estableciendo el modo de traducción de entidades y contexto. La implementación de Microsoft WinSNMP almacena el modo en una base de datos.
ms.assetid: 2550f235-1351-440a-8b4e-f0d30b058229
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab459c0b33ffe1cc43c81858b57ec55942f61f2b5b736ca0124f31f52cc960d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009063"
---
# <a name="setting-the-entity-and-context-translation-mode"></a>Establecer el modo de traducción de entidades y contexto

La aplicación WinSNMP puede especificar la interpretación y traducción de parámetros de entidad y contexto estableciendo el modo de traducción de entidades y contexto. La implementación de Microsoft WinSNMP almacena el modo en una base de datos.

El valor del modo de traducción de entidades y contexto determina la manera en que la función [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) y la [**función SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) interpretan las cadenas de entrada. El valor también determina el tipo de cadena de salida que devuelven las funciones [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) y [**SnmpContextToStr.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) Para obtener más información, [vea Compatibilidad con cadenas de direcciones IPX en WinSNMP.](support-for-ipx-address-strings-in-winsnmp.md)

La implementación devuelve el modo de traducción de contexto y entidad predeterminado actual *en el parámetro nTranslateMode* de la [**función SnmpStartup.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) Para recuperar la entidad actual y el modo de traducción de contexto en vigor para la implementación, una aplicación puede llamar a la [**función SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) en cualquier momento.

Los modos de traducción de entidades y contexto válidos siguen.

| Modo                      | Significado                                                                                                                                                                                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ TRADUCIDO       | La implementación usa su base de datos para traducir nombres descriptivos para entidades SNMP y objetos administrados. La implementación los traduce en sus componentes SNMPv1 o SNMPv2C.                                                                                                  |
| SNMPAPI \_ UNTRANSLATED \_ V1 | La implementación interpreta los parámetros de entidad SNMP como direcciones de transporte SNMP literales y los parámetros de contexto como cadenas literales de la comunidad SNMP. Para las entidades de destino SNMPv2, la implementación crea mensajes SNMP salientes que contienen un valor de cero en el campo de versión. |
| SNMPAPI \_ UNTRANSLATED \_ V2 | La implementación interpreta los parámetros de entidad SNMP como direcciones de transporte SNMP y los parámetros de contexto como cadenas literales de la comunidad SNMP. Para las entidades de destino SNMPv2, la implementación crea mensajes SNMP salientes que contienen un valor de 1 en el campo de versión.            |



 

La implementación intenta asociar los recursos de su base de datos con la dirección de transporte literal de la entidad de administración.

Para cambiar la entidad y el modo de traducción de contexto que establece una aplicación WinSNMP, debe llamar a [**la función SnmpSetTranslateMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) Si el modo de traducción solicitado no es válido, se produce un error en la función y [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) devuelve el código de error SNMPAPI \_ MODE \_ INVALID.

 

 




