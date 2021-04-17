---
description: La interfaz de programación de aplicaciones (API) de configuración de proporciona un conjunto de funciones a las que puede llamar la aplicación de instalación para realizar operaciones de instalación. Estas funciones de configuración funcionan con archivos INF de Windows para proporcionar la siguiente funcionalidad de configuración.
ms.assetid: 58201596-cb8c-480a-abef-896c1f9ef098
title: Información general
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32b99c6079fdb61fd6bfd0033ffccb9ebb7b922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667606"
---
# <a name="overview"></a>Información general

La interfaz de programación de aplicaciones (API) de configuración de proporciona un conjunto de funciones a las que puede llamar la aplicación de instalación para realizar operaciones de instalación. Estas funciones de configuración funcionan con archivos INF de Windows para proporcionar la siguiente funcionalidad de configuración.



| Para información acerca de                       | Vea                                                                                                                                                                         |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivos de colas                               | [Colas de archivos](file-queues.md)                                                                                                                                              |
| Instalación de archivos                            | [Colas de archivos](file-queues.md)<br/> [Instalación de aplicaciones](setup-applications.md)<br/> [Crear aplicaciones de instalación](creating-setup-applications.md)<br/> |
| Control de errores y solicitud de medios     | [Solicitud de disco y control de errores](disk-prompting-and-error-handling.md)                                                                                                  |
| Actualizar entradas del registro                   | [Instalación de aplicaciones](setup-applications.md)                                                                                                                                |
| Registrar archivos instalados                     | [Registro de archivos](file-log.md)                                                                                                                                                    |
| Almacenar las rutas de acceso de origen usadas más recientemente | [Lista de orígenes MRU](mru-source-list.md)                                                                                                                                      |



 

Las versiones de Unicode y ANSI están disponibles para la mayoría de las funciones de configuración. Los archivos de texto Unicode deben contener la marca de orden de bytes de 0xFEFF estándar para permitir que las funciones de instalación identifiquen el archivo como texto Unicode.

Aunque la API de instalación admite la solicitud de nuevos elementos multimedia y cuadros de diálogo de control de errores básicos, las funciones de configuración no proporcionan la funcionalidad del asistente ni una interfaz de usuario genérica.

Los desarrolladores deben considerar si pueden usar [Windows Installer](/windows/desktop/Msi/windows-installer-portal) para instalar sus aplicaciones en lugar de la API de instalación. Windows Installer reduce el costo total de propiedad (TCO) para los clientes, ya que les permite instalar y configurar de forma eficaz sus productos y aplicaciones. El instalador también puede proporcionar a su producto nuevas capacidades para anunciar características sin instalarlas, instalar productos a petición y agregar personalizaciones de usuario.

 

