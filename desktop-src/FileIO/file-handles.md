---
description: Cuando un proceso abre un archivo mediante la función CreateFile, se asocia un identificador de archivo a él hasta que el proceso finaliza o el identificador se cierra mediante la función CloseHandle.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Identificadores de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa39768d8467c162fdb0bebae874255c76e20e95750506ba81f32e538e26bc7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927825"
---
# <a name="file-handles"></a>Identificadores de archivo

Cuando un proceso abre un archivo mediante la  función [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) se asocia un identificador de archivo a él hasta que el proceso finaliza o el identificador se cierra mediante la [**función CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) El identificador de archivo se usa para identificar el archivo en muchas llamadas de función.

Cada identificador de archivo y objeto de archivo suele ser único para cada proceso que abre un archivo; las únicas excepciones a esto son cuando se duplica un identificador de archivo mantenido por un proceso o cuando un proceso secundario hereda los identificadores de archivo del proceso primario. En estas situaciones, estos identificadores de archivo son únicos, pero ven un único objeto de archivo compartido. Consulte [**DuplicateHandle para**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) obtener más información sobre la duplicación de identificadores de archivos que mantienen los procesos.

Tenga en cuenta que aunque los identificadores de archivo suelen ser privados para un proceso, los datos de archivo a los que apuntan los identificadores de archivo no lo son. Por lo tanto, los procesos y subprocesos que comparten el mismo archivo deben sincronizar su acceso. Para la mayoría de las operaciones en un archivo, un proceso identifica el archivo a través de su grupo privado de identificadores.

 

 
