---
description: Recupera una descripción independiente del equipo de una excepción e información sobre el estado del equipo que existe para el subproceso cuando se produce la excepción. Solo se puede llamar a esta función desde la expresión de filtro de un controlador de excepciones.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: Macro GetExceptionInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 425cfbe10ac2ee66f10e016489ff070b67b6fc243a472f95b4f5809724998a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279225"
---
# <a name="getexceptioninformation-macro"></a>Macro GetExceptionInformation

Recupera una descripción independiente del equipo de una excepción e información sobre el estado del equipo que existe para el subproceso cuando se produce la excepción. Solo se puede llamar a esta función desde la expresión de filtro de un controlador de excepciones.

> [!Note]  
> El compilador de optimización de Microsoft C/C++ interpreta esta función como una palabra clave y su uso fuera de la sintaxis adecuada de control de excepciones genera un error del compilador.

 

## <a name="syntax"></a>Sintaxis


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a>Parámetros

Esta macro no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Puntero a una [**estructura EXCEPTION \_ POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) que contiene punteros a las dos estructuras siguientes:

-   [**EXCEPTION \_ Estructura**](/windows/desktop/api/WinNT/ns-winnt-exception_record) RECORD que contiene una descripción de la excepción.
-   [**Estructura CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) que contiene la información de estado del equipo.

## <a name="remarks"></a>Comentarios

La expresión de filtro (desde la que se llama a la función) se evalúa si se produce una excepción durante la ejecución del bloque **\_ \_ try** y determina si se ejecuta o no el bloque **\_ \_ except.**

La expresión de filtro puede invocar una función de filtro. La función de filtro no puede llamar **a GetExceptionInformation.** Sin embargo, el valor devuelto **de GetExceptionInformation** se puede pasar como parámetro a una función de filtro.

Para pasar la información [**de EXCEPTION \_ POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) al bloque de controlador de excepciones, la expresión de filtro o la función de filtro deben copiar el puntero o los datos en un almacenamiento seguro al que el controlador pueda acceder más adelante.

En el caso de los controladores anidados, cada expresión de filtro se evalúa hasta que una se evalúa como **EXCEPTION \_ EXECUTE \_ HANDLER** o **EXCEPTION CONTINUE \_ \_ EXECUTION**. Cada expresión de filtro puede invocar **GetExceptionInformation para** obtener información de excepción.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[**PUNTEROS \_ DE EXCEPCIÓN**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[**REGISTRO DE \_ EXCEPCIÓN**](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[**GetExceptionCode**](getexceptioncode.md)
</dt> <dt>

[**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[Funciones de control de excepciones estructurado](structured-exception-handling-functions.md)
</dt> <dt>

[Información general sobre el control de excepciones estructurado](structured-exception-handling.md)
</dt> <dt>

[Habilitar Windows compatibilidad con Intel AVX](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
