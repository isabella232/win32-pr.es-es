---
description: Motor de instalador que se usa para instalar aplicaciones o actualizaciones o servicios que se ejecutan en Windows. Configura y repara las aplicaciones instaladas. Escriba paquetes MSI personalizados para crear una instalación o actualización del programa de instalación de exe para una aplicación.
ms.assetid: c90b8cbe-d7a1-44ad-ae65-80115bd55e4f
title: Windows Installer
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: d818a3decc7cbede527929dc3756ba2edf193421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678025"
---
# <a name="windows-installer"></a>Windows Installer

> [!NOTE]
> Esta documentación está destinada a desarrolladores de software que desean usar Windows Installer para compilar paquetes de instalador para aplicaciones de. Si busca un paquete redistribuible para Windows Installer 4,5 y versiones anteriores, consulte [este artículo](windows-installer-redistributables.md). Tenga en cuenta que no hay ningún redistribuible para Windows Installer 5,0. Esta versión se incluye con el sistema operativo en Windows 7, Windows Server 2008 R2 y versiones posteriores de cliente y servidor (incluido Windows 10).

Microsoft Windows Installer es un servicio de instalación y configuración proporcionado con Windows. El servicio del instalador permite a los clientes proporcionar una mejor implementación corporativa y proporciona un formato estándar para la administración de componentes. El instalador también habilita el anuncio de las aplicaciones y características según el sistema operativo. Para obtener más información, vea [compatibilidad de la plataforma con el anuncio](platform-support-of-advertisement.md).

En esta documentación se describen Windows Installer 5,0 y versiones anteriores. No todas las capacidades disponibles en versiones posteriores de Windows Installer están disponibles en versiones anteriores. En esta documentación no se describen las versiones anteriores a Windows Installer 2,0. Los paquetes de instalación y las revisiones que se crean para Windows Installer 2,0 se pueden instalar con Windows Installer 3,0 y versiones posteriores.

Windows Installer 3,0 y versiones posteriores, puede instalar varias revisiones con una sola transacción que integre el progreso de la instalación, la reversión y los reinicios. El instalador puede aplicar revisiones en un orden específico, independientemente del orden en el que se proporcionen las revisiones al sistema. La revisión con Windows Installer 3,0 solo actualiza los archivos afectados por la revisión y puede ser mucho más rápido que las versiones anteriores del instalador. Las revisiones instaladas con Windows Installer 3,0 o posterior se pueden desinstalar en cualquier orden para dejar el estado del producto igual que si la revisión no se hubiera instalado nunca. Las cuentas con privilegios de administrador pueden usar la API de Windows Installer 3,0 y versiones posteriores para consultar e inventariar información de productos, características, componentes y revisiones. El instalador se puede usar para leer, editar y reemplazar listas de origen para orígenes de red, URL y multimedia. Los administradores pueden enumerar entre los contextos de usuario e instalar y administrar las listas de origen desde un proceso externo.

Windows Installer 4,5 y versiones posteriores pueden instalar varios paquetes de instalación mediante el [*procesamiento de transacciones*](t-gly.md). Si no se pueden instalar correctamente todos los paquetes de la transacción, o si el usuario cancela la instalación, el Windows Installer puede revertir los cambios y restaurar el equipo a su estado original. El instalador garantiza que todos los paquetes que pertenecen a una transacción de varios paquetes están instalados o ninguno de los paquetes está instalado.

A partir de Windows Installer 5,0, se puede crear un paquete para proteger nuevas cuentas, [servicios](../services/services.md)de Windows, archivos, carpetas y claves del registro. El paquete puede especificar un descriptor de seguridad que deniegue permisos, especifica la herencia de permisos de un recurso primario o especifica los permisos de una nueva cuenta. Para obtener más información, consulte [protección de recursos](securing-resources-.md). El servicio Windows Installer 5,0 puede enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de la clave del componente. Para obtener más información, vea [enumerar componentes](enumerating-components-.md). Mediante el uso de la [configuración de servicios](using-services-configuration.md), Windows Installer paquetes 5,0 pueden personalizar los servicios de un equipo. Los desarrolladores de configuración pueden usar Windows Installer 5,0 y la creación de un [solo paquete](single-package-authoring.md) para desarrollar paquetes de instalación únicos capaces de instalar una aplicación en el [contexto de instalación](installation-context.md)por equipo o por usuario.

