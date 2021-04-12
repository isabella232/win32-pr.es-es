---
title: Cambiar el nombre del archivo de recursos compilados
description: De forma predeterminada, al compilar recursos, RC nombra el archivo de recursos compilado (. res) con el nombre base del archivo. RC y lo coloca en el mismo directorio que el archivo. rc.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268330"
---
# <a name="renaming-the-compiled-resource-file"></a>Cambiar el nombre del archivo de recursos compilados

De forma predeterminada, al compilar recursos, RC nombra el archivo de recursos compilado (. res) con el nombre base del archivo. RC y lo coloca en el mismo directorio que el archivo. rc. A continuación, se debe invocar CVTRES para convertir el archivo. res a un formato de recursos binario (. RBJ) que el enlazador puede entender. En el ejemplo siguiente se compila MyApp. RC y se crea un archivo de recursos compilado denominado MyApp. res en el mismo directorio que MyApp. RC:

**RC MyApp. RC**

La opción **/FO** proporciona a el archivo. res resultante un nombre que difiere del nombre del archivo. RC correspondiente. Por ejemplo, para asignar un nombre al archivo. res resultante NewFile. res, use el siguiente comando:

**RC-FO NewFile. res MyApp. RC**

La opción **/FO** también puede colocar el archivo. res en un directorio diferente. Por ejemplo, el comando siguiente coloca el archivo de recursos compilado MyApp. res en el directorio C: \\ source \\ Resource:

**RC-FO c: \\ recurso de origen \\ \\ MyApp. res MyApp. RC**

 

 




