---
description: Muestra cómo registrar un verbo que extiende el &\# 0034; Sincronizar&\# 0034 y &\# 0034; Compartir&\# 0034; verbos en la barra de comandos del explorador de Windows.
title: Verbos Sincronizar y Compartir
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986035"
---
# <a name="sync-and-share-verbs"></a>Verbos Sincronizar y Compartir

Muestra cómo registrar un verbo que extiende los verbos "sincronizar" y "compartir" en la barra de comandos del explorador de Windows.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Ejecutar el ejemplo](#running-the-sample)
-   [Quitar el ejemplo](#removing-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Ubicación      | URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo de SyncAndShareVerbs](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo (Sync):

1.  Navegue hasta el directorio que contiene el `sync.reg` archivo.
2.  Escriba `sync.reg ` en la línea de comandos o haga doble clic en el icono `sync.reg` registrarlo.
3.  Abra el explorador de Windows y seleccione un archivo.
4.  Haga clic en la opción **sincronizar** en la barra de comandos y seleccione una subopción como **Paint**.

Para ejecutar el ejemplo (recurso compartido):

1.  Navegue hasta el directorio que contiene el `share.reg` archivo.
2.  Escriba `share.reg` en la línea de comandos o haga doble clic en el icono `share.reg` registrarlo.
3.  Abra el explorador de Windows y seleccione un archivo. Haga clic en la opción **compartir** en la barra de comandos.
4.  Haga clic en la opción **compartir con** en la barra de comandos y seleccione una subopción como **Paint**.

## <a name="removing-the-sample"></a>Quitar el ejemplo

Para quitar el ejemplo (Sync):

1.  Navegue hasta el directorio que contiene el archivo Uninstallsync. reg.
2.  Escriba `uninstallsync.reg` en la línea de comandos o haga doble clic en el icono de `uninstallsync.reg` .

Para quitar el ejemplo (recurso compartido):

1.  Navegue hasta el directorio que contiene el archivo Uninstallshare. reg.
2.  Escriba `uninstallshare.reg` en la línea de comandos o haga doble clic en el icono de `uninstallshare.reg.`

 

 



