---
description: En general, cada objeto de Active Directory se asigna exactamente a una instancia de WMI.
ms.assetid: c6c7f3c3-7174-4278-bf40-d99ed8bd0c8d
ms.tgt_platform: multiple
title: Asignación de instancias de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51eaec7b2c6ef121d0f65df375e1bb0fce32cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082980"
---
# <a name="mapping-active-directory-instances"></a>Asignación de instancias de Active Directory

En general, cada objeto de Active Directory se asigna exactamente a una instancia de WMI. La clase WMI correspondiente a la instancia de WMI es la misma que la clase proporcionada por el proveedor de clases de la clase Active Directory correspondiente. La propiedad clave **ADSIPath** de cada instancia se rellena con la ruta de acceso ADSI del objeto.

En este tema se describen las siguientes secciones:

-   [Asignar espacios de nombres](#mapping-namespaces)
-   [Asignar valores de atributo](#mapping-attribute-values)
-   [Asignación de asociaciones de instancia](#mapping-instance-associations)

> [!Note]  
> Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-namespaces"></a>Asignar espacios de nombres

Cada uno de los espacios de nombres en ADSI asigna uno a uno a los espacios de nombres en el \\ espacio de nombres del directorio raíz de WMI \\ . El nombre del espacio de nombres WMI es el mismo que el valor **ProgID** del proveedor de servicios de directorio que proporciona el espacio de nombres. En concreto, Active Directory se asigna al \\ espacio de nombres LDAP en el \\ espacio de nombres del directorio raíz \\ . WMI crea el \\ espacio de nombres LDAP como parte del proceso de registro del proveedor de clases.

## <a name="mapping-attribute-values"></a>Asignar valores de atributo

En la tabla siguiente se muestra la asignación entre cada atributo de un objeto Active Directory y una propiedad WMI.



| Sintaxis de Active Directory | Tipo de datos WMI                                 | Valor de propiedad WMI                                                        |
|-------------------------|-----------------------------------------------|---------------------------------------------------------------------------|
| Access-Point            | **\_cadena CIM**                               | Se asigna desde el valor de la cadena.                                      |
| Boolean                 | **\_BOOLEANO CIM**                              | Se asigna directamente al valor booleano adecuado.                         |
| Cadena sin distinción entre mayúsculas y minúsculas | **\_cadena CIM**                               | Se asigna desde el valor de la cadena.                                      |
| Cadena que distingue mayúsculas de minúsculas   | **\_cadena CIM**                               | Se asigna desde el valor de la cadena.                                      |
| Nombre completo      | **\_cadena CIM**                               | Se asigna desde el valor de la cadena.                                      |
| DN-Binary               | Objeto incrustado de clase **DN \_ con \_ binario** | Se asignan a las instancias del **DN con la clase \_ \_ String** .                    |
| DN-String               | Objeto incrustado de clase **DN \_ con \_ cadena** | Se asignan a las instancias del **DN con la clase \_ \_ String** .                    |
| Enumeración             | **\_SINT32 CIM**                               | Se asigna directamente al valor entero.                                     |
| IA5-String              | **\_cadena CIM**                               | Se asigna desde el valor de la cadena.                                      |
| Entero                 | **\_SINT32 CIM**                               | Se asigna directamente al valor entero.                                     |
| Descriptor de seguridad de NT  | Objeto incrustado de la clase **, uint8array**       | Asignadas a instancias de la clase **, uint8array** .                          |
| Cadena numérica          | **\_cadena CIM**                               | Se asigna desde el valor de la cadena.                                      |
| Identificador de objeto               | **\_cadena CIM**                               | Asignada a partir de la representación de cadena del OID; por ejemplo, "1.3.3.4". |
| Cadena de octeto            | Objeto incrustado de la clase **, uint8array**       | Asignadas a instancias de la clase **, uint8array** .                          |
| O nombre                 | **\_cadena CIM**                               | Se asigna desde el valor de la cadena.                                      |
| Presentation-Address    | **\_cadena CIM**                               | Se asigna desde el valor de la cadena.                                      |
| Cadena de caso de impresión       | **\_cadena CIM**                               | Se asigna desde el valor de la cadena.                                      |
| Vínculo de réplica            | Objeto incrustado de la clase **, uint8array**       | Asignadas a instancias de la clase **, uint8array** .                          |
| SID                     | Objeto incrustado de la clase **, uint8array**       | Asignadas a instancias de la clase **, uint8array** .                          |
| Hora                    | **\_fecha y hora de CIM**                             | Se convierte en la \_ representación de fecha y hora de CIM y se asigna.                 |
| No definido               | N/D                                           | N/D                                                                       |
| Cadena Unicode          | **\_cadena CIM**                               | Se asigna desde el valor de la cadena.                                      |
| Hora codificada UTC          | **\_fecha y hora de CIM**                             | Se convierte en la \_ representación de fecha y hora de CIM y se asigna.                 |



 

Para obtener más información sobre **, uint8array** y **DN \_ con \_ binario**, consulte [asignación de atributos](mapping-active-directory-classes.md).

## <a name="mapping-instance-associations"></a>Asignación de asociaciones de instancia

El proveedor de servicios de directorio asigna las diferentes relaciones de contenedor en Active Directory mediante el uso de instancias de la clase de [**\_ \_ \_ contención de la instancia de DS LDAP**](/previous-versions/windows/desktop/dsprov/ds-ldap-instance-containment) .

 

 
