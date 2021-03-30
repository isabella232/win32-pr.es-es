---
title: Redistribuir Windows Media Player 10
description: Redistribuir Windows Media Player 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773446"
---
# <a name="redistributing-windows-media-player-10"></a>Redistribuir Windows Media Player 10

Puede instalar Windows Media Player 10 en Windows XP mediante el siguiente programa de instalación.

-   MP10Setup.exe

Este es un ejemplo de una línea de comandos para la instalación sin interfaz de usuario y sin solicitud de reinicio o reinicio.


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



En la tabla siguiente se muestran parámetros adicionales que puede usar con el programa de instalación de Windows Media Player 10.



| Parámetro              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedir la migración de la biblioteca.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Cree un punto de restauración del sistema anidado. Úselo si la aplicación crea un punto de restauración del sistema para anidar el punto de restauración de Windows Media Player en el punto de restauración de la aplicación.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | No permitir la creación de un punto de restauración del sistema. Esta marca deshabilitará la creación de un punto de restauración del sistema. En la mayoría de los casos, esta marca no debe usarse para la redistribución de software general. Esto solo debe usarse cuando se puede realizar una elección explícita en nombre del usuario final para no admitir la reversión de los archivos de Windows Media Player a una versión anterior del reproductor. Esta marca solo se debe usar para la instalación corporativa o la instalación del fabricante de equipos originales (OEM). |
| /DefaultService        | Establezca la tienda en línea inicial. Para obtener más información, consulte [configuración de parámetros de línea de comandos para tiendas en línea](setup-command-line-parameters-for-online-stores.md).                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Redistribuir el software de Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




