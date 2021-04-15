---
description: Las siguientes herramientas solo están disponibles en los componentes de Windows SDK para los desarrolladores de Windows Installer.
ms.assetid: b1305eaf-cd25-4684-a593-d8b1aac83592
title: Herramientas de desarrollo de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f4d3cfdac2bae4c131b47e1c5e0cf7a63fc5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360860"
---
# <a name="windows-installer-development-tools"></a>Herramientas de desarrollo de Windows Installer

Las siguientes herramientas solo están disponibles en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).



| Utilidad                          | Descripción                                                                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Instmsi.exe](instmsi-exe.md)   | Paquete redistribuible para instalar el Windows Installer en sistemas operativos Windows anteriores a Windows me.                                                                                                                               |
| [Msicert.exe](msicert-exe.md)   | Rellena la tabla MsiDigitalSignature y la tabla MsiDigitalCertificate con la información de firma digital que pertenece a los archivos contenedores externos en la tabla de medios.                                                                           |
| [Msidb.exe](msidb-exe.md)       | Importa y exporta tablas y secuencias de base de datos, combina bases de datos y aplica transformaciones.                                                                                                                                                       |
| [Msifiler.exe](msifiler-exe.md) | Rellena la tabla de archivos con versiones de archivo, idiomas y tamaños basados en un directorio de origen. También puede actualizar la tabla MsiFileHash con los hash de archivo.                                                                                      |
| [Msiinfo.exe](msiinfo-exe.md)   | Edita o muestra el [flujo de información de Resumen](summary-information-stream.md).                                                                                                                                                                  |
| [Msimerg.exe](msimerg-exe.md)   | Combina una base de datos en otra.                                                                                                                                                                                                                |
| [Msimsp.exe](msimsp-exe.md)     | Herramienta de creación de revisiones. El método recomendado para generar un paquete de revisión es usar una herramienta de creación de revisiones como Msimsp.exe con PATCHWIZ.DLL.                                                                                                 |
| [Msistuff.exe](msistuff-exe.md) | Muestra o configura los recursos del ejecutable Setup.exe bootstrap.                                                                                                                                                                      |
| [MSITool. Mak](msitool-mak.md)   | Archivo make que se puede utilizar para realizar herramientas y acciones personalizadas.                                                                                                                                                                                      |
| [Msitran.exe](msitran-exe.md)   | Genera una transformación o aplica un archivo de transformación a una base de datos.                                                                                                                                                                                 |
| [Msival2.exe](msival2-exe.md)   | Ejecuta uno o un conjunto de [evaluadores de coherencia internos (CIEM)](internal-consistency-evaluators-ices.md).                                                                                                                                       |
| [Msizap.exe](msizap-exe.md)     | Quita Windows Installer información de un producto o de todos los productos instalados en un equipo.                                                                                                                                                      |
| [Orca.exe](orca-exe.md)         | Editor de base de datos. Crea y edita archivos. msi y módulos de combinación.                                                                                                                                                                                 |
| [PATCHWIZ.DLL](patchwiz-dll.md) | Genera un [paquete de revisión](patch-packages.md) de Windows Installer a partir de un archivo de propiedades de creación de revisiones (archivo. PCP). El método recomendado para generar un paquete de revisión es usar una herramienta de creación de revisiones como Msimsp.exe con PATCHWIZ.DLL. |
| [Wilogutl.exe](wilogutl-exe.md) | Ayuda al análisis de los archivos de registro desde una instalación Windows Installer y muestra las soluciones sugeridas a los errores.                                                                                                                              |



 

 

 