## <a name="where-applicable"></a>Donde sea aplicable

Windows Installer permite la instalación y configuración eficientes de los productos y aplicaciones que se ejecutan en Windows. El instalador proporciona nuevas capacidades para anunciar características sin instalarlas, instalar productos a petición y agregar personalizaciones de usuario.

Windows Installer 5,0 que se ejecuta en Windows Server 2012 o Windows 8 admite la instalación de aplicaciones aprobadas en Windows RT. No se puede instalar en Windows RT un paquete de Windows Installer, revisión o transformación que no haya firmado Microsoft. La propiedad de Resumen de la [**plantilla**](template-summary.md) indica la plataforma que es compatible con una base de datos de instalación y, en este caso, debe incluir el valor de Windows RT.

Windows Installer está diseñado para el desarrollo de aplicaciones de estilo de escritorio.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta documentación está destinada a desarrolladores de software que desean crear aplicaciones que utilicen Windows Installer. Proporciona información general sobre los paquetes de instalación y el servicio de instalador. Contiene descripciones completas de la interfaz de programación de aplicaciones y los elementos de la base de datos del instalador. Esta documentación también contiene información adicional para los desarrolladores que desean usar un editor de tablas o una herramienta de creación de paquetes para realizar o mantener una instalación.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Windows Installer 5,0 está incluido en, Windows 7, Windows Server 2008 R2 y versiones posteriores. No hay ningún redistribuible para Windows Installer 5,0.

Las versiones anteriores a Windows Installer 5,0 se lanzaron con Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP y Windows 2000. [Windows Installer redistribuibles](windows-installer-redistributables.md) están disponibles para Windows Installer 4,5 y algunas versiones anteriores.

* Windows Installer 4,5 requiere Windows Server 2008, Windows Vista, Windows XP con Service Pack 2 (SP2) y versiones posteriores, y Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores.

* Windows Installer 4,0 requiere Windows Vista o Windows Server 2008. No hay ningún redistribuible para instalar Windows Installer 4,0 en otros sistemas operativos. En Windows Vista con Service Pack 1 (SP1) y Windows Server 2008 se incluye una versión actualizada de Windows Installer 4,0, que no agrega ninguna característica nueva.

* Windows Installer 3,1 requiere Windows Server 2003, Windows XP o Windows 2000 con Service Pack 3 (SP3).

* Windows Installer 3,0 requiere Windows Server 2003, Windows XP o Windows 2000 con SP3. Windows Installer 3,0 se incluye en Windows XP con Service Pack 2 (SP2). Está disponible como paquete redistribuible para Windows 2000 Server con Service Pack 3 (SP3) y Windows 2000 Server con Service Pack 4 (SP4), Windows XP RTM y Windows XP con Service Pack 1 (SP1) y Windows Server 2003 RTM.

* Windows Installer 2,0 está incluido en Windows Server 2003 y Windows XP.

* Windows Installer 2,0 está disponible como paquete para instalar o actualizar a Windows Installer 2,0 en Windows 2000. Este paquete no debe usarse para instalar o actualizar Windows Installer 2,0 en Windows Server 2003 y Windows XP.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Roadmap](roadmap-to-windows-installer-documentation.md)<br/>                        | Guía para la documentación de Windows Installer.<br/>       |
| [Información general](about-windows-installer.md)<br/>                                          | Información general sobre el instalador.<br/>          |
| [Novedades de Windows Installer](what-s-new-in-windows-installer.md)<br/>           | Enumera las adiciones y los cambios realizados en Windows Installer.<br/> |
| [Referencia](installer-function-reference.md)<br/>                                    | Documentación de funciones de Windows Installer.<br/>     |
| [Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)<br/> | Windows Installer ejemplos mediante el uso de scripts.<br/>          |



 

 

 
