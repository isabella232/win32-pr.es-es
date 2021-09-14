---
description: En general, cada objeto Active Directory asigna exactamente a una instancia wmi.
ms.assetid: c6c7f3c3-7174-4278-bf40-d99ed8bd0c8d
ms.tgt_platform: multiple
title: Asignación Active Directory instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51eaec7b2c6ef121d0f65df375e1bb0fce32cc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967147"
---
# <a name="mapping-active-directory-instances"></a>Asignación Active Directory instancias

En general, cada objeto Active Directory asigna exactamente a una instancia wmi. La clase WMI correspondiente a la instancia de WMI es la misma que la clase proporcionada por el proveedor de clases de la clase Active Directory clase. La propiedad **clave ADSIPath** de cada instancia se rellena con la ruta de acceso adsi del objeto.

En este tema se de abordan las secciones siguientes:

-   [Asignación de espacios de nombres](#mapping-namespaces)
-   [Asignación de valores de atributo](#mapping-attribute-values)
-   [Asociación de instancias de asignación](#mapping-instance-associations)

> [!Note]  
> Para obtener más información sobre la compatibilidad y la instalación de este componente en un sistema operativo específico, vea Disponibilidad del [sistema operativo de componentes WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-namespaces"></a>Asignación de espacios de nombres

Cada uno de los espacios de nombres de ADSI asigna uno a uno a los espacios de nombres del espacio de nombres del \\ \\ directorio raíz wmi. El nombre del espacio de nombres WMI es el mismo que el valor **de ProgId** del proveedor de servicios de directorio que proporciona el espacio de nombres . En concreto, Active Directory asigna al espacio \\ de nombres LDAP en el espacio de nombres del directorio \\ \\ raíz. WMI crea el espacio \\ de nombres LDAP como parte del proceso de registro del proveedor de clases.

## <a name="mapping-attribute-values"></a>Asignación de valores de atributo

En la tabla siguiente se muestra la asignación entre cada atributo de un objeto Active Directory y una propiedad WMI.



| Active Directory sintaxis | Tipo de datos WMI                                 | Valor de la propiedad WMI                                                        |
|-------------------------|-----------------------------------------------|---------------------------------------------------------------------------|
| Access-Point            | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Boolean                 | **CIM \_ BOOLEAN**                              | Se asigna directamente al valor booleano adecuado.                         |
| Cadena que no tiene en cuenta mayúsculas de minúsculas | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Cadena que distingue mayúsculas de minúsculas   | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Nombre completo      | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| DN-Binary               | Objeto incrustado de clase **DN \_ con \_ binary** | Se asigna a instancias de la **clase DN \_ With \_ String.**                    |
| DN-String               | Objeto incrustado de clase **DN \_ con \_ cadena** | Se asigna a instancias de la **clase DN \_ With \_ String.**                    |
| Enumeración             | **CIM \_ SINT32**                               | Se asigna directamente al valor entero.                                     |
| IA5-String              | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Entero                 | **CIM \_ SINT32**                               | Se asigna directamente al valor entero.                                     |
| NT Security Descriptor  | Objeto incrustado de clase **Uint8Array**       | Asignado a instancias de la **clase Uint8Array.**                          |
| Cadena numérica          | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Identificador de objeto               | **CIM \_ STRING**                               | Asignado a partir de la representación de cadena del OID; por ejemplo, "1.3.3.4". |
| Cadena de octeto            | Objeto incrustado de clase **Uint8Array**       | Asignado a instancias de la **clase Uint8Array.**                          |
| Nombre OR                 | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Presentation-Address    | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Cadena de caso de impresión       | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Vínculo de réplica            | Objeto incrustado de la **clase Uint8Array**       | Asignado a instancias de la **clase Uint8Array.**                          |
| SID                     | Objeto incrustado de clase **Uint8Array**       | Asignado a instancias de la **clase Uint8Array.**                          |
| Time                    | **CIM \_ DATETIME**                             | Se convierte en la representación DATETIME de CIM \_ y se asigna.                 |
| No definido               | N/D                                           | N/D                                                                       |
| Cadena Unicode          | **CIM \_ STRING**                               | Asignado a partir del valor de la cadena.                                      |
| Hora codificada UTC          | **CIM \_ DATETIME**                             | Se convierte en la representación DATETIME de CIM \_ y se asigna.                 |



 

Para obtener más información sobre **Uint8Array** y **DN \_ con \_ binario,** vea [Atributos de asignación.](mapping-active-directory-classes.md)

## <a name="mapping-instance-associations"></a>Asociación de instancias de asignación

El proveedor de servicios de directorio asigna las distintas relaciones de contenedor Active Directory mediante instancias de la clase contención de instancias [**\_ LDAP \_ \_ de DS.**](/previous-versions/windows/desktop/dsprov/ds-ldap-instance-containment)

 

 
