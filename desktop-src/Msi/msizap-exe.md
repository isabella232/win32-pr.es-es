---
description: Msizap.exe es una utilidad de línea de comandos que quita toda la información de Windows Installer de un producto o todos los productos instalados en un equipo. Es posible que los productos instalados por el instalador no funcionen después de usar Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f29de42f41a72f06f62627489f8f44d1b21c5c76066ba1b1a990334f53c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943676"
---
# <a name="msizapexe"></a>Msizap.exe

Msizap.exe es una utilidad de línea de comandos que quita toda la información de Windows Installer de un producto o todos los productos instalados en un equipo. Es posible que los productos instalados por el instalador no funcionen después de usar Msizap.

En Windows 2000 y Windows XP, se requieren privilegios administrativos para usar Msizap.exe.

Esta herramienta solo está disponible en los componentes [Windows SDK para](platform-sdk-components-for-windows-installer-developers.md) desarrolladores Windows Instalador y no se debe redistribuir. Use la versión reciente de Msizap.exe (versión 3.1.4000.2726 o posterior) que está disponible en los componentes del SDK de Windows para desarrolladores del instalador de Windows para Windows Vista o superior. Las versiones inferiores Msizap.exe pueden quitar información sobre todas las actualizaciones que se han aplicado a otras aplicaciones en el equipo del usuario. Si se quita esta información, es posible que estas otras aplicaciones deban quitarse y reinstalarse para recibir actualizaciones adicionales.

## <a name="syntax"></a>Syntax

**msizap T**_\[ WA! \] {código de producto}_

**msizap T**_\[ \] <msi package> WA!_

**msizap \* *** \[ WA! \]* **ALLPRODUCTS**

**msizap PWSA?!**

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msizap.exe usa opciones de línea de comandos que no tienen en cuenta mayúsculas de minúsculas que se muestran en la tabla siguiente.



| Opción | Descripción                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | Quita todas las Windows del Instalador y las claves del Registro, ajusta los recuentos de DLL compartidos y detiene Windows installer. También quita la clave In-Progress y la información de reversión.                                                                           |
| a      | Solo cambia las ACL a Control total de administración para cualquier eliminación especificada.                                                                                                                                                                                            |
| e      | Para todos los usuarios, quita todos los archivos de datos Windows installer almacenados en caché que se hayan huérfano.                                                                                                                                                                       |
| p      | Quita la In-Progress clave.                                                                                                                                                                                                                                  |
| s      | Quita la información de reversión.                                                                                                                                                                                                                                 |
| t      | Quita toda la información del código de producto especificado. Cuando use esta opción, incluya el código de producto entre llaves. Esta opción se puede usar con la ruta de acceso completa al archivo .msi o con el código del producto.                                        |
| w      | Quita la Windows del instalador para todos los usuarios. Cuando no se establece esta opción, solo se quita la información del usuario actual. El uso de esta opción requiere que se cargue el perfil del usuario para que el subárbol del Registro por usuario esté disponible. |
| ?      | Ayuda detallada.                                                                                                                                                                                                                                                 |
| !      | Fuerza una respuesta "sí" a cualquier mensaje.                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



