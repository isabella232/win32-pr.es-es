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
# <a name="message-tables"></a><span data-ttu-id="47ac9-105">Tablas de mensajes</span><span class="sxs-lookup"><span data-stu-id="47ac9-105">Message Tables</span></span>

<span data-ttu-id="47ac9-106">Las tablas de mensajes son recursos de cadena especiales que se usan al mostrar mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="47ac9-106">Message tables are special string resources used when displaying error messages.</span></span> <span data-ttu-id="47ac9-107">Se declaran en un archivo de recursos mediante la instrucción de definición de recursos [MESSAGETABLE](../menurc/messagetable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="47ac9-107">They are declared in a resource file using the [MESSAGETABLE](../menurc/messagetable-resource.md) resource-definition statement.</span></span> <span data-ttu-id="47ac9-108">Para tener acceso a las cadenas de mensaje, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="47ac9-108">To access the message strings, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function.</span></span>

<span data-ttu-id="47ac9-109">El sistema proporciona una tabla de mensajes para los [códigos de error del sistema](system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="47ac9-109">The system provides a message table for the [system error codes](system-error-codes.md).</span></span> <span data-ttu-id="47ac9-110">Para recuperar la cadena que corresponde al código de error, llame a [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con el \_ mensaje Format de la \_ \_ marca System.</span><span class="sxs-lookup"><span data-stu-id="47ac9-110">To retrieve the string that corresponds to the error code, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag.</span></span>

<span data-ttu-id="47ac9-111">Para proporcionar una tabla de mensajes para la aplicación, siga las instrucciones de [archivos de texto del mensaje](../eventlog/message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="47ac9-111">To provide a message table for your application, follow the instructions in [Message Text Files](../eventlog/message-text-files.md).</span></span> <span data-ttu-id="47ac9-112">Para recuperar cadenas de la tabla de mensajes, llame a [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con el \_ mensaje Format de la \_ \_ marca HMODULE.</span><span class="sxs-lookup"><span data-stu-id="47ac9-112">To retrieve strings from your message table, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_HMODULE flag.</span></span>

 

 
