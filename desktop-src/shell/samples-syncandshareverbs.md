---
description: Muestra cómo registrar un verbo que extiende el &\# 0034; Sincronización&\# 0034; y &\# 0034; Comparta&\# 0034; verbos en la barra de comandos Windows Explorer.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256886"
---
# <a name="sync-and-share-verbs"></a>Verbos Sincronizar y Compartir

Muestra cómo registrar un verbo que extiende los verbos "Sync" y "Share" en la barra de comandos Windows Explorer.

En este tema se incluyen las siguientes secciones.

-   [Requisitos](#requirements)
-   [Descargar el ejemplo](#downloading-the-sample)
-   [Ejecución del ejemplo](#running-the-sample)
-   [Quitar el ejemplo](#removing-the-sample)

## <a name="requirements"></a>Requisitos



| Producto                                | Versión mínima del producto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Kit de desarrollo de software de Windows (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Descargar el ejemplo

| Location      | Dirección URL de ruta de acceso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Ejemplo SyncAndShareVerbs](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a>Ejecutar el ejemplo

Para ejecutar el ejemplo (sincronización):

1.  Vaya al directorio que contiene el `sync.reg` archivo.
2.  Escriba `sync.reg ` en la línea de comandos o haga doble clic en el icono para `sync.reg` registrarlo.
3.  Abra el explorador Windows y seleccione un archivo.
4.  Haga clic **en la opción** Sincronizar en la barra de comandos y seleccione una subopción como **Paint**.

Para ejecutar el ejemplo (recurso compartido):

1.  Vaya al directorio que contiene el `share.reg` archivo.
2.  Escriba `share.reg` en la línea de comandos o haga doble clic en el icono para `share.reg` registrarlo.
3.  Abra Windows Explorer y seleccione un archivo. Haga clic en **la opción** Compartir en la barra de comandos.
4.  Haga clic **en la opción Compartir** con en la barra de comandos y seleccione una subopción como **Paint**.

## <a name="removing-the-sample"></a>Quitar el ejemplo

Para quitar el ejemplo (sincronización):

1.  Vaya al directorio que contiene el archivo Uninstallsync.reg.
2.  Escriba `uninstallsync.reg` en la línea de comandos o haga doble clic en el icono de `uninstallsync.reg` .

Para quitar el ejemplo (recurso compartido):

1.  Vaya al directorio que contiene el archivo Uninstallshare.reg.
2.  Escriba `uninstallshare.reg` en la línea de comandos o haga doble clic en el icono de `uninstallshare.reg.`

 

 



