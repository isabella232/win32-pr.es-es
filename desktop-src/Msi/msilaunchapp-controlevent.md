---
description: Este evento de control ejecuta un archivo especificado. Si el archivo no existe, o si se produce un error en el evento, Windows Installer registra el error en el registro detallado sin mostrar un cuadro de diálogo que contiene un mensaje de error.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652527"
---
# <a name="msilaunchapp-controlevent"></a>MsiLaunchApp ControlEvent,

Este evento de control ejecuta un archivo especificado. Si el archivo no existe, o si se produce un error en el evento, Windows Installer registra el error en el registro detallado sin mostrar un cuadro de diálogo que contiene un mensaje de error.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible. Este ControlEvent, está disponible a partir de Windows Installer 5,0.

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Los campos del valor del argumento están delimitados por espacios. El primer campo contiene un valor de cadena que especifica el archivo que se va a ejecutar. Use un valor de cadena de \[ \# *filekey* \] para identificar el archivo y reemplace *filekey* por el identificador del archivo que aparece en la columna archivo de la tabla [archivo](file-table.md) . Los campos restantes del argumento pueden contener parámetros utilizados por el archivo que se está ejecutando.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Para permitir que un usuario elija ejecutar un archivo al final de una instalación. Este evento puede estar condicionado en una propiedad establecida por un control [CheckBox](checkbox-control.md) mostrado en el cuadro de diálogo final de la instalación. El control CheckBox no debe mostrarse durante la eliminación del paquete.

 

 



