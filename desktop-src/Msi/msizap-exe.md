---
description: Msizap.exe es una utilidad de línea de comandos que quita toda la información Windows Installer de un producto o de todos los productos instalados en un equipo. Es posible que los productos instalados por el instalador no funcionen después de usar Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082462"
---
# <a name="msizapexe"></a>Msizap.exe

Msizap.exe es una utilidad de línea de comandos que quita toda la información Windows Installer de un producto o de todos los productos instalados en un equipo. Es posible que los productos instalados por el instalador no funcionen después de usar Msizap.

En Windows 2000 y Windows XP, se necesitan privilegios administrativos para usar Msizap.exe.

Esta herramienta solo está disponible en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md) y no se debe redistribuir. Use la versión reciente de Msizap.exe (versión 3.1.4000.2726 o superior) que está disponible en los componentes de Windows SDK para Windows Installer desarrolladores de Windows Vista o superior. Las versiones inferiores de Msizap.exe pueden quitar información acerca de todas las actualizaciones que se han aplicado a otras aplicaciones en el equipo del usuario. Si se quita esta información, es posible que sea necesario quitar y volver a instalar estas otras aplicaciones para recibir actualizaciones adicionales.

## <a name="syntax"></a>Sintaxis

¡ **Msizap T**_\[ wa! \] {código de producto}_

¡ **Msizap T**_\[ wa \] <msi package> !_

**\* *** Msizap \[ WA \]* **ALLPRODUCTS**

**PWSA de Msizap?**

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msizap.exe usa las opciones de línea de comandos que no distinguen mayúsculas de minúsculas que se muestran en la tabla siguiente.



| Opción | Descripción                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | Quita todos los Windows Installer carpetas y claves del registro, ajusta los recuentos de DLL compartidas y detiene Windows Installer servicio. También quita la In-Progress clave y la información de reversión.                                                                           |
| a      | Solo cambia las ACL al control total de administración para cualquier eliminación especificada.                                                                                                                                                                                            |
| e      | Para todos los usuarios, quita todos los archivos de datos Windows Installer almacenados en caché que se hayan huérfano.                                                                                                                                                                       |
| p      | Quita la clave de In-Progress.                                                                                                                                                                                                                                  |
| s      | Quita la información de reversión.                                                                                                                                                                                                                                 |
| t      | Quita toda la información del código de producto especificado. Al usar esta opción, incluya el código de producto entre llaves. Esta opción se puede usar con la ruta de acceso completa al archivo. msi o con el código del producto.                                        |
| w      | Quita Windows Installer información de todos los usuarios. Cuando no se establece esta opción, solo se quita la información del usuario actual. El uso de esta opción requiere que se cargue el perfil del usuario para que el subárbol del registro por usuario del usuario esté disponible. |
| ?      | Ayuda detallada.                                                                                                                                                                                                                                                 |
| !      | Fuerza una respuesta "sí" a cualquier solicitud.                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



