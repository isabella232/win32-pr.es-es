---
title: palabra clave declare_guid
description: La \_ palabra clave declare GUID indica a MIDL que emita una variable GUID en el archivo de encabezado generado.
keywords:
- palabra clave declare_guid MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105721321"
---
# <a name="declare_guid-keyword"></a>declare la \_ palabra clave GUID

La palabra clave **declare \_ GUID** indica a MIDL que emita una variable GUID en el archivo de encabezado generado.

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre-variable* 
</dt> <dd>

Especifica un nombre de variable para el identificador en el archivo de encabezado generado.

</dd> <dt>

*guid*
</dt> <dd>

Especifica el [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) que se aplicará al nombre de variable en el archivo de encabezado generado.

</dd> </dl>

## <a name="examples"></a>Ejemplos

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a>Observaciones

`declare_guid`El uso de es equivalente al uso de `cpp_quote` para generar una invocación de la `EXTERN_GUID` macro.

En el ejemplo anterior se obtiene el siguiente resultado:

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

La `declare_guid` instrucción se proporciona por comodidad. Tiene la ventaja de usar la misma sintaxis GUID que el [ `uuid` atributo](uuid.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**cpp_quote**](cpp-quote.md)
</dt> <dt>

[**uuid (atributo)**](uuid.md)
</dt> <dt>

[**Estructura GUID**](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
