---
description: Cada definición de objeto MIB contiene una cláusula ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) que define los derechos de acceso al objeto.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Cláusulas Access y MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697424"
---
# <a name="access-and-max-access-clauses"></a>Cláusulas Access y MAX-ACCESS

Cada definición de objeto MIB contiene una cláusula ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) que define los derechos de acceso al objeto.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

En la tabla siguiente se muestra la asignación de la cláusula de acceso SNMPv1.



| Cláusula de acceso MIB | Calificador de CIM       |
|-------------------|---------------------|
| solo lectura         | **Lectura**            |
| lectura y escritura        | **Lectura**, **escritura** |
| de solo escritura        | **Escritura**           |
| no accesible    | **No \_ accesible** |



 

En la tabla siguiente se muestra la asignación de la cláusula de acceso MAX de SNMPv2C.



| MIB: cláusula de acceso     | Calificador de CIM       |
|-----------------------|---------------------|
| solo lectura             | **Lectura**            |
| lectura y escritura            | **Lectura**, **escritura** |
| lectura y creación           | **Lectura**            |
| accesible para notificaciones | **No \_ accesible** |
| no accesible        | **No \_ accesible** |



 

Cuando un objeto MIB se asigna a no accesible y no es una propiedad con clave de la clase, no hay ninguna asignación del propio objeto MIB.

 

 



