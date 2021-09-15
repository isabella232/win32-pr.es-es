---
description: El motor del instalador que se usa para instalar aplicaciones, actualizaciones o servicios se ejecuta en Windows. Configura y repara las aplicaciones instaladas. Escriba paquetes msi personalizados para crear una instalación de exe o actualizar o actualizar para una aplicación.
ms.assetid: c90b8cbe-d7a1-44ad-ae65-80115bd55e4f
title: Windows Installer
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 1d990dc2b285c1f7b9c2b263f3841c62825d5162
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476865"
---
# <a name="windows-installer"></a>Windows Installer

> [!NOTE]
> Esta documentación está pensada para desarrolladores de software que desean usar Windows Installer para compilar paquetes de instalador para aplicaciones. Si busca un redistribuible para Windows Installer 4.5 y versiones anteriores, consulte [este artículo](windows-installer-redistributables.md). Tenga en cuenta que no hay ningún redistribuible para Windows Installer 5.0. Esta versión se incluye con el sistema operativo en Windows 7, Windows Server 2008 R2 y versiones posteriores de cliente y servidor (incluidas Windows 10).

Microsoft Windows Installer es un servicio de instalación y configuración proporcionado con Windows. El servicio de instalador permite a los clientes proporcionar una mejor implementación corporativa y proporciona un formato estándar para la administración de componentes. El instalador también habilita el anuncio de aplicaciones y características según el sistema operativo. Para obtener más información, vea [Compatibilidad con plataformas de anuncios.](platform-support-of-advertisement.md)

En esta documentación se Windows Installer 5.0 y versiones anteriores. No todas las funcionalidades disponibles en versiones posteriores Windows Installer están disponibles en versiones anteriores. En esta documentación no se describen las versiones anteriores a Windows Installer 2.0. Los paquetes de instalación y las revisiones que se crean para Windows Installer 2.0 todavía se pueden instalar mediante Windows Installer 3.0 y versiones posteriores.

Windows El instalador 3.0 y versiones posteriores pueden instalar varias revisiones con una única transacción que integre el progreso de la instalación, la reversión y los reinicios. El instalador puede aplicar revisiones en un orden especificado, independientemente del orden en que se proporcionan las revisiones al sistema. La aplicación de revisiones Windows Installer 3.0 solo actualiza los archivos afectados por la revisión y puede ser significativamente más rápida que las versiones anteriores del instalador. Las revisiones instaladas con Windows Installer 3.0 o posterior se pueden desinstalar en cualquier orden para dejar el estado del producto igual que si la revisión nunca se hubiera instalado. Las cuentas con privilegios de administrador pueden usar la API de Windows Installer 3.0 y versiones posteriores para consultar e inventariar información de productos, características, componentes y revisiones. El instalador se puede usar para leer, editar y reemplazar listas de origen para orígenes de red, dirección URL y medios. Los administradores pueden enumerar entre contextos de usuario e instalación, y administrar listas de origen desde un proceso externo.

Windows El instalador 4.5 y versiones posteriores pueden instalar varios paquetes de instalación mediante el [*procesamiento de transacciones*](t-gly.md). Si todos los paquetes de la transacción no se pueden instalar correctamente o si el usuario cancela la instalación, el instalador de Windows puede revertir los cambios y restaurar el equipo a su estado original. El instalador garantiza que todos los paquetes que pertenecen a una transacción de varios paquetes están instalados o ninguno de los paquetes están instalados.

A partir Windows Installer 5.0, se puede crear un paquete para proteger nuevas cuentas, Windows [Services,](../services/services.md)archivos, carpetas y claves del Registro. El paquete puede especificar un descriptor de seguridad que deniegue permisos, especifique la herencia de permisos de un recurso primario o especifique los permisos de una nueva cuenta. Para obtener información, vea [Securing Resources](securing-resources-.md). El Windows Installer 5.0 puede enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de clave para el componente. Para obtener más información, [vea Enumerating Components](enumerating-components-.md). Mediante [la configuración de servicios](using-services-configuration.md), Windows Installer 5.0 pueden personalizar los servicios en un equipo. Los desarrolladores de instalación pueden usar Windows Installer 5.0 y Single [Package Authoring](single-package-authoring.md) para desarrollar paquetes de instalación única capaces de instalar una aplicación en el contexto de instalación por equipo o por [usuario.](installation-context.md)

