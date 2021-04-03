---
description: Las tablas de mensajes son recursos de cadena especiales que se usan al mostrar mensajes de error. Se declaran en un archivo de recursos mediante la instrucción de definición de recursos MESSAGETABLE. Para tener acceso a las cadenas de mensaje, use la función FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Tablas de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998115"
---
# <a name="message-tables"></a>Tablas de mensajes

Las tablas de mensajes son recursos de cadena especiales que se usan al mostrar mensajes de error. Se declaran en un archivo de recursos mediante la instrucción de definición de recursos [MESSAGETABLE](../menurc/messagetable-resource.md) . Para tener acceso a las cadenas de mensaje, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .

El sistema proporciona una tabla de mensajes para los [códigos de error del sistema](system-error-codes.md). Para recuperar la cadena que corresponde al código de error, llame a [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con el \_ mensaje Format de la \_ \_ marca System.

Para proporcionar una tabla de mensajes para la aplicación, siga las instrucciones de [archivos de texto del mensaje](../eventlog/message-text-files.md). Para recuperar cadenas de la tabla de mensajes, llame a [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con el \_ mensaje Format de la \_ \_ marca HMODULE.

 

 
