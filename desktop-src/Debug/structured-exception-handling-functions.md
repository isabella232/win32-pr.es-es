---
description: Las siguientes funciones se usan en el control de excepciones estructurado.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Funciones de control de excepciones estructurado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659455"
---
# <a name="structured-exception-handling-functions"></a>Funciones de control de excepciones estructurado

Las siguientes funciones se usan en el control de excepciones estructurado.

-   [**AbnormalTermination**](abnormaltermination.md)

    Indica si el bloque **\_ \_ try** de un controlador de terminación terminó normalmente.

-   [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    Registra un controlador de continuación de vectores.

-   [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    Registra un controlador de excepciones vectorizado.

-   [**GetExceptionCode**](getexceptioncode.md)

    Recupera un código que identifica el tipo de excepción que se ha producido.

-   [**GetExceptionInformation**](getexceptioninformation.md)

    Recupera una descripción independiente de la máquina de una excepción e información sobre el estado del equipo que existía para el subproceso cuando se produjo la excepción.

-   [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    Genera una excepción en el subproceso que realiza la llamada.

-   [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    Anula el registro de un controlador de continuación vectorizado.

-   [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    Anula el registro de un controlador de excepciones vectorizado.

-   [**RtlAddGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    Informa al sistema de una tabla de funciones dinámicas que representa una región de memoria que contiene código.

-   [**RtlDeleteGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    Informa al sistema de que una tabla de funciones dinámicas notificada previamente ya no está en uso.

-   [**RtlGrowFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    Informa de que una tabla de funciones dinámicas ha aumentado de tamaño.

-   [**SetUnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    Permite a una aplicación sustituir el controlador de excepciones de nivel superior de cada subproceso y proceso.

-   [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    Pasa las excepciones no controladas al depurador, si se está depurando el proceso.

-   [**VectoredHandler**](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    Función definida por la aplicación que actúa como controlador de excepciones vectorizadas.

Las siguientes funciones solo se usan en Windows de 64 bits.

-   [**RtlAddFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    Agrega una tabla de funciones dinámicas a la lista de tablas de funciones dinámicas.

-   [**RtlCaptureContext**](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    Recupera un registro de contexto en el contexto del llamador.

-   [**RtlDeleteFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    Quita una tabla de funciones dinámicas de la lista de tablas de funciones dinámicas.

-   [**RtlInstallFunctionTableCallback**](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    Agrega una tabla de funciones dinámicas a la lista de tablas de funciones dinámicas.

-   [**RtlRestoreContext**](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    Restaura el contexto del llamador en el registro de contexto especificado.

 

 
