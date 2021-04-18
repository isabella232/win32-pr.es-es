---
description: Windows Installer proporciona a los desarrolladores de paquetes la capacidad de crear una interfaz de usuario interna que tenga varios niveles de funcionalidad.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Niveles de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279322"
---
# <a name="user-interface-levels"></a>Niveles de la interfaz de usuario

Windows Installer proporciona a los desarrolladores de paquetes la capacidad de crear una interfaz de usuario interna que tenga varios niveles de funcionalidad. Dado que el autor del paquete debe crear la interfaz de usuario interna, el comportamiento de la interfaz de usuario completa, la interfaz de usuario reducida, la interfaz de usuario básica y el nivel ninguno depende del paquete de instalación. En la tabla siguiente se describe la funcionalidad que se suele atribuir a los niveles de interfaz de usuario.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nivel de interfaz de usuario</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Interfaz de usuario completa</td>
<td>Muestra cuadros de diálogo modales y no modales creados en la interfaz de usuario interna. Muestra cuadros de <a href="error-dialog.md">diálogo de error</a> creados.
<blockquote>
[!Note]<br />
Los cuadros de diálogo modales requieren la intervención del usuario antes de que la instalación pueda continuar y se especifican estableciendo el <a href="modal-dialog-style-bit.md">bit de estilo del cuadro de diálogo modal</a> en la columna atributos de la tabla del <a href="dialog-table.md">cuadro de diálogo</a> . Un cuadro de diálogo no modal no requiere la intervención del usuario para que la instalación continúe.
</blockquote>
<br/> Una interfaz de usuario completa normalmente exhibe el <a href="user-interface-wizard-behavior.md">comportamiento del Asistente para la interfaz de usuario</a>.<br/></td>
</tr>
<tr class="even">
<td>Interfaz de usuario reducida</td>
<td>Muestra los cuadros de diálogo no modales creados en la interfaz de usuario. No muestra ningún cuadro de diálogo modal creado. Muestra cuadros de <a href="error-dialog.md">diálogo de error</a> creados. Muestra mensajes de <a href="authoring-disk-prompt-messages.md">petición de disco</a> . Muestra cuadros de <a href="filesinuse-dialog.md">diálogo de FilesInUse</a> .</td>
</tr>
<tr class="odd">
<td>Interfaz de usuario básica</td>
<td>Muestra los cuadros de diálogo no modales integrados que muestran mensajes de progreso. Muestra cuadros de diálogo de error integrados. No muestra ningún cuadro de diálogo creado. Solicita a los usuarios que inserten un disco mostrando un cuadro de diálogo que contiene el valor de la propiedad <a href="diskprompt.md"><strong>DiskPrompt</strong></a> .</td>
</tr>
<tr class="even">
<td>None</td>
<td>Ninguno significa una instalación silenciosa que no muestra ninguna interfaz de usuario.</td>
</tr>
</tbody>
</table>



 

El nivel de la interfaz de usuario interna se puede establecer mediante [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). El instalador establece la propiedad [**elemento uilevel**](uilevel.md) en el nivel actual de la interfaz de usuario.

Si se establece la propiedad [**LIMITUI**](limitui.md) , el nivel de la interfaz de usuario (UI) que se usa al instalar el paquete está restringido a básico.

Para obtener un ejemplo de creación de la interfaz de usuario, vea [un ejemplo de instalación](an-installation-example.md).

 

 




