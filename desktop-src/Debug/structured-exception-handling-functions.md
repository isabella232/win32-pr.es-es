---
description: Las funciones siguientes se usan en el control estructurado de excepciones.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Funciones estructuradas de control de excepciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164629"
---
# <a name="structured-exception-handling-functions"></a>Funciones estructuradas de control de excepciones

Las funciones siguientes se usan en el control estructurado de excepciones.

-   [**AbnormalTermination**](abnormaltermination.md)

    Indica si el bloque **\_ \_ try** de un controlador de terminación finalizó con normalidad.

-   [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    Registra un controlador de continuación vectorado.

-   [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    Registra un controlador de excepciones vectorial.

-   [**GetExceptionCode**](getexceptioncode.md)

    Recupera un código que identifica el tipo de excepción que se produjo.

-   [**GetExceptionInformation**](getexceptioninformation.md)

    Recupera una descripción independiente del equipo de una excepción e información sobre el estado de la máquina que existía para el subproceso cuando se produjo la excepción.

-   [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    Genera una excepción en el subproceso que realiza la llamada.

-   [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    Anula el registro de un controlador de continuación vectorado.

-   [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    Anula el registro de un controlador de excepciones vectorial.

-   [**RtlAddGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    Informa al sistema de una tabla de funciones dinámicas que representa una región de memoria que contiene código.

-   [**RtlDeleteGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    Informa al sistema de que una tabla de funciones dinámicas notificada previamente ya no está en uso.

-   [**RtlGrowFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    Informa de que una tabla de funciones dinámicas ha aumentado de tamaño.

-   [**SetUnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    Permite que una aplicación sustituya al controlador de excepciones de nivel superior de cada subproceso y proceso.

-   [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    Pasa excepciones no controladas al depurador, si el proceso se está depurando.

-   [**VectoredHandler**](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    Función definida por la aplicación que actúa como controlador de excepciones vectorial.

Las funciones siguientes solo se usan en las funciones de 64 Windows.

-   [**RtlAddFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    Agrega una tabla de funciones dinámicas a la lista de tablas de funciones dinámicas.

-   [**RtlCaptureContext**](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    Recupera un registro de contexto en el contexto del autor de la llamada.

-   [**RtlDeleteFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    Quita una tabla de funciones dinámicas de la lista de tablas de funciones dinámicas.

-   [**RtlInstallFunctionTableCallback**](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    Agrega una tabla de funciones dinámicas a la lista de tablas de funciones dinámicas.

-   [**RtlRestoreContext**](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    Restaura el contexto del autor de la llamada al registro de contexto especificado.

 

 
