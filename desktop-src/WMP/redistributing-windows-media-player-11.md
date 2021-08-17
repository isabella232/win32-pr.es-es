---
title: Redistribuir Reproductor de Windows Media 11
description: Redistribuir Reproductor de Windows Media 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec17042165ed891370d1543fad303150c4b21d1f1db7f9da38de9f75d02876a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746564"
---
# <a name="redistributing-windows-media-player-11"></a>Redistribuir Reproductor de Windows Media 11

Puede instalar Reproductor de Windows Media 11 en Windows XP mediante uno de los siguientes programas de instalación, donde *localeId* es un identificador de configuración regional.

-   wmp11-windowsxp-x86-*localeId*.exe
-   wmp11-windowsxp-x64-*localeId*.exe

Este es un ejemplo de una línea de comandos para la instalación sin interfaz de usuario y sin símbolo del sistema de reinicio o reinicio.


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



En la tabla siguiente se muestran parámetros adicionales que puede usar con Reproductor de Windows Media programa de instalación de 11.



| Parámetro              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Evitar la migración de bibliotecas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Cree un punto de restauración del sistema anidado. Úsenos si la aplicación crea un punto de restauración del sistema para anidar el Reproductor de Windows Media de restauración dentro del punto de restauración de la aplicación.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | No permitir la creación de un punto de restauración del sistema. Esta marca deshabilitará la creación de un punto de restauración del sistema. En la mayoría de las circunstancias, esta marca no debe usarse para la redistribución general de software. Esto solo se debe usar cuando se puede realizar una elección explícita en nombre del usuario final para no admitir la reversión de los archivos Reproductor de Windows Media a una versión anterior del Reproductor. Esta marca solo debe usarse para la implementación corporativa o la instalación del fabricante de equipos originales (OEM). |
| /DefaultService        | Establezca la tienda en línea inicial. Para obtener más información, vea [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Redistribuir Reproductor de Windows Media Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




