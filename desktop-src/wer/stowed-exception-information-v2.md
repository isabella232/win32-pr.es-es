---
title: STOWED_EXCEPTION_INFORMATION_V2 estructura
description: Contiene información de excepción stowed.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- STOWED_EXCEPTION_INFORMATION_V2 estructura Informe de errores de Windows
- PSTOWED_EXCEPTION_INFORMATION_V2 puntero de estructura Informe de errores de Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_V2
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefd313f0edcc122708f141cd65418beaade03a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360242"
---
# <a name="stowed_exception_information_v2-structure"></a>Estructura STOWED \_ EXCEPTION \_ INFORMATION \_ V2

Contiene información de excepción stowed.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_V2 {
  STOWED_EXCEPTION_INFORMATION_HEADER Header;
  HRESULT                             ResultCode;
  struct {
    DWORD ExceptionForm  :2;
    DWORD ThreadId  :30;
  };
  union {
    struct {
      PVOID ExceptionAddress;
      ULONG StackTraceWordSize;
      ULONG StackTraceWords;
      PVOID StackTrace;
    };
    struct {
      PWSTR ErrorText;
    };
  };
  ULONG                               NestedExceptionType;
  PVOID                               NestedException;
} STOWED_EXCEPTION_INFORMATION_V2, *PSTOWED_EXCEPTION_INFORMATION_V2;
```



## <a name="members"></a>Members

<dl> <dt>

**Header**
</dt> <dd>

Tipo: **[ **ENCABEZADO DE INFORMACIÓN \_ DE \_ EXCEPCIÓN CON \_ STOWED**](stowed-exception-information-header.md)**

</dd> <dd>

Estructura [**STOWED \_ EXCEPTION INFORMATION \_ \_ HEADER**](stowed-exception-information-header.md) que contiene información para esta estructura primaria.

</dd> <dt>

**ResultCode**
</dt> <dd>

Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Código [**HRESULT**](/windows/desktop/WinProg/windows-data-types) para la excepción stowed.

</dd> <dt>

**ExceptionForm**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor de 2 bits que identifica la forma de la excepción.



| Value                                                                                                                                                                                                                                                                  | Significado                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <dt>**STOWED \_ FORMULARIO \_ DE \_ EXCEPCIÓN BINARY**</dt> <dt>0x01</dt> </dl> | Este valor indica que la forma de la excepción es binaria.<br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <dt>**STOWED \_ TEXTO \_ DEL FORMULARIO \_ DE**</dt> <dt>EXCEPCIÓN 0x02</dt> </dl>       | Este valor indica que la forma de la excepción es texto.<br/>   |



 

</dd> <dt>

**ThreadId**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor de 30 bits que identifica el subproceso que produjo la excepción. El valor se desplaza a la derecha en 2 bits cuando se almacena. Para volver a convertirlo en un identificador de subproceso válido, cambie el valor a la izquierda en 2. Por ejemplo:

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

(*estructura sin nombre*)
</dt> <dd>

Los miembros de esta estructura anidada solo son válidos si el **miembro ExceptionForm** está establecido en **STOWED \_ EXCEPTION FORM \_ \_ BINARY**.

<dl> <dt>

**ExceptionAddress**
</dt> <dd>

Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Puntero que contiene la dirección de excepción.

</dd> <dt>

**StackTraceWordSize**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamaño, en bytes, de cada palabra del seguimiento de la pila al que apunta el miembro **StackTrace.** Este valor se establece en 4 para plataformas de 32 bits y 8 para plataformas de 64 bits.

</dd> <dt>

**StackTraceWords**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de palabras en el seguimiento de la pila al que **apunta el miembro StackTrace.** El número de palabras es igual al número de elementos de la matriz.

</dd> <dt>

**StackTrace**
</dt> <dd>

Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Puntero a un bloque de memoria que contiene el seguimiento de la pila.

</dd> </dl> </dd> <dt>

(*estructura sin nombre*)
</dt> <dd>

El miembro de esta estructura anidada solo es válido si el **miembro ExceptionForm** está establecido en **STOWED \_ EXCEPTION FORM \_ \_ TEXT**.

<dl> <dt>

**ErrorText**
</dt> <dd>

Tipo: **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Puntero a una cadena terminada en NULL que contiene el texto de error de la excepción.

</dd> </dl> </dd> <dt>

**NestedExceptionType**
</dt> <dd>

Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor de 32 bits que especifica el tipo de objeto al que apunta el **miembro NestedException.** Defina el valor con esta macro de definición de tipo de intercambio de bytes que supone little-endian:

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

Estas son algunas definiciones de tipo comunes:



| Value                                                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <dt>**STOWED \_ EXCEPTION \_ NESTED \_ TYPE \_ NONE**</dt> <dt>(0x00000000)</dt> </dl>                                  | Este valor especifica que no hay ningún objeto de excepción anidado.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <dt>**STOWED \_ EXCEPTION \_ NESTED \_ TYPE \_ WIN32**</dt> <dt>STOWED EXCEPTION NESTED \_ \_ \_ TYPE('W32E')</dt> </dl>    | Este valor especifica que el miembro **NestedException** apunta a un [**objeto EXCEPTION \_ RECORD.**](/windows/desktop/api/winnt/ns-winnt-exception_record)<br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <dt>**STOWED \_ EXCEPTION \_ NESTED \_ TYPE \_ STOWED**</dt> <dt>STOWED EXCEPTION NESTED \_ \_ \_ TYPE('STOW')</dt> </dl> | Este valor especifica que el miembro **NestedException** apunta a otro objeto de excepción con stowed. El otro objeto de excepción con stowed puede ser un objeto **STOWED \_ EXCEPTION INFORMATION \_ \_ V2** o una versión diferente con un miembro **Header** válido, es decir, un miembro **Header** que contiene un encabezado [**STOWED EXCEPTION INFORMATION \_ HEADER \_ \_ válido.**](stowed-exception-information-header.md)<br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <dt>**STOWED \_ EXCEPTION \_ NESTED \_ TYPE \_ CLR**</dt> <dt>STOWED EXCEPTION NESTED \_ \_ \_ TYPE('CLR1')</dt> </dl>          | Este valor especifica que el miembro **NestedException** apunta a un objeto de excepción 'CLR1'.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <dt>**STOWED \_ TIPO \_ ANIDADO \_ DE \_ EXCEPCIÓN:**</dt> <dt> \_ EXCEPCIÓN \_ STOWED EXCEPTION NESTED \_ TYPE('ASÍNS1')</dt> </dl>          | Este valor especifica que el miembro **NestedException** apunta a un objeto de excepción de lenguaje.<br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

**NestedException**
</dt> <dd>

Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Puntero a un tipo de excepción anidada. El tipo de objeto se indica mediante el **miembro NestedExceptionType.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

**STOWED \_ EXCEPTION \_ INFORMATION \_ V2** y [**STOWED EXCEPTION INFORMATION \_ \_ \_ HEADER**](stowed-exception-information-header.md) no están definidos actualmente en un encabezado que esté disponible públicamente, por lo que debe definirlos en el código fuente antes de usarlos.

La **estructura STOWED \_ EXCEPTION INFORMATION \_ \_ V1** es idéntica a esta estructura, salvo que no contiene los **miembros NestedExceptionType** y **NestedException.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                         |
| Encabezado<br/>                   | <dl> <dt>Ninguna</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**REGISTRO DE \_ EXCEPCIONES**](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[**ENCABEZADO DE INFORMACIÓN \_ DE EXCEPCIÓN \_ STOWED \_**](stowed-exception-information-header.md)
</dt> </dl>

 