## <a name="where-applicable"></a>Donde sea aplicable

Windows El instalador permite la instalación y configuración eficaces de los productos y aplicaciones que se ejecutan en Windows. El instalador proporciona nuevas funcionalidades para anunciar características sin instalarlas, instalar productos a petición y agregar personalizaciones de usuario.

Windows El instalador 5.0 que se ejecuta Windows Server 2012 o Windows 8 admite la instalación de aplicaciones aprobadas en Windows RT. Un Windows, revisión o transformación del instalador que no haya sido firmado por Microsoft no se puede instalar en Windows RT. La [**propiedad Resumen de**](template-summary.md) plantilla indica la plataforma que es compatible con una base de datos de instalación y, en este caso, debe incluir el valor de Windows RT.

Windows El instalador está pensado para el desarrollo de aplicaciones de estilo de escritorio.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Esta documentación está pensada para desarrolladores de software que desean crear aplicaciones que usan Windows Installer. Proporciona información general sobre los paquetes de instalación y el servicio de instalador. Contiene descripciones completas de la interfaz de programación de aplicaciones y elementos de la base de datos del instalador. Esta documentación también contiene información complementaria para los desarrolladores que desean usar un editor de tablas o una herramienta de creación de paquetes para realizar o mantener una instalación.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Windows Installer 5.0 se incluye con, Windows 7, Windows Server 2008 R2 y versiones posteriores. No hay ningún redistribuible para Windows Installer 5.0.

Las versiones anteriores a Windows Installer 5.0 se publicaron con Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP y Windows 2000. [Windows Installer Redistributables](windows-installer-redistributables.md) están disponibles para Windows Installer 4.5 y algunas versiones anteriores.

* Windows El instalador 4.5 requiere Windows Server 2008, Windows Vista, Windows XP con Service Pack 2 (SP2) y versiones posteriores, y Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores.

* Windows El instalador 4.0 requiere Windows Vista o Windows Server 2008. No hay ningún redistribuible para instalar Windows Installer 4.0 en otros sistemas operativos. Hay disponible una versión actualizada de Windows Installer 4.0, que no agrega nuevas características, en Windows Vista con Service Pack 1 (SP1) y Windows Server 2008.

* Windows El instalador 3.1 requiere Windows Server 2003, Windows XP o Windows 2000 con Service Pack 3 (SP3).

* Windows El instalador 3.0 requiere Windows Server 2003, Windows XP o Windows 2000 con SP3. Windows El instalador 3.0 se incluye en Windows XP con Service Pack 2 (SP2). Está disponible como redistribuible para Windows Server con Service Pack 3 (SP3) y Windows 2000 Server con Service Pack 4 (SP4), Windows XP RTM y Windows XP con Service Pack 1 (SP1) y Windows Server 2003 RTM.

* Windows El instalador 2.0 se encuentra en Windows Server 2003 y Windows XP.

* Windows Installer 2.0 está disponible como paquete para instalar o actualizar a Windows Installer 2.0 en Windows 2000. Este paquete no debe usarse para instalar o actualizar Windows Installer 2.0 en Windows Server 2003 y Windows XP.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Roadmap](roadmap-to-windows-installer-documentation.md)<br/>                        | Una guía para obtener Windows installer.<br/>       |
| [Información general](about-windows-installer.md)<br/>                                          | Información general sobre el instalador.<br/>          |
| [Novedades del instalador de Windows](what-s-new-in-windows-installer.md)<br/>           | Enumera las adiciones y los cambios en Windows Installer.<br/> |
| [Referencia](installer-function-reference.md)<br/>                                    | Documentación de las Windows Installer.<br/>     |
| [Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)<br/> | Windows Ejemplos del instalador mediante script.<br/>          |



 

 

 
