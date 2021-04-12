---
description: El proveedor del Protocolo simple de administración de redes (SNMP) permite a las aplicaciones cliente obtener acceso a información de SNMP a través de Instrumental de administración de Windows (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI y SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279295"
---
# <a name="wmi-and-snmp"></a>WMI y SNMP

El proveedor del Protocolo simple de administración de redes (SNMP) permite a las aplicaciones cliente obtener acceso a información de SNMP a través de Instrumental de administración de Windows (WMI). El proveedor SNMP no se instala de forma predeterminada. Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

El Protocolo simple de administración de redes (SNMP) utiliza un esquema para definir objetos. El esquema es diferente del esquema utilizado en WMI. El esquema SNMPv1 y SNMPv2C se denomina estructura de la información de administración (SMI) y se empaqueta como archivos de base de información de administración (MIB). Los archivos MIB definen objetos mediante un lenguaje estándar: notación de sintaxis abstracta 1 (ASN. 1) y varias definiciones de macro que sirven como plantillas para describir los objetos. Las macros proporcionan información como el nombre del objeto, el identificador, la sintaxis, la descripción, los derechos de acceso, las operaciones del protocolo y la codificación del protocolo. En la tabla siguiente se muestra cómo el proveedor SNMP controla distintos aspectos de un objeto MIB.



| Tema                                                    | Descripción                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [NOTIFICATION-TYPE (macro)](notification-type-macro.md)   | Cómo se asigna la macro de **tipo de notificación** de SNMP a WMI.  |
| [Macro OBJECT-TYPE](object-type-macro.md)               | Cómo se asigna la macro **Object-Type** de SNMP a WMI.        |
| [Macro de Convención de texto](textual-convention-macro.md) | Cómo se asigna la macro de **Convención de texto** de SNMP a WMI. |
| [TRAP-TYPE (macro)](trap-type-macro.md)                   | Cómo se asigna la macro **Trap-Type** de SNMP a WMI.          |



 

El proveedor SNMP incluye un compilador que traduce los objetos MIB en objetos WMI. El compilador SNMP también puede generar errores u otros mensajes. Para obtener más información, vea [mensajes de error del compilador SNMP](snmp-compiler-error-messages.md) y [mensajes de información general](general-information-messages.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> </dl>

 

 



