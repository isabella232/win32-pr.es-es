---
description: Lo llama el compilador para implementar extensiones de control de excepciones estructurado.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: __C_specific_handler función (WDM. h)
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
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660413"
---
# <a name="__c_specific_handler-function"></a>\_\_\_Función de controlador específica de C \_

Lo llama el compilador para implementar extensiones de control de excepciones estructurado.

La dirección relativa del controlador específico del lenguaje está presente en la información de desenredo \_ cada vez que se establecen marcas UNW Flag \_ \_ EHANDLER o UNW \_ Flag \_ UHANDLER. Se llama al controlador específico del lenguaje como parte de la búsqueda de un controlador de excepciones o como parte de un desenredado. Para obtener más información, consulte [controlador específico del lenguaje](/cpp/build/language-specific-handler).

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

*ExceptionRecord* \[ de\]
</dt> <dd>

Proporciona un puntero a un registro de excepción, que tiene la definición estándar de Win64.

</dd> <dt>

*EstablisherFrame* \[ de\]
</dt> <dd>

Dirección de la base de la asignación de pila fija para esta función.

</dd> <dt>

*ContextRecord* \[ in, out\]
</dt> <dd>

Apunta al contexto de la excepción en el momento en que se produjo la excepción (en el caso del controlador de excepciones) o en el contexto de "desenredo" actual (en el caso del controlador de terminación).

</dd> <dt>

*DispatcherContext* \[ in, out\]
</dt> <dd>

Apunta al contexto del distribuidor para esta función.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>WDM. h</dt> </dl>        |
| Biblioteca<br/> | <dl> <dt>NtosKrnl. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Ntoskrnl.exe</dt> </dl> |



 

