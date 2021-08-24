---
description: Las tablas de mensajes son recursos de cadena especiales que se usan al mostrar mensajes de error. Se declaran en un archivo de recursos mediante la instrucción messagetable resource-definition. Para acceder a las cadenas de mensaje, use la función FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Tablas de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6141f78342db2554e85053adda7ee68bdb0e855f213f103da1bb7f62eac1d703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691825"
---
# <a name="message-tables"></a>Tablas de mensajes

Las tablas de mensajes son recursos de cadena especiales que se usan al mostrar mensajes de error. Se declaran en un archivo de recursos mediante la [instrucción messagetable](../menurc/messagetable-resource.md) resource-definition. Para acceder a las cadenas de mensaje, use la [**función FormatMessage.**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)

El sistema proporciona una tabla de mensajes para los códigos [de error del sistema](system-error-codes.md). Para recuperar la cadena que corresponde al código de error, llame a [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM \_ \_ SYSTEM.

Para proporcionar una tabla de mensajes para la aplicación, siga las instrucciones de [Archivos de texto de mensaje](../eventlog/message-text-files.md). Para recuperar cadenas de la tabla de mensajes, llame [**a FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM \_ \_ HMODULE.

 

 
