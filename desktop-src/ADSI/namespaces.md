---
title: Espacios de nombres
description: Los objetos que residen dentro de un espacio de nombres determinado se identifican mediante un nombre único.
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- ADSI de espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29d93963b2fc2b3fa6ea0eb486fe95b46ba0e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418351"
---
# <a name="namespaces"></a>Espacios de nombres

Los objetos que residen dentro de un espacio de nombres determinado se identifican mediante un nombre único. Por ejemplo, los archivos almacenados en una unidad de disco de PC residen en el espacio de nombres del sistema de archivos. El nombre único de un archivo se basa en la ubicación en la que se almacena en el espacio de nombres del sistema de archivos. Por ejemplo:


```C++
C:\public\documents\adsi\adsi_spec.doc
```



Los espacios de nombres del servicio de directorio también identifican los objetos que contienen por nombres únicos que normalmente se basan en la ubicación del directorio donde se encuentra el objeto. Por ejemplo, en un directorio X. 500, un objeto dado podría tener un nombre similar al siguiente:


```C++
CN=John,OU=Marketing,O=Fabrikam
```



Los distintos servicios de directorio usan diferentes formatos para asignar nombres a los objetos que contienen. Esto hace que trabajar con distintos espacios de nombres sea desafiante, especialmente para los desarrolladores, considerando todos los distintos entornos en los que se puede estar ejecutando el código.

El objetivo de Active Directory interfaces de servicio (ADSI) es proporcionar un marco de nomenclatura que permita el acceso a los espacios de nombres de diferentes proveedores de servicios de directorio.

ADSI define una Convención de nomenclatura que puede identificar de forma única un objeto en un entorno heterogéneo. Estos nombres se denominan cadenas ADsPath. Las cadenas ADsPath tienen varias formas:


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



Los diferentes proveedores ADSI pueden introducir formatos ADsPath adicionales (como el proveedor ADSI para el servidor de Internet Information Services, que admiten "IIS://" ADsPaths).

 

 




