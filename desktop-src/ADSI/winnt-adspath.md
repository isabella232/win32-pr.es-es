---
title: WinNT ADsPath
description: Este tema contiene ejemplos de cadenas que se usarán para WinNT ADsPath.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- ADSI del proveedor de servicios WinNT, WinNT ADsPath
- ADsPath ADSI, WinNT, description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4971209a516d9e0c759e892322c99db1807a4bf88e771281299af30abc47d47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838375"
---
# <a name="winnt-adspath"></a>WinNT ADsPath

La cadena ADsPath para el proveedor ADSI WinNT puede ser una de las siguientes formas:


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



El nombre de dominio puede ser un nombre NETBIOS o un nombre DNS.

El servidor es el nombre de un servidor específico dentro del dominio.

La ruta de acceso es la ruta de acceso de en el objeto , como "printserver1/printer2".

El nombre del objeto es el nombre de un objeto específico.

La clase de objeto es el nombre de clase del objeto con nombre. Un ejemplo de este uso sería "WinNT://MyServer/JeffSmith,user". Especificar un nombre de clase puede mejorar el rendimiento de la operación de enlace.

 

 




