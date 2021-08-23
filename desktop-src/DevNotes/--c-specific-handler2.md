---
description: Llamado por el compilador para implementar extensiones estructuradas de control de excepciones.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: __C_specific_handler función (Wdm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: c61d14b591f54ea44ba0f33a36a2ca5acecb129ba46b5f45fcc18185f5d9448c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017833"
---
# <a name="__c_specific_handler-function"></a>\_\_Función \_ de controlador específica de C \_

Llamado por el compilador para implementar extensiones estructuradas de control de excepciones.

La dirección relativa del controlador específico del lenguaje está presente en LA INFORMACIÓN DE DESENREDO cada vez que se establecen las marcas \_ UNW FLAG EHANDLER o \_ \_ UNW \_ FLAG \_ UHANDLER. Se llama al controlador específico del lenguaje como parte de la búsqueda de un controlador de excepciones o como parte de un desenredo. Para obtener más información, vea [Language Specific Handler](/cpp/build/language-specific-handler).

## <a name="syntax"></a>Sintaxis


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ExceptionRecord* \[ En\]
</dt> <dd>

Proporciona un puntero a un registro de excepción, que tiene la definición estándar de Win64.

</dd> <dt>

*EstablisherFrame* \[ En\]
</dt> <dd>

Dirección de la base de la asignación de pila fija para esta función.

</dd> <dt>

*ContextRecord* \[ in, out\]
</dt> <dd>

Apunta al contexto de excepción en el momento en que se produjo la excepción (en el caso del controlador de excepciones) o al contexto actual de "desenredo" (en el caso del controlador de terminación).

</dd> <dt>

*DispatcherContext* \[ in, out\]
</dt> <dd>

Apunta al contexto del distribuidor para esta función.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wdm.h</dt> </dl>        |
| Biblioteca<br/> | <dl> <dt>NtosKrnl.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Ntoskrnl.exe</dt> </dl> |



 

