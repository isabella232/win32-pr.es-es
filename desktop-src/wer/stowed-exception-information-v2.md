---
title: Estructura de STOWED_EXCEPTION_INFORMATION_V2
description: Contiene información de excepción estibada.
ms.assetid: 79267974-EE1B-4427-A6D6-265F6BC5D73A
keywords:
- Estructura de STOWED_EXCEPTION_INFORMATION_V2 Informe de errores de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705181"
---
# <a name="stowed_exception_information_v2-structure"></a>Estructura de la información de excepción de la \_ \_ \_ versión V2

Contiene información de excepción estibada.

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



## <a name="members"></a>Miembros

<dl> <dt>

**Header**
</dt> <dd>

Tipo: **[ **\_ \_ \_ encabezado de información de excepción estibada**](stowed-exception-information-header.md)**

</dd> <dd>

La estructura de [**encabezado de \_ información de excepción \_ \_ estibada**](stowed-exception-information-header.md) que contiene información para esta estructura primaria.

</dd> <dt>

**ResultCode**
</dt> <dd>

Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Código [**HRESULT**](/windows/desktop/WinProg/windows-data-types) para la excepción estibada.

</dd> <dt>

**ExceptionForm**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor de 2 bits que identifica el formato de la excepción.



| Value                                                                                                                                                                                                                                                                  | Significado                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_FORM_BINARY"></span><span id="stowed_exception_form_binary"></span><dl> <dt>**\_ Estibada Formulario de excepción \_ \_ binario**</dt> <dt>0x01</dt> </dl> | Este valor indica que el formato de la excepción es binario.<br/> |
| <span id="STOWED_EXCEPTION_FORM_TEXT"></span><span id="stowed_exception_form_text"></span><dl> <dt>**\_ Estibada \_ \_ Texto del formulario de excepción**</dt> <dt>0x02</dt> </dl>       | Este valor indica que el formato de la excepción es texto.<br/>   |



 

</dd> <dt>

**ThreadId**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Un valor de 30 bits que identifica el subproceso que ha generado la excepción. El valor se desplaza a la derecha 2 bits cuando se almacena. Para volver a convertirlo en un identificador de subproceso válido, desplace el valor a la izquierda en 2. Por ejemplo:

``` syntax
DWORD ActualThreadId = (StowedException.ThreadId << 2);
```

</dd> <dt>

(*struct sin nombre*)
</dt> <dd>

Los miembros de esta estructura anidada solo son válidos si el miembro **ExceptionForm** se establece en un **\_ \_ \_ archivo binario de formulario de excepción estibada**.

<dl> <dt>

**ExceptionAddress**
</dt> <dd>

Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Puntero que contiene la dirección de la excepción.

</dd> <dt>

**StackTraceWordSize**
</dt> <dd>

Tipo: **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamaño, en bytes, de cada palabra del seguimiento de la pila al que apunta el miembro **StackTrace** . Este valor se establece en 4 para las plataformas de 32 bits y 8 para las plataformas de 64 bits.

</dd> <dt>

**StackTraceWords**
</dt> <dd>

Tipo: **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

El número de palabras del seguimiento de la pila al que apunta el miembro **StackTrace** . El número de palabras es igual al número de elementos de la matriz.

</dd> <dt>

**StackTrace**
</dt> <dd>

Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Un puntero a un bloque de memoria que contiene el seguimiento de la pila.

</dd> </dl> </dd> <dt>

(*struct sin nombre*)
</dt> <dd>

El miembro de esta estructura anidada solo es válido si el miembro **ExceptionForm** está establecido en **texto de \_ \_ formulario de \_ excepción estibada**.

<dl> <dt>

**ErrorText**
</dt> <dd>

