---
description: Puede proporcionar toda la información necesaria para configurar agregar o quitar programas en el panel de control estableciendo los valores de determinadas propiedades del instalador en el paquete de Windows Installer de la aplicación.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configuración de agregar o quitar programas con Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/30/2021
ms.locfileid: "105994507"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Configuración de agregar o quitar programas con Windows Installer

Puede proporcionar toda la información necesaria para configurar agregar o quitar programas en el panel de control estableciendo los valores de determinadas propiedades del instalador en el paquete de Windows Installer de la aplicación. Al establecer estas propiedades, se escriben automáticamente los valores correspondientes en el registro. Si el instalador detecta que el producto está marcado para su eliminación completa, las operaciones se agregan automáticamente al script para quitar la carpeta agregar o quitar programas en la información del panel de control del producto.

Si una aplicación no está registrada, no aparece en Agregar o quitar programas en el panel de control. Para obtener más información, vea [Agregar y quitar una aplicación y no dejar ningún seguimiento en el registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).

Las aplicaciones que se han instalado en el contexto de [instalación](installation-context.md) por usuario se muestran en Agregar o quitar programas del usuario actual. Las aplicaciones que se han instalado en el contexto de instalación por equipo se muestran en Agregar o quitar programas de todos los usuarios. Las aplicaciones que no se han instalado por equipo y que solo se han instalado como aplicaciones por usuario para los usuarios que no son el usuario actual, no aparecen en Agregar o quitar programas del usuario actual.

Tenga en cuenta que los paquetes de instalación que usan la propiedad [**LIMITUI**](limitui.md) también deben contener [**ARPNOMODIFY**](arpnomodify.md). Esto es necesario para que un usuario obtenga el comportamiento correcto en Agregar o quitar programas en la utilidad del panel de control al intentar configurar un producto.

El instalador usa las siguientes [propiedades públicas](public-properties.md) para administrar agregar o quitar programas en el panel de control.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre de propiedad</th>
<th>Breve descripción de la propiedad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></td>
<td>Dirección URL del canal de actualización para la aplicación. Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</td>
</tr>
<tr class="even">
<td><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></td>
<td>Proporciona comentarios para agregar o quitar programas en el panel de control. Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></td>
<td>Proporciona el contacto para agregar o quitar programas en el panel de control. Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</td>
</tr>
<tr class="even">
<td><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></td>
<td>Ruta de acceso completa a la carpeta principal de la aplicación. Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</td>
</tr>
<tr class="odd">
<td><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></td>
<td>Dirección de Internet, o dirección URL, para obtener soporte técnico. Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</td>
</tr>
<tr class="even">
<td><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></td>
<td>Números de teléfono de soporte técnico. Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></td>
<td>Impide que se muestre un botón cambiar para el producto en Agregar o quitar programas en el panel de control.
<blockquote>
<b>Nota:</b> Esto solo afecta a la presentación en el ARP. El Windows Installer todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></td>
<td>Impide que se muestre un botón Quitar del producto en Agregar o quitar programas en el panel de control. El producto aún se puede quitar si se selecciona el botón cambiar si el paquete de instalación se ha creado con una interfaz de usuario que proporciona la eliminación del producto como opción.
<blockquote>
<b>Nota:</b> Esto solo afecta a la presentación en el ARP. El Windows Installer todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></td>
<td>Deshabilita el botón reparar en Agregar o quitar programas en el panel de control.
<blockquote>
<b>Nota:</b> Esto solo afecta a la presentación en el ARP. El Windows Installer todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></td>
<td>Identifica el icono que se muestra en Agregar o quitar programas. Si no se define esta propiedad, agregar o quitar programas especifica el icono de presentación.</td>
</tr>
<tr class="odd">
<td><a href="arpreadme.md"><strong>ARPREADME</strong></a></td>
<td>Proporciona el archivo Léame para agregar o quitar programas en el panel de control. Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</td>
</tr>
<tr class="even">
<td><a href="arpsize.md"><strong>ARPSIZE</strong></a></td>
<td>Tamaño estimado de la aplicación en KB.</td>
</tr>
<tr class="odd">
<td><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></td>
<td>Impide que la aplicación se muestre en la lista programas de agregar o quitar programas en el panel de control.
<blockquote>
<b>Nota:</b> Esto solo afecta a la presentación en el ARP. El Windows Installer todavía es capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></td>
<td>Dirección URL de la Página principal de la aplicación. Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></td>
<td>Dirección URL para la información de actualización de la aplicación. Valor que el instalador escribe en la <a href="uninstall-registry-key.md">clave del registro de desinstalación</a>.</td>
</tr>
</tbody>
</table>

> [!Note]  
> Para obtener información sobre la herramienta establecer programa y valores predeterminados, consulte la sección [trabajar con configurar acceso y programas predeterminados del equipo](/previous-versions//bb776877(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desinstalar la clave del registro](uninstall-registry-key.md)
</dt> </dl>
