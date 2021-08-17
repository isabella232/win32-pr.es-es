---
description: En general, cada objeto Active Directory asigna exactamente a una instancia wmi.
ms.assetid: c6c7f3c3-7174-4278-bf40-d99ed8bd0c8d
ms.tgt_platform: multiple
title: Asignación Active Directory instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a3e40a6f4a85ebb1bb3d7e1e5a5de7bc43c754ff7672f694aff05b62853dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317642"
---
# <a name="mapping-active-directory-instances"></a>Asignación Active Directory instancias

En general, cada objeto Active Directory asigna exactamente a una instancia wmi. La clase WMI correspondiente a la instancia de WMI es la misma que la clase proporcionada por el proveedor de clases de la clase Active Directory clase correspondiente. La propiedad **clave ADSIPath** de cada instancia se rellena con la ruta de acceso ADSI del objeto .

En este tema se de abordan las siguientes secciones:

-   [Asignar espacios de nombres](#mapping-namespaces)
-   [Asignación de valores de atributo](#mapping-attribute-values)
-   [Asociación de instancias de asignación](#mapping-instance-associations)

> [!Note]  
> Para obtener más información sobre la compatibilidad y la instalación de este componente en un sistema operativo específico, vea Disponibilidad del sistema operativo [de componentes WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-namespaces"></a>Asignar espacios de nombres

Cada uno de los espacios de nombres de ADSI asigna uno a uno a los espacios de nombres del espacio de nombres del \\ directorio \\ raíz de WMI. El nombre del espacio de nombres WMI es el mismo que el valor **de ProgId** del proveedor de servicios de directorio que proporciona el espacio de nombres . En concreto, Active Directory asigna al espacio \\ de nombres LDAP en el espacio de nombres del directorio \\ \\ raíz. WMI crea el espacio \\ de nombres LDAP como parte del proceso de registro del proveedor de clases.

## <a name="mapping-attribute-values"></a>Asignación de valores de atributo

En la tabla siguiente se muestra la asignación entre cada atributo de un objeto Active Directory y una propiedad WMI.



| Active Directory sintaxis | Tipo de datos WMI                                 | Valor de la propiedad WMI                                                        |
|-------------------------|-----------------------------------------------|---------------------------------------------------------------------------|
| Access-Point            | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Boolean                 | **CIM \_ BOOLEAN**                              | Se asigna directamente al valor booleano adecuado.                         |
| Cadena que no tiene en cuenta mayúsculas de minúsculas | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Cadena que distingue mayúsculas de minúsculas   | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Nombre completo      | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| DN-Binary               | Objeto incrustado de la **clase DN \_ con \_ binario** | Se asigna a instancias de la **clase DN \_ With \_ String.**                    |
| DN-String               | Objeto incrustado de la **clase DN \_ con \_ cadena** | Se asigna a instancias de la **clase DN \_ With \_ String.**                    |
| Enumeración             | **CIM \_ SINT32**                               | Se asigna directamente al valor entero.                                     |
| IA5-String              | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Entero                 | **CIM \_ SINT32**                               | Se asigna directamente al valor entero.                                     |
| NT Security Descriptor  | Objeto incrustado de la **clase Uint8Array**       | Se asigna a instancias de la **clase Uint8Array.**                          |
| Cadena numérica          | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Identificador de objeto               | **CIM \_ STRING**                               | Se asigna a partir de la representación de cadena del OID; por ejemplo, "1.3.3.4". |
| Octet String            | Objeto incrustado de la **clase Uint8Array**       | Se asigna a instancias de la **clase Uint8Array.**                          |
| Nombre OR                 | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Presentation-Address    | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Cadena de mayúsculas y minúsculas de impresión       | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Vínculo de réplica            | Objeto incrustado de la **clase Uint8Array**       | Se asigna a instancias de la **clase Uint8Array.**                          |
| SID                     | Objeto incrustado de la **clase Uint8Array**       | Se asigna a instancias de la **clase Uint8Array.**                          |
| Time                    | **CIM \_ DATETIME**                             | Se convierte en la representación DATETIME de CIM \_ y se asigna.                 |
| No definido               | N/D                                           | N/D                                                                       |
| Cadena Unicode          | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Hora codificada UTC          | **CIM \_ DATETIME**                             | Se convierte en la representación DATETIME de CIM \_ y se asigna.                 |



 

Para obtener más información sobre **Uint8Array** y **DN \_ con \_ binario,** vea [Atributos de asignación](mapping-active-directory-classes.md).

## <a name="mapping-instance-associations"></a>Asociación de instancias de asignación

El proveedor de Servicios de directorio asigna las diferentes relaciones de contenedor Active Directory mediante instancias de la clase contención de [**instancias \_ LDAP \_ \_ de DS.**](/previous-versions/windows/desktop/dsprov/ds-ldap-instance-containment)

 

 
