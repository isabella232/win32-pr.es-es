---
description: El proveedor Simple Network Management Protocol (SNMP) permite a las aplicaciones cliente acceder a la información de SNMP a través Windows Management Instrumentation (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI y SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f1327afe2a86a1f56f40c0a93d904148ccaf1fd0547b6cb623d9eb420c2a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992305"
---
# <a name="wmi-and-snmp"></a>WMI y SNMP

El proveedor Simple Network Management Protocol (SNMP) permite a las aplicaciones cliente acceder a la información de SNMP a través Windows Management Instrumentation (WMI). El proveedor SNMP no está instalado de forma predeterminada. Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

El Protocolo simple de administración de redes (SNMP) usa un esquema para definir objetos . El esquema es diferente del esquema utilizado en WMI. El esquema SNMPv1 y SNMPv2C se denomina estructura de información de administración (SMI) y se empaqueta como archivos de base de información de administración (MIB). Los archivos MIB definen objetos mediante un lenguaje estándar (Abstract Syntax Notation 1 (ASN.1) y una serie de definiciones de macro que sirven como plantillas para describir los objetos. Las macros proporcionan información como el nombre del objeto, el identificador, la sintaxis, la descripción, los derechos de acceso, las operaciones de protocolo y la codificación del protocolo. En la tabla siguiente se muestra cómo el proveedor SNMP controla distintos aspectos de un objeto MIB.



| Tema                                                    | Descripción                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [NOTIFICATION-TYPE (Macro)](notification-type-macro.md)   | Cómo se asigna la macro **NOTIFICATION-TYPE** de SNMP a WMI.  |
| [OBJECT-TYPE (Macro)](object-type-macro.md)               | Cómo se asigna la macro **OBJECT-TYPE** de SNMP a WMI.        |
| [TEXTUAL-CONVENTION (Macro)](textual-convention-macro.md) | Cómo se asigna la macro **TEXTUAL-CONVENTION** de SNMP a WMI. |
| [TRAP-TYPE Macro](trap-type-macro.md)                   | Cómo se asigna la macro **TRAP-TYPE** de SNMP a WMI.          |



 

El proveedor SNMP incluye un compilador que traduce objetos MIB en objetos WMI. El compilador SNMP también puede generar errores u otros mensajes. Para obtener más información, vea [Mensajes de error del compilador SNMP](snmp-compiler-error-messages.md) y Mensajes de información [general](general-information-messages.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> <dt>

[Proveedores WMI](wmi-providers.md)
</dt> </dl>

 

 



