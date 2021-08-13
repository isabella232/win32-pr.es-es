---
description: Este evento de control ejecuta un archivo especificado. Si el archivo no existe, o si se produce un error en el evento, Windows Installer registra el error en el registro detallado sin mostrar un cuadro de diálogo que contenga un mensaje de error.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982152d58748ba8b1b8f9d302766e1e9c55eb2ee3c9fa0ce7582507c017dc9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627802"
---
# <a name="msilaunchapp-controlevent"></a>MsiLaunchApp ControlEvent

Este evento de control ejecuta un archivo especificado. Si el archivo no existe, o si se produce un error en el evento, Windows Installer registra el error en el registro detallado sin mostrar un cuadro de diálogo que contenga un mensaje de error.

**[Windows Instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** No se admite. Este ControlEvent está disponible a partir de Windows Installer 5.0.

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Los campos del valor del argumento se delimitan por espacios. El primer campo contiene un valor de cadena que especifica el archivo que se va a ejecutar. Use un valor de cadena de filekey para identificar el archivo y reemplace filekey por el identificador del archivo que aparece en la columna Archivo \[ \#  \] de la [tabla](file-table.md) File.  Los campos restantes del argumento pueden contener parámetros usados por el archivo que se ejecuta.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Para permitir que un usuario elija ejecutar un archivo al final de una instalación. Este evento se puede condición en una propiedad establecida por un control [CheckBox](checkbox-control.md) que se muestra en el cuadro de diálogo final de la instalación. El control CheckBox no debe mostrarse durante la eliminación del paquete.

 

 



