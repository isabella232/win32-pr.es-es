---
description: Un subárbol es un grupo lógico de claves, subclaves y valores del Registro que tiene un conjunto de archivos compatibles que contienen copias de seguridad de sus datos.
ms.assetid: fe517d88-7b03-4dc3-b3db-6a92665bca8e
title: Subárboles del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f942a275855c710de53a0d93df0b4654dd596f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371893"
---
# <a name="registry-hives"></a>Subárboles del Registro

Un *subárbol* es un grupo lógico de claves, subclaves y valores del Registro que tiene un conjunto de archivos compatibles cargados en la memoria cuando se inicia el sistema operativo o cuando un usuario inicia sesión.

Cada vez que un nuevo usuario inicia sesión en un equipo, se crea un nuevo subárbol para ese usuario con un archivo independiente para el perfil de usuario. Esto se denomina subárbol *del perfil de usuario.* El subárbol de un usuario contiene información específica del Registro relativa a la configuración de la aplicación del usuario, el escritorio, el entorno, las conexiones de red y las impresoras. Los subárboles de perfil de usuario se encuentran en la **clave HKEY \_ USERS.**

Los archivos del Registro tienen los dos formatos siguientes: estándar y más reciente. El formato estándar es el único formato admitido por Windows 2000. También es compatible con versiones posteriores de Windows compatibilidad con versiones anteriores. El formato más reciente se admite a partir de Windows XP. En las versiones de Windows que admiten el formato más reciente, los siguientes subárboles siguen utilizando el formato estándar: **HKEY \_ CURRENT \_ USER**, **HKEY \_ LOCAL MACHINE \_ \\ SAM**, **HKEY LOCAL MACHINE \_ \_ \\ Security** y **HKEY USERS \_ \\ . DEFAULT**; todos los demás subárboles usan el formato más reciente.

La mayoría de los archivos compatibles con los subárboles se encuentran en el directorio %SystemRoot% \\ System32 \\ Config. Estos archivos se actualizan cada vez que un usuario inicia sesión. Las extensiones de nombre de archivo de los archivos de estos directorios o, en algunos casos, la falta de una extensión, indican el tipo de datos que contienen. En la tabla siguiente se enumeran estas extensiones junto con una descripción de los datos del archivo.



| Extensión       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ninguno<br/> | Una copia completa de los datos de Hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| .alt<br/> | Copia de seguridad del subárbol **HKEY \_ LOCAL MACHINE \_ \\ System** crítico. Solo la clave del sistema tiene un archivo .alt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| .log<br/> | Registro de transacciones de cambios en las claves y las entradas de valor del subárbol.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| .sav<br/> | Copia de seguridad de un subárbol.<br/> **Windows Server 2003 y Windows XP/2000:** Copias de los archivos de Hive a medida que miraban al final de la fase de modo de texto en el programa de instalación. El programa de instalación tiene dos fases: modo de texto y modo gráfico. El subárbol se copia en un archivo .sav después de la fase de modo de texto de la instalación para protegerlo de los errores que pueden producirse si se produce un error en la fase del modo gráfico de la instalación. Si se produce un error en la instalación durante la fase de modo gráfico, solo se repite la fase del modo gráfico cuando se reinicia el equipo. El archivo .sav se usa para restaurar los datos de Hive.<br/> |



 

En la tabla siguiente se enumeran los subárboles estándar y sus archivos compatibles.



| Subárbol del Registro                      | Archivos de compatibilidad                           |
|------------------------------------|--------------------------------------------|
| **CONFIGURACIÓN ACTUAL DE HKEY \_ \_**          | System, System.alt, System.log, System.sav |
| **USUARIO ACTUAL DE HKEY \_ \_**            | Ntuser.dat, Ntuser.dat.log                 |
| **HKEY \_ LOCAL \_ MACHINE \\ SAM**      | Sam, Sam.log, Sam.sav                      |
| **HKEY \_ LOCAL \_ MACHINE \\ Security** | Security, Security.log, Security.sav       |
| **HKEY \_ LOCAL \_ MACHINE \\ Software** | Software, Software.log, Software.sav       |
| **Sistema HKEY \_ LOCAL \_ \\ MACHINE**   | System, System.alt, System.log, System.sav |
| **HKEY \_ USERS \\ . PREDETERMINADO**          | Default, Default.log, Default.sav          |



 

 

 




