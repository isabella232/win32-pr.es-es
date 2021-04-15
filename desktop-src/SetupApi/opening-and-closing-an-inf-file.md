---
description: Antes de que las funciones de configuración puedan tener acceso a la información del archivo INF, debe abrirlo con una llamada a la función SetupOpenInfFile. Esta función devuelve un identificador al archivo INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Abrir y cerrar un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545790"
---
# <a name="opening-and-closing-an-inf-file"></a>Abrir y cerrar un archivo INF

Antes de que las funciones de configuración puedan tener acceso a la información del archivo INF, debe abrirlo con una llamada a la función [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) . Esta función devuelve un identificador al archivo INF.

Si no conoce el nombre del archivo INF que necesita abrir, puede usar la función [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) para obtener una lista de archivos INF en un directorio.

Después de abrir un archivo INF, puede anexar más archivos INF al archivo INF abierto mediante la función [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) . Es funcionalmente similar a una instrucción include. Cuando las siguientes funciones de instalación hagan referencia a un archivo INF abierto, también podrán tener acceso a cualquier información almacenada en los archivos anexados.

Si no especifica un archivo INF durante la llamada a la función [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , **SetupOpenAppendInfFile** anexa los archivos especificados por la clave **LayoutFile** en la sección **versión** del archivo INF abierto.

Cuando ya no necesite la información del archivo INF, llame a la función [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) para liberar los recursos asignados durante la llamada a [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).

 

 



