---
description: Cada definición de objeto MIB contiene una cláusula ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) que define los derechos de acceso al objeto.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Cláusulas ACCESS y MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 985b4bfe968841436cedd352a01a609aac6ba2d725887b6a638ffcd95656935d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120945"
---
# <a name="access-and-max-access-clauses"></a>Cláusulas ACCESS y MAX-ACCESS

Cada definición de objeto MIB contiene una cláusula ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) que define los derechos de acceso al objeto.

> [!Note]  
> Para obtener más información sobre cómo instalar el proveedor, vea [Configuración del entorno SNMP de WMI.](setting-up-the-wmi-snmp-environment.md)

 

En la tabla siguiente se muestra la asignación de la cláusula ACCESS de SNMPv1.



| Cláusula ACCESS de MIB | Calificador CIM       |
|-------------------|---------------------|
| solo lectura         | **Lectura**            |
| lectura y escritura        | **Lectura** y **escritura** |
| de solo escritura        | **Escritura**           |
| no accesible    | **No \_ accesible** |



 

En la tabla siguiente se muestra la asignación de la cláusula MAX-ACCESS de SNMPv2C.



| Cláusula MIB-ACCESS     | Calificador CIM       |
|-----------------------|---------------------|
| solo lectura             | **Lectura**            |
| lectura y escritura            | **Lectura** y **escritura** |
| read-create           | **Lectura**            |
| accessible-for-notify | **No \_ accesible** |
| no accesible        | **No \_ accesible** |



 

Cuando un objeto MIB se asigna a no accesible y no es una propiedad con clave de la clase , no hay ninguna asignación del propio objeto MIB.

 

 



