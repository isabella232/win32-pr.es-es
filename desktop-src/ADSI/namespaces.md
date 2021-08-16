---
title: Espacios de nombres
description: Los objetos que residen dentro de un espacio de nombres determinado se identifican mediante un nombre único.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- adsi de espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d416782f2a96ca716f6e803ad9d0b4200c82cff6ad0ad033751a89a5d2c8af1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839390"
---
# <a name="namespaces"></a>Espacios de nombres

Los objetos que residen dentro de un espacio de nombres determinado se identifican mediante un nombre único. Por ejemplo, los archivos almacenados en una unidad de disco del equipo residen en el espacio de nombres del sistema de archivos. El nombre único de un archivo se basa en dónde se almacena en el espacio de nombres del sistema de archivos. Por ejemplo:


```C++
C:\public\documents\adsi\adsi_spec.doc
```



Los espacios de nombres del servicio de directorio también identifican los objetos que contienen por nombres únicos que normalmente se basan en la ubicación del directorio donde se puede encontrar el objeto. Por ejemplo, en un directorio X.500, un objeto determinado podría tener un nombre como el siguiente:


```C++
CN=John,OU=Marketing,O=Fabrikam
```



Los distintos servicios de directorio usan formularios diferentes para asignar nombres a los objetos que contienen. Esto dificulta el trabajo con distintos espacios de nombres, especialmente para los desarrolladores, teniendo en cuenta todos los distintos entornos en los que el código podría estar en ejecución.

Un objetivo de Active Directory Service Interfaces (ADSI) es proporcionar un marco de nomenclatura que permita el acceso a espacios de nombres de diferentes proveedores de servicios de directorio.

ADSI define una convención de nomenclatura que puede identificar de forma única un objeto en un entorno heterogéneo. Estos nombres se denominan cadenas ADsPath. Las cadenas ADsPath tienen varias formas:


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



Los distintos proveedores adsi pueden introducir formatos ADsPath adicionales (como el proveedor adsi para el servidor Internet Information Services, que admite los ADsPath de "IIS://").

 

 




