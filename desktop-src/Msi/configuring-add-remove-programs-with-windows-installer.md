---
description: Puede proporcionar toda la información necesaria para configurar Agregar o quitar programas en Panel de control estableciendo los valores de determinadas propiedades del instalador en el paquete del instalador Windows aplicación.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configuración de agregar o quitar programas con Windows instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99e1393eb586cfe1067840e4622fddd777a84512f55f9e82f7c9fad3b1f5688f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638754"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Configuración de agregar o quitar programas con Windows instalador

Puede proporcionar toda la información necesaria para configurar Agregar o quitar programas en Panel de control estableciendo los valores de determinadas propiedades del instalador en el paquete del instalador Windows aplicación. Al establecer estas propiedades, se escriben automáticamente los valores correspondientes en el Registro. Si el instalador detecta que el producto está marcado para su eliminación completa, las operaciones se agregan automáticamente al script para quitar la carpeta Agregar o quitar programas en Panel de control información del producto.

Si una aplicación no está registrada, no aparece en Agregar o quitar programas en Panel de control. Para obtener más información, vea [Agregar y quitar una aplicación y No dejar ningún seguimiento en el Registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).

Las aplicaciones que se han instalado [](installation-context.md) en el contexto de instalación por usuario se muestran en agregar o quitar programas del usuario actual. Las aplicaciones que se han instalado en el contexto de instalación por máquina se muestran en Agregar o quitar programas de todos los usuarios. Las aplicaciones que no se han instalado por equipo y que solo se han instalado como aplicaciones por usuario para usuarios distintos del usuario actual, no aparecen en la página Agregar o quitar programas del usuario actual.

Tenga en cuenta que los paquetes de instalación [**que usan la propiedad LIMITUI**](limitui.md) también deben contener [**ARPNOMODIFY**](arpnomodify.md). Esto es necesario para que un usuario obtenga el comportamiento correcto de Agregar o quitar programas en la utilidad Panel de control al intentar configurar un producto.

El instalador usa las siguientes [propiedades públicas para](public-properties.md) administrar Agregar o quitar programas en Panel de control.

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
<td>Dirección URL del canal de actualización de la aplicación. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro.</a></td>
</tr>
<tr class="even">
<td><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></td>
<td>Proporciona comentarios para agregar o quitar programas en el Panel de control. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro.</a></td>
</tr>
<tr class="odd">
<td><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></td>
<td>Proporciona el contacto para agregar o quitar programas en el Panel de control. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro.</a></td>
</tr>
<tr class="even">
<td><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></td>
<td>Ruta de acceso completa a la carpeta principal de la aplicación. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro.</a></td>
</tr>
<tr class="odd">
<td><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></td>
<td>Dirección de Internet, o dirección URL, para soporte técnico. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro.</a></td>
</tr>
<tr class="even">
<td><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></td>
<td>Números de teléfono de soporte técnico. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro.</a></td>
</tr>
<tr class="odd">
<td><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></td>
<td>Impide la presentación de un botón Cambiar para el producto en Agregar o quitar programas en el Panel de control.
<blockquote>
<b>Nota:</b> Esto solo afecta a la presentación en ARP. El Windows de aplicaciones sigue siendo capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></td>
<td>Impide la presentación de un botón Quitar para el producto en agregar o quitar programas en el Panel de control. El producto todavía se puede quitar seleccionando el botón Cambiar si el paquete de instalación se ha creado con una interfaz de usuario que proporciona la eliminación del producto como opción.
<blockquote>
<b>Nota:</b> Esto solo afecta a la presentación en ARP. El Windows de aplicaciones sigue siendo capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></td>
<td>Deshabilita el botón Reparar de la ventana Agregar o quitar programas de la Panel de control.
<blockquote>
<b>Nota:</b> Esto solo afecta a la presentación en ARP. El Windows de aplicaciones sigue siendo capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></td>
<td>Identifica el icono que se muestra en Agregar o quitar programas. Si no se define esta propiedad, Agregar o quitar programas especifica el icono de presentación.</td>
</tr>
<tr class="odd">
<td><a href="arpreadme.md"><strong>ARPREADME</strong></a></td>
<td>Proporciona el Archivo Léame para agregar o quitar programas en Panel de control. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro.</a></td>
</tr>
<tr class="even">
<td><a href="arpsize.md"><strong>ARPSIZE</strong></a></td>
<td>Tamaño estimado de la aplicación en KB.</td>
</tr>
<tr class="odd">
<td><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></td>
<td>Impide la presentación de la aplicación en la lista de programas de agregar o quitar programas del Panel de control.
<blockquote>
<b>Nota:</b> Esto solo afecta a la presentación en ARP. El Windows de aplicaciones sigue siendo capaz de reparar, instalar a petición y desinstalar aplicaciones a través de una línea de comandos o la interfaz de programación.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></td>
<td>Dirección URL de la página principal de la aplicación. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro.</a></td>
</tr>
<tr class="odd">
<td><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></td>
<td>Dirección URL de la información de actualización de la aplicación. Valor que escribe el instalador en desinstalar la <a href="uninstall-registry-key.md">clave del Registro.</a></td>
</tr>
</tbody>
</table>

> [!Note]  
> Para obtener información sobre la herramienta Establecer programa y valores predeterminados, consulte la sección [Working with Set Program Access and Computer Defaults](/previous-versions//bb776877(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desinstalar clave del Registro](uninstall-registry-key.md)
</dt> </dl>
