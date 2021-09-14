---
description: Windows El instalador proporciona a los desarrolladores de paquetes la capacidad de crear una interfaz de usuario interna que tiene varios niveles de funcionalidad.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Interfaz de usuario niveles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbe932ea10b62d20ca06a027b935ff04289cdef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074283"
---
# <a name="user-interface-levels"></a>Interfaz de usuario niveles

Windows El instalador proporciona a los desarrolladores de paquetes la capacidad de crear una interfaz de usuario interna que tiene varios niveles de funcionalidad. Dado que el autor del paquete debe crear la interfaz de usuario interna, el comportamiento de la interfaz de usuario completa, la interfaz de usuario reducida, la interfaz de usuario básica y los niveles Ninguno depende del paquete de instalación. En la tabla siguiente se describe la funcionalidad que normalmente se atribuyó a los niveles de interfaz de usuario.




| Nivel de interfaz de usuario | Descripción | 
|----------|-------------|
| Interfaz de usuario completa | Muestra los cuadros de diálogo modales y no modales que se han escrito en la interfaz de usuario interna. Muestra cuadros de <a href="error-dialog.md">diálogo de error de</a> creación.<blockquote>[!Note]<br />Los cuadros de diálogo modales requieren la entrada del usuario antes de que la instalación pueda continuar y se especifican estableciendo el Bit de estilo de diálogo <a href="modal-dialog-style-bit.md">modal</a> en la columna Atributos de la <a href="dialog-table.md">tabla dialog.</a> Un cuadro de diálogo no modelo no requiere la entrada del usuario para que la instalación continúe.</blockquote><br /> Normalmente, una interfaz de usuario completa <a href="user-interface-wizard-behavior.md">muestra Interfaz de usuario comportamiento del asistente.</a><br /> | 
| Interfaz de usuario reducida | Muestra los cuadros de diálogo no modelo que se han escrito en la interfaz de usuario. No muestra ningún cuadro de diálogo modal de creación. Muestra cuadros de <a href="error-dialog.md">diálogo de error de</a> creación. Muestra los <a href="authoring-disk-prompt-messages.md">mensajes del símbolo del</a> sistema de disco. Muestra <a href="filesinuse-dialog.md">ArchivosUso cuadros de diálogo.</a> | 
| Interfaz de usuario básica | Muestra los cuadros de diálogo de modeless integrados que muestran los mensajes de progreso. Muestra los cuadros de diálogo de error integrados. No muestra ningún cuadro de diálogo de creación. Solicita a los usuarios que inserten un disco mostrando un cuadro de diálogo que contiene el valor de la propiedad <a href="diskprompt.md"><strong>DiskPrompt.</strong></a> | 
| None | Ninguno significa una instalación silenciosa que no muestra ninguna interfaz de usuario. | 




 

El nivel de la interfaz de usuario interna se puede establecer mediante [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). El instalador establece la [**propiedad UILevel**](uilevel.md) en el nivel actual de la interfaz de usuario.

Si se establece la propiedad [**LIMITUI,**](limitui.md) el nivel de interfaz de usuario (UI) usado al instalar el paquete se restringe a Básico.

Para obtener un ejemplo de creación de la interfaz de usuario, vea [Un ejemplo de instalación](an-installation-example.md).

 

 




