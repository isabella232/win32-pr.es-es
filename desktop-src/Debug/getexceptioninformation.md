---
description: Recupera una descripción independiente del equipo de una excepción e información sobre el estado del equipo que existe para el subproceso cuando se produce la excepción. Solo se puede llamar a esta función desde dentro de la expresión de filtro de un controlador de excepciones.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: GetExceptionInformation (macro)
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807819"
---
# <a name="getexceptioninformation-macro"></a>GetExceptionInformation (macro)

Recupera una descripción independiente del equipo de una excepción e información sobre el estado del equipo que existe para el subproceso cuando se produce la excepción. Solo se puede llamar a esta función desde dentro de la expresión de filtro de un controlador de excepciones.

> [!Note]  
> El compilador de optimización de C/C++ de Microsoft interpreta esta función como una palabra clave y su uso fuera de la sintaxis de control de excepciones adecuada genera un error del compilador.

 

## <a name="syntax"></a>Sintaxis


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a>Parámetros

Esta macro no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Un puntero a una estructura de [**\_ punteros de excepción**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) que contiene punteros a las dos estructuras siguientes:

-   [**Excepción \_ de**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Estructura de registro que contiene una descripción de la excepción.
-   Estructura de [**contexto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) que contiene la información de estado del equipo.

## <a name="remarks"></a>Observaciones

La expresión de filtro (desde la que se llama a la función) se evalúa si se produce una excepción durante la ejecución del bloque **\_ \_ try** y determina si se ejecuta el bloque **\_ \_ Except** .

La expresión de filtro puede invocar una función de filtro. La función Filter no puede llamar a **GetExceptionInformation**. Sin embargo, el valor devuelto de **GetExceptionInformation** se puede pasar como un parámetro a una función de filtro.

Para pasar la información de [**\_ punteros de excepción**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) al bloque de controlador de excepciones, la expresión de filtro o la función de filtro deben copiar el puntero o los datos en un almacenamiento seguro al que el controlador puede tener acceso más adelante.

En el caso de los controladores anidados, cada expresión de filtro se evalúa hasta que se evalúa una como **\_ \_ controlador de ejecución de excepción** o continuación de la **\_ \_ ejecución** de la excepción. Cada expresión de filtro puede invocar **GetExceptionInformation** para obtener la información de la excepción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CONTEXTO**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[**\_punteros de excepción**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[**registro de excepción \_**](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[**GetExceptionCode**](getexceptioncode.md)
</dt> <dt>

[**GetXStateFeaturesMask**](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[Funciones de control de excepciones estructurado](structured-exception-handling-functions.md)
</dt> <dt>

[Información general sobre el control estructurado de excepciones](structured-exception-handling.md)
</dt> <dt>

[Habilitar la compatibilidad con Windows para Intel AVX](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
