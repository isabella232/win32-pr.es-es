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
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164642"
---
# <a name="getexceptioninformation-macro"></a>Macro GetExceptionInformation

Recupera una descripción independiente del equipo de una excepción e información sobre el estado del equipo que existe para el subproceso cuando se produce la excepción. Solo se puede llamar a esta función desde la expresión de filtro de un controlador de excepciones.

> [!Note]  
> El compilador de optimización de Microsoft C/C++ interpreta esta función como una palabra clave y su uso fuera de la sintaxis de control de excepciones adecuada genera un error del compilador.

 

## <a name="syntax"></a>Sintaxis


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a>Parámetros

Esta macro no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Puntero a una [**estructura EXCEPTION \_ POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) que contiene punteros a las dos estructuras siguientes:

-   [**EXCEPCIÓN \_ Estructura RECORD**](/windows/desktop/api/WinNT/ns-winnt-exception_record) que contiene una descripción de la excepción.
-   [**Estructura CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) que contiene la información de estado del equipo.

## <a name="remarks"></a>Observaciones

La expresión de filtro (desde la que se llama a la función) se evalúa si se **\_ \_** produce una excepción durante la ejecución del bloque **\_ \_ try** y determina si se ejecuta o no el bloque except.

La expresión de filtro puede invocar una función de filtro. La función filter no puede llamar **a GetExceptionInformation.** Sin embargo, el valor devuelto **de GetExceptionInformation** se puede pasar como parámetro a una función de filtro.

Para pasar la información [**de EXCEPTION \_ POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) al bloque de controlador de excepciones, la expresión de filtro o la función de filtro deben copiar el puntero o los datos en un almacenamiento seguro al que el controlador pueda acceder más adelante.

En el caso de los controladores anidados, cada expresión de filtro se evalúa hasta que se evalúa como **EXCEPTION \_ EXECUTE \_ HANDLER** o **EXCEPTION CONTINUE \_ \_ EXECUTION**. Cada expresión de filtro puede invocar **GetExceptionInformation para** obtener información de excepción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CONTEXTO**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[**PUNTEROS \_ DE EXCEPCIÓN**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[**REGISTRO DE \_ EXCEPCIONES**](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[**GetExceptionCode**](getexceptioncode.md)
</dt> <dt>

[**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[Funciones estructuradas de control de excepciones](structured-exception-handling-functions.md)
</dt> <dt>

[Información general sobre el control estructurado de excepciones](structured-exception-handling.md)
</dt> <dt>

[Habilitación Windows compatibilidad con Intel AVX](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
