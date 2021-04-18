---
description: Control de errores en Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Control de errores de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705614"
---
# <a name="handling-winsock-errors"></a>Control de errores de Winsock

La mayoría de las funciones de Windows Sockets 2 no devuelven la causa específica de un error cuando la función devuelve. Algunas funciones de Winsock devuelven un valor de cero si se realiza correctamente. De lo contrario, \_ se devuelve el valor de socket error (-1) y se puede recuperar un número de error concreto llamando a la función [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . En el caso de las funciones de Winsock que devuelven un identificador, un valor devuelto de Socket no válido \_ (0xFFFF) indica un error y se puede recuperar un número de error concreto llamando a **WSAGetLastError**. En el caso de las funciones de Winsock que devuelven un puntero, un valor devuelto de **null** indica un error y se puede recuperar un número de error concreto llamando a la función **WSAGetLastError** .

Un código de error de Winsock se puede convertir en HRESULT para su uso en una llamada a procedimiento remoto (RPC) mediante HRESULT \_ de \_ Win32. En versiones anteriores del kit de desarrollo de software (SDK) de la plataforma, HRESULT \_ de \_ Win32 se definía como una macro en el archivo de encabezado *Winerror. h* . En el kit de desarrollo de software (SDK) de Microsoft Windows, HRESULT \_ de \_ Win32 se define como una función insertada en el archivo de encabezado *Winerror. h* .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códigos de error de Windows Sockets](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



