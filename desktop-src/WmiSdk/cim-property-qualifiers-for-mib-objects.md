---
description: El proveedor SNMP usa los siguientes calificadores de propiedad CIM al asignar definiciones de objeto MIB a definiciones de clase CIM.
ms.assetid: 6e858e7e-5c46-4350-9696-c5efa1252c00
ms.tgt_platform: multiple
title: Calificadores de propiedad CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f2a25edf9c15930202d3c8cf79d3d62b0d1dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278549"
---
# <a name="cim-property-qualifiers-for-mib-objects"></a>Calificadores de propiedad CIM para objetos MIB

El proveedor SNMP usa los siguientes calificadores de propiedad CIM al asignar definiciones de objeto MIB a definiciones de clase CIM. Un calificador obligatorio debe estar presente para que el proveedor SNMP resuelva por completo un objeto MIB. Si no se define un calificador obligatorio, se devuelve un error. Especificar un valor de calificador no válido también devuelve un error.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 



| Qualifier                          | Descripción                                                                                                                                                                                            |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bits**                           | **cadena** Obligatorio, si el calificador de **\_ Convención textual** no es igual a bits.<br/> Valores enumerados para la definición de subtipo de un bit.<br/>                                        |
| **CIMTYPE**                        | **cadena** Obligación<br/> Representación textual de CIM que da formato a un valor de protocolo CIM subyacente.<br/>                                                                                    |
| **Defval**                         | **cadena** Opta<br/> Valor predeterminado del objeto.<br/>                                                                                                                                       |
| **Descripción**                    | **cadena** Opta<br/> Descripción del objeto.<br/>                                                                                                                                    |
| **Mostrar \_ sugerencia**                  | **cadena** Opta<br/> Modo en que los datos del objeto deberían aparecer para un usuario.<br/>                                                                                                    |
| **Encoding**                       | **cadena** Opta<br/> Tipo de SNMP que se usa al codificar fotogramas de protocolo SNMPv1 y SNMPv2C.<br/>                                                                                              |
| **Enumeración**                    | **cadena** Obligatorio, si el calificador de **\_ Convención textual** no es igual a ENUMERATEDINTEGER.<br/> Valores enumerados para una definición de subtipo de entero enumerado.<br/>                  |
| **\_Longitud fija**                  | **UInt32** Opta<br/> Valor de longitud fija.<br/>                                                                                                                                           |
| [**Clave**](standard-qualifiers.md) | **Booleano** Opta<br/> Propiedad clave de una definición de clase.<br/>                                                                                                                             |
| **Orden de claves \_**                     | **UInt32** Opcional, a menos que se especifique [**key**](standard-qualifiers.md) .<br/> Orden de la propiedad de clave en la definición de clase.<br/>                                                   |
| **Nombre**                           | **cadena** Obligación<br/> Nombre implícito de la propiedad. Tenga en cuenta que este calificador no se ha definido explícitamente.<br/>                                                                           |
| **Identificador de objeto \_**             | **cadena** Obligación<br/> Identificador del objeto MIB del objeto.<br/>                                                                                                                              |
| **Sintaxis de objetos \_**                 | **cadena** Opta<br/> Definición de tipo con nombre del objeto.<br/>                                                                                                                               |
| **Lectura**                           | **Booleano** Opcional (se debe especificar al menos una de **lectura** o **escritura** )<br/> Concede acceso de lectura al objeto.<br/>                                                                     |
| **Referencia**                      | **cadena** Opta<br/> Hace referencia a otro documento que contiene más información sobre el objeto.<br/>                                                                                   |
| **Estado**                         | **cadena** Opta<br/> Indica si se debe admitir el objeto.<br/>                                                                                                               |
| **\_Convención textual**            | **cadena** Obligación<br/> Representación textual de la cláusula de sintaxis de la macro MIB de [tipo de objeto](object-type-macro.md) .<br/>                                                           |
| **Unidades**                          | **cadena** Opta<br/> Definición precisa de lo que representa el objeto.<br/>                                                                                                             |
| **\_Longitud variable**               | **cadena** Opta<br/> Valores mínimo, máximo y de longitud fija asociados a la definición de tipo del objeto.<br/>                                                                       |
| **Valor de la variable \_**                | **cadena** Opta<br/> Valores de intervalo y fijos asociados a la definición de tipo del objeto.<br/>                                                                                         |
| **\_Clave virtual**                   | **Booleano** Opta<br/> Indica que el valor de la propiedad se debe basar en el supraconjunto de información de instancia asociado a todos los objetos MIB accesibles en la definición de clase.<br/> |
| **Escritura**                          | **Booleano** Opcional (se debe especificar al menos una de **lectura** o **escritura** )<br/> Concede acceso de escritura al objeto.<br/>                                                                    |



 

 

 




