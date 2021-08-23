---
description: Para que las funciones de instalación puedan acceder a la información del INF, debe abrirla con una llamada a la función SetupOpenInfFile. Esta función devuelve un identificador al archivo INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Apertura y cierre de un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05500b473a904a3834fa507cff0d22c466153f4e08d95f75d0c076c66d86675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665555"
---
# <a name="opening-and-closing-an-inf-file"></a>Apertura y cierre de un archivo INF

Para que las funciones de instalación puedan acceder a la información del INF, debe abrirla con una llamada a la [**función SetupOpenInfFile.**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) Esta función devuelve un identificador al archivo INF.

Si no conoce el nombre del archivo INF que necesita abrir, puede usar la función [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) para obtener una lista de archivos INF en un directorio.

Después de abrir un archivo INF, puede anexar archivos INF adicionales al archivo INF abierto mediante la función [**SetupOpenAppendInfFile.**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) Esto es funcionalmente similar a una instrucción include. Cuando las funciones de instalación posteriores hacen referencia a un archivo INF abierto, también podrán acceder a cualquier información almacenada en los archivos anexados.

Si no especifica un archivo INF durante la llamada a la función  [**SetupOpenAppendInfFile,**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) **SetupOpenAppendInfFile** anexa los archivos especificados por la clave **LayoutFile** en la sección Versión del archivo INF abierto.

Cuando ya no necesite la información en el archivo INF, llame a la función [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) para liberar los recursos asignados durante la llamada a [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).

 

 



