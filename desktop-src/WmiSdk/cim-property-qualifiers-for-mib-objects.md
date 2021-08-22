---
description: El proveedor SNMP usa los siguientes calificadores de propiedad CIM al asignar definiciones de objetos MIB a definiciones de clase CIM.
ms.assetid: 6e858e7e-5c46-4350-9696-c5efa1252c00
ms.tgt_platform: multiple
title: Calificadores de propiedades CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2fd45f250b603fcea97040a35faf43f6343311094e97a52ca06823e99bfcac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131717"
---
# <a name="cim-property-qualifiers-for-mib-objects"></a>Calificadores de propiedades CIM para objetos MIB

El proveedor SNMP usa los siguientes calificadores de propiedad CIM al asignar definiciones de objetos MIB a definiciones de clase CIM. Debe haber un calificador obligatorio para que el proveedor SNMP resuelva completamente un objeto MIB. Si no se define un calificador obligatorio, se devuelve un error. Si se especifica un valor de calificador no válido, también se devuelve un error.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configurar el entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 



| Qualifier                          | Descripción                                                                                                                                                                                            |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bits**                           | **string** Obligatorio, si el **\_ calificador Textual Convention** no es igual a BITS.<br/> Valores enumerados para la definición de subtipo de un bit.<br/>                                        |
| **Cimtype**                        | **string** Obligatorio<br/> Representación textual cim que da formato a un valor de protocolo CIM subyacente.<br/>                                                                                    |
| **Defval**                         | **string** Opcional<br/> Valor predeterminado del objeto.<br/>                                                                                                                                       |
| **Descripción**                    | **string** Opcional<br/> Descripción del objeto.<br/>                                                                                                                                    |
| **Sugerencia para \_ mostrar**                  | **string** Opcional<br/> Manera en que los datos del objeto deben aparecer a un usuario.<br/>                                                                                                    |
| **Encoding**                       | **string** Opcional<br/> Tipo SNMP usado al codificar tramas de protocolo SNMPv1 y SNMPv2C.<br/>                                                                                              |
| **Enumeración**                    | **string** Obligatorio, si el **\_ calificador Textual Convention** no es igual a ENUMERATEDINTEGER.<br/> Valores enumerados para una definición de subtipo entero enumerado.<br/>                  |
| **Longitud \_ fija**                  | **uint32** Opcional<br/> Valor de longitud fija.<br/>                                                                                                                                           |
| [**Clave**](standard-qualifiers.md) | **Bool** Opcional<br/> Propiedad key de una definición de clase.<br/>                                                                                                                             |
| **Orden de \_ claves**                     | **uint32** Opcional, a menos [**que se**](standard-qualifiers.md) especifique Key.<br/> Orden de la propiedad key en la definición de clase.<br/>                                                   |
| **Nombre**                           | **string** Obligatorio<br/> Nombre implícito de la propiedad. Tenga en cuenta que este calificador no está definido explícitamente.<br/>                                                                           |
| **Identificador de \_ objeto**             | **string** Obligatorio<br/> Identificador de objeto MIB del objeto.<br/>                                                                                                                              |
| **Sintaxis de \_ objetos**                 | **string** Opcional<br/> Definición de tipo con nombre del objeto.<br/>                                                                                                                               |
| **Lectura**                           | **Bool** Opcional (se debe especificar **al** **menos** una de lectura o escritura)<br/> Concede acceso de lectura al objeto .<br/>                                                                     |
| **Referencia**                      | **string** Opcional<br/> Hace referencia a otro documento que contiene más información sobre el objeto .<br/>                                                                                   |
| **Estado**                         | **string** Opcional<br/> Indica si el objeto debe ser compatible.<br/>                                                                                                               |
| **Convención \_ textual**            | **string** Obligatorio<br/> Representación textual de la cláusula SYNTAX de la macro [MIB OBJECT-TYPE.](object-type-macro.md)<br/>                                                           |
| **Unidades**                          | **string** Opcional<br/> Definición precisa de lo que representa el objeto.<br/>                                                                                                             |
| **Longitud \_ variable**               | **string** Opcional<br/> Valores mínimos, máximos y de longitud fija asociados a la definición de tipo del objeto.<br/>                                                                       |
| **Valor de \_ variable**                | **string** Opcional<br/> Valores fijos y con intervalos asociados a la definición de tipo del objeto.<br/>                                                                                         |
| **Clave \_ virtual**                   | **Bool** Opcional<br/> Indica que el valor de la propiedad debe basarse en el superconjunto de información de instancia asociado a todos los objetos MIB accesibles en la definición de clase.<br/> |
| **Escritura**                          | **Bool** Opcional (se debe especificar **al** **menos** una de lectura o escritura)<br/> Concede acceso de escritura al objeto .<br/>                                                                    |



 

 

 




