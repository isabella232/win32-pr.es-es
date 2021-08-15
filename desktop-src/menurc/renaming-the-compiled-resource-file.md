---
title: Cambiar el nombre del archivo de recursos compilado
description: De forma predeterminada, al compilar recursos, RC asigna un nombre al archivo de recursos compilados (.res) con el nombre base del archivo .rc y lo coloca en el mismo directorio que el archivo .rc.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60f2a920eeed6c1b96b512511b965b0243b89e4f6888120c6183b7a3104963c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733522"
---
# <a name="renaming-the-compiled-resource-file"></a>Cambiar el nombre del archivo de recursos compilado

De forma predeterminada, al compilar recursos, RC asigna un nombre al archivo de recursos compilados (.res) con el nombre base del archivo .rc y lo coloca en el mismo directorio que el archivo .rc. A continuación, se debe invocar CVTRES para convertir el archivo .res en un formato de recurso binario (.rbj) que el vinculador pueda entender. En el ejemplo siguiente se compila MyApp.rc y se crea un archivo de recursos compilado denominado MyApp.res en el mismo directorio que MyApp.rc:

**rc myapp.rc**

La **opción /fo** proporciona al archivo .res resultante un nombre que difiere del nombre del archivo .rc correspondiente. Por ejemplo, para dar nombre al archivo .res resultante NewFile.res, use el siguiente comando:

**rc -fo newfile.res myapp.rc**

La **opción /fo** también puede colocar el archivo .res en un directorio diferente. Por ejemplo, el comando siguiente coloca el archivo de recursos compilado MyApp.res en el directorio C: \\ Recurso de \\ origen:

**rc -fo c: \\ recurso \\ de origen \\ myapp.res myapp.rc**

 

 




