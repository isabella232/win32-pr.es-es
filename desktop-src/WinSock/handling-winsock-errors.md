---
description: Control de errores en Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Control de errores de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbb0ea47fc023ce0d6ae47f82a6bb9d732e052d5749fe58f9a405d6784d941b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097905"
---
# <a name="handling-winsock-errors"></a>Control de errores de Winsock

La mayoría Windows sockets 2 no devuelven la causa específica de un error cuando se devuelve la función. Algunas funciones winsock devuelven un valor de cero si se realiza correctamente. De lo contrario, se devuelve el valor SOCKET ERROR (-1) y se puede recuperar un número de error específico llamando \_ a la [**función WSAGetLastError.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) Para las funciones winsock que devuelven un identificador, un valor devuelto de SOCKET NO VÁLIDO (0xffff) indica un error y se puede recuperar un número de error específico llamando a \_ **WSAGetLastError**. Para las funciones winsock que devuelven un puntero, un valor devuelto de **NULL** indica un error y se puede recuperar un número de error específico llamando a la función **WSAGetLastError.**

Un código de error de Winsock se puede convertir en HRESULT para su uso en una llamada a procedimiento remoto (RPC) mediante HRESULT \_ FROM \_ WIN32. En versiones anteriores del Kit de desarrollo de software de plataforma (SDK), HRESULT FROM WIN32 se definió como una macro en el archivo de encabezado \_ \_ *Winerror.h.* En el Kit de desarrollo de software (SDK) de Microsoft Windows, HRESULT FROM WIN32 se define como una función insertda en el archivo de encabezado \_ \_ *Winerror.h.*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Códigos de error de sockets](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



