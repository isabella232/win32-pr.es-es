---
description: Un subárbol es un grupo lógico de claves, subclaves y valores del registro que tiene un conjunto de archivos auxiliares que contienen copias de seguridad de sus datos.
ms.assetid: fe517d88-7b03-4dc3-b3db-6a92665bca8e
title: Subárboles del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f942a275855c710de53a0d93df0b4654dd596f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910321"
---
# <a name="registry-hives"></a>Subárboles del registro

Un *subárbol* es un grupo lógico de claves, subclaves y valores del registro que tiene un conjunto de archivos auxiliares que se cargan en la memoria cuando se inicia el sistema operativo o cuando un usuario inicia sesión.

Cada vez que un usuario nuevo inicia sesión en un equipo, se crea un nuevo Hive para ese usuario con un archivo independiente para el perfil de usuario. Esto se denomina *subárbol de Perfil de usuario*. El subárbol de un usuario contiene información específica del registro relativa a la configuración de la aplicación del usuario, el escritorio, el entorno, las conexiones de red y las impresoras. Los subárboles de Perfil de usuario se encuentran en la clave de **\_ usuarios HKEY** .

Los archivos de registro tienen los dos formatos siguientes: estándar y más reciente. El formato estándar es el único formato que admite Windows 2000. También se admite en versiones posteriores de Windows por compatibilidad con versiones anteriores. El formato más reciente se admite a partir de Windows XP. En las versiones de Windows que admiten el formato más reciente, los siguientes subárboles siguen usando el formato estándar: **HKEY \_ Current \_ User**, **HKEY \_ local \_ Machine \\ Sam**, **HKEY \_ local \_ Machine \\ Security** y **HKEY \_ users \\ . Valor predeterminado**; el resto de subárboles usan el formato más reciente.

La mayoría de los archivos auxiliares para los subárboles se encuentran en el directorio% SystemRoot% \\ system32 \\ config. Estos archivos se actualizan cada vez que un usuario inicia sesión. Las extensiones de nombre de archivo de los archivos de estos directorios o, en algunos casos, una falta de extensión, indican el tipo de datos que contienen. En la tabla siguiente se enumeran estas extensiones junto con una descripción de los datos del archivo.



| Extensión       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ninguno<br/> | Una copia completa de los datos de Hive.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| . Alt<br/> | Una copia de seguridad del subárbol de **\_ \_ \\ sistema del equipo local HKEY** crítico. Solo la clave del sistema tiene un archivo. Alt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| .log<br/> | Un registro de transacciones de los cambios en las entradas de claves y valores del subárbol.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| . SAV<br/> | Una copia de seguridad de un subárbol.<br/> **Windows Server 2003 y Windows XP/2000:** Copias de los archivos de Hive tal como se encontraban al final de la fase de modo de texto del programa de instalación. El programa de instalación de tiene dos fases: el modo de texto y el modo de gráficos. El subárbol se copia en un archivo. SAV después de la fase de modo de texto del programa de instalación para protegerlo de los errores que pueden producirse si se produce un error en la fase del programa de instalación en modo gráfico. Si se produce un error en el programa de instalación durante la fase de modo gráficos, solo se repite la fase de modo gráfico cuando se reinicia el equipo. el archivo. SAV se usa para restaurar los datos de Hive.<br/> |



 

En la tabla siguiente se enumeran los subárboles estándar y sus archivos auxiliares.



| Subárbol del registro                      | Archivos auxiliares                           |
|------------------------------------|--------------------------------------------|
| **HKEY \_ \_ configuración actual**          | System, System. Alt, System. log, System. SAV |
| **HKEY \_ Current \_ User**            | Ntuser. dat, Ntuser. dat. log                 |
| **HKEY \_ \_ equipo local \\ Sam**      | Sam, Sam. log, Sam. SAV                      |
| **HKEY \_ local \_ Machine \\ Security** | Security, Security. log, Security. SAV       |
| **HKEY \_ \_ software de máquina local \\** | Software, software. log, software. SAV       |
| **HKEY \_ \_ \\ sistema del equipo local**   | System, System. Alt, System. log, System. SAV |
| **\_los usuarios HKEY \\ . PREDETERMINADA**          | Default. log, default. SAV          |



 

 

 




