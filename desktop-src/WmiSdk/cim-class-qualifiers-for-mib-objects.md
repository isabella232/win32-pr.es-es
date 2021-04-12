---
description: El proveedor SNMP usa los siguientes calificadores de clase CIM al asignar definiciones de objeto MIB a definiciones de clase CIM.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: Calificadores de clase CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278553"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a>Calificadores de clase CIM para objetos MIB

El proveedor SNMP usa los siguientes calificadores de clase CIM al asignar definiciones de objeto MIB a definiciones de clase CIM. Un calificador obligatorio debe estar presente para que el proveedor SNMP resuelva por completo un objeto de grupo. Si no se define un calificador obligatorio, se devuelve un error. Especificar un valor de calificador no válido también devuelve un error.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 



| Qualifier           | Descripción                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Descripción**     | **cadena** Opta<br/> Descripción de la clase.<br/>                                                                      |
| **ObjectId de grupo \_** | **cadena** Obligatorio, si la clase es para el proveedor de clase SNMP.<br/> Identificador de objeto de la colección fabricada.<br/> |
| **\_Importaciones de módulos** | **cadena** Opta<br/> Lista separada por comas de nombres de módulos MIB utilizados para resolver importaciones.<br/>                              |
| **Nombre del módulo \_**    | **cadena** Opta<br/> Nombre de identidad de un módulo MIB.<br/>                                                                 |
| **Referencia**       | **cadena** Opta<br/> Hace referencia a otro documento que contiene más información sobre la clase.<br/>                     |
| **Simple**       | **Booleano** Obligatorio para las clases asignadas desde colecciones escalares.<br/> Indica una clase que solo puede tener una instancia.<br/>  |



 

 

 




