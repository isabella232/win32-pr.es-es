---
description: Puede proporcionar toda la información necesaria para configurar Agregar o quitar programas en Panel de control estableciendo los valores de determinadas propiedades del instalador en el paquete del instalador Windows la aplicación.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configuración de Agregar o quitar programas con Windows Instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48ad8499d395ffc4a5aad5491883f9c3161b78a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465492"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Configuración de Agregar o quitar programas con Windows Instalador

Puede proporcionar toda la información necesaria para configurar Agregar o quitar programas en Panel de control estableciendo los valores de determinadas propiedades del instalador en el paquete del instalador Windows la aplicación. Al establecer estas propiedades, se escriben automáticamente los valores correspondientes en el Registro. Si el instalador detecta que el producto está marcado para su eliminación completa, las operaciones se agregan automáticamente al script para quitar la carpeta Agregar o quitar programas en Panel de control información del producto.

Si una aplicación no está registrada, no aparece en Agregar o quitar programas en Panel de control. Para obtener más información, [vea Agregar y quitar una aplicación y No dejar ningún seguimiento en el Registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).

Las aplicaciones que se han instalado [](installation-context.md) en el contexto de instalación por usuario se muestran en agregar o quitar programas del usuario actual. Las aplicaciones que se han instalado en el contexto de instalación por equipo se muestran en Agregar o quitar programas de todos los usuarios. Las aplicaciones que no se han instalado por equipo y que solo se han instalado como aplicaciones por usuario para usuarios distintos del usuario actual, no aparecen en agregar o quitar programas del usuario actual.

Tenga en cuenta que los paquetes de instalación [**que usan la propiedad LIMITUI**](limitui.md) también deben contener [**ARPNOMODIFY**](arpnomodify.md). Esto es necesario para que un usuario obtenga el comportamiento correcto de Agregar o quitar programas en la utilidad Panel de control al intentar configurar un producto.

El instalador usa las siguientes [propiedades públicas para](public-properties.md) administrar Agregar o quitar programas en Panel de control.


| Nombre de propiedad | Breve descripción de la propiedad | 
|---------------|-------------------------------|
| <a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a> | Dirección URL del canal de actualización de la aplicación. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro</a>. | 
| <a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a> | Proporciona comentarios para agregar o quitar programas en el Panel de control. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro</a>. | 
| <a href="arpcontact.md"><strong>ARPCONTACT</strong></a> | Proporciona el contacto para agregar o quitar programas en el Panel de control. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro</a>. | 
| <a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a> | Ruta de acceso completa a la carpeta principal de la aplicación. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro</a>. | 
| <a href="arphelplink.md"><strong>ARPHELPLINK</strong></a> | Dirección de Internet, o dirección URL, para soporte técnico. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro</a>. | 
| <a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a> | Números de teléfono de soporte técnico. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro</a>. | 
| <a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a> | Impide la presentación de un botón Cambiar para el producto en Agregar o quitar programas en el Panel de control.<blockquote><b>Nota:</b> Esto solo afecta a la presentación en ARP. El instalador Windows todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.</blockquote><br /> | 
| <a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a> | Impide la presentación de un botón Quitar para el producto en la página Agregar o quitar programas de la Panel de control. El producto todavía se puede quitar seleccionando el botón Cambiar si el paquete de instalación se ha creado con una interfaz de usuario que proporciona la eliminación del producto como opción.<blockquote><b>Nota:</b> Esto solo afecta a la presentación en ARP. El instalador Windows todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.</blockquote><br /> | 
| <a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a> | Deshabilita el botón Reparar de la página Agregar o quitar programas de la Panel de control.<blockquote><b>Nota:</b> Esto solo afecta a la presentación en ARP. El instalador Windows todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.</blockquote><br /> | 
| <a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a> | Identifica el icono que se muestra en Agregar o quitar programas. Si no se define esta propiedad, Agregar o quitar programas especifica el icono de presentación. | 
| <a href="arpreadme.md"><strong>ARPREADME</strong></a> | Proporciona el Archivo Léame para agregar o quitar programas en Panel de control. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro</a>. | 
| <a href="arpsize.md"><strong>ARPSIZE</strong></a> | Tamaño estimado de la aplicación en KB. | 
| <a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a> | Impide la presentación de la aplicación en la lista de programas de agregar o quitar programas de la Panel de control.<blockquote><b>Nota:</b> Esto solo afecta a la presentación en ARP. El instalador Windows todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.</blockquote><br /> | 
| <a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a> | Dirección URL de la página principal de la aplicación. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro</a>. | 
| <a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a> | Dirección URL de la información de actualización de la aplicación. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro</a>. | 


> [!Note]  
> Para obtener información sobre la herramienta Establecer programa y valores predeterminados, consulte la sección Trabajar con establecer el acceso al programa y los valores [predeterminados del equipo.](/previous-versions//bb776877(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desinstalar clave del Registro](uninstall-registry-key.md)
</dt> </dl>
