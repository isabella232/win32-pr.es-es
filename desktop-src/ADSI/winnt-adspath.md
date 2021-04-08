---
title: ADsPath de Winnt
description: En este tema se incluyen ejemplos de cadenas que se usan para el ADsPath de Winnt.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- Proveedor de servicios de WinNT ADSI, ADsPath de Winnt
- ADsPath ADSI, WinNT, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea2c3db1b5234fb07045d921858766a105c4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993830"
---
# <a name="winnt-adspath"></a>ADsPath de Winnt

La cadena ADsPath del proveedor WinNT de ADSI puede ser una de las siguientes formas:


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

La ruta de acceso es la ruta de acceso de en el objeto, como "servidorimpresión1/Printer2".

El nombre del objeto es el nombre de un objeto específico.

La clase de objeto es el nombre de clase del objeto con nombre. Un ejemplo de este uso sería "WinNT://MyServer/JeffSmith,user". Especificar un nombre de clase puede mejorar el rendimiento de la operación de enlace.

 

 




