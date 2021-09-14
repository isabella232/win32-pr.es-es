---
description: Este evento de control ejecuta un archivo especificado. Si el archivo no existe o si se produce un error en el evento, Windows Installer registra el error en el registro detallado sin mostrar un cuadro de diálogo que contenga un mensaje de error.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071843"
---
# <a name="msilaunchapp-controlevent"></a>MsiLaunchApp ControlEvent

Este evento de control ejecuta un archivo especificado. Si el archivo no existe o si se produce un error en el evento, Windows Installer registra el error en el registro detallado sin mostrar un cuadro de diálogo que contenga un mensaje de error.

**[Windows instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Este ControlEvent está disponible a partir de Windows Installer 5.0.

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Los campos del valor del argumento están delimitados por espacios. El primer campo contiene un valor de cadena que especifica el archivo que se va a ejecutar. Use un valor de cadena de filekey para identificar el archivo y reemplace filekey por el identificador del archivo que aparece en la columna Archivo \[ \#  \] de la [tabla](file-table.md) Archivo.  Los campos restantes del argumento pueden contener parámetros utilizados por el archivo que se ejecuta.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Para permitir que un usuario elija ejecutar un archivo al final de una instalación. Este evento puede estar condicionado por una propiedad establecida por un control [CheckBox](checkbox-control.md) que se muestra en el cuadro de diálogo final de la instalación. El control CheckBox no debe mostrarse durante la eliminación del paquete.

 

 