Tipo: **[ **PWSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Un puntero a una cadena terminada en null que contiene el texto del error de la excepción.

</dd> </dl> </dd> <dt>

**NestedExceptionType**
</dt> <dd>

Tipo: **[ **ULong**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor de 32 bits que especifica el tipo de objeto al que apunta el miembro **NestedException** . Defina el valor con esta macro de definición de tipo de intercambio de bytes que presupone Little-Endian:

``` syntax
#define STOWED_EXCEPTION_NESTED_TYPE(t) ((((((ULONG)(t)) >> 24) & 0xFF) <<  0) | \
                                         (((((ULONG)(t)) >> 16) & 0xFF) <<  8) | \
                                         (((((ULONG)(t)) >>  8) & 0xFF) << 16) | \
                                         (((((ULONG)(t)) >>  0) & 0xFF) << 24))
```

Estas son algunas definiciones de tipos comunes:



| Value                                                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_NESTED_TYPE_NONE"></span><span id="stowed_exception_nested_type_none"></span><dl> <dt>**\_ Estibada \_Tipo anidado de excepción \_ \_ ninguno**</dt> <dt>(0x00000000)</dt> </dl>                                  | Este valor especifica que no hay ningún objeto de excepción anidado.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_WIN32"></span><span id="stowed_exception_nested_type_win32"></span><dl> <dt>**\_ Estibada \_Tipo anidado \_ de \_ excepción**</dt> tipo <dt>anidado de excepción Win32 estibada \_ \_ \_ (' W32E ')</dt> </dl>    | Este valor especifica que el miembro **NestedException** señala a un objeto de [**\_ registro de excepción**](/windows/desktop/api/winnt/ns-winnt-exception_record) .<br/>                                                                                                                                                                                                                                                              |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_STOWED"></span><span id="stowed_exception_nested_type_stowed"></span><dl> <dt>**\_ Estibada tipo \_ \_ \_ anidado**</dt> de excepción de tipo anidado de <dt>excepción estibada \_ \_ \_ (' estiba ')</dt> </dl> | Este valor especifica que el miembro **NestedException** señala a otro objeto de excepción estibada. El otro objeto de excepción estibada puede ser un objeto de **\_ información de excepción de \_ \_ V2** u otra versión con un miembro de **encabezado** válido, es decir, un miembro de **encabezado** que contenga un encabezado de [**\_ información de excepción \_ \_ estibada**](stowed-exception-information-header.md)válido.<br/> |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_CLR"></span><span id="stowed_exception_nested_type_clr"></span><dl> <dt>**\_ Estibada Tipo \_ anidado \_ \_**</dt> de excepción tipo <dt>anidado de excepción CLR estibada \_ \_ \_ (' archivo clr1 ')</dt> </dl>          | Este valor especifica que el miembro **NestedException** señala a un objeto de excepción ' archivo clr1 '.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="STOWED_EXCEPTION_NESTED_TYPE_LEO"></span><span id="stowed_exception_nested_type_leo"></span><dl> <dt>**\_ Estibada Tipo \_ anidado \_ \_**</dt> de excepción <dt> \_ \_ tipo anidado de excepción \_ (' LEO1 ')</dt> </dl>          | Este valor especifica que el miembro **NestedException** señala a un objeto de excepción de idioma.<br/>                                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

**NestedException**
</dt> <dd>

Tipo: **[ **PVOID**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Un puntero a un tipo de excepción anidada. El miembro **NestedExceptionType** indica el tipo de objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**\_ Estibada La \_ información \_ de excepción V2** y el [**\_ encabezado de \_ información \_ de excepción estibada**](stowed-exception-information-header.md) no se definen actualmente en un encabezado que está disponible públicamente, por lo que debe definirlos en el código fuente antes de usarlos.

La estructura V1 de la **\_ información de excepción \_ \_ estibada** es idéntica a esta estructura, salvo que no contiene los miembros **NestedExceptionType** y **NestedException** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                         |
| Encabezado<br/>                   | <dl> <dt>None</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**registro de excepción \_**](/windows/desktop/api/winnt/ns-winnt-exception_record)
</dt> <dt>

[**encabezado de \_ información de excepción estibada \_ \_**](stowed-exception-information-header.md)
</dt> </dl>

 

