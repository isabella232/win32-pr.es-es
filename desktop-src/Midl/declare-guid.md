---
title: palabra clave declare_guid
description: La palabra \_ clave declare guid indica a MIDL que emita una variable GUID en el archivo de encabezado generado.
keywords:
- declare_guid clave MIDL
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a6854836ef0c45d1892bda9edb250a8c8cfa7d69862ac3424e2a2e96a43991d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991512"
---
# <a name="declare_guid-keyword"></a>palabra \_ clave declare guid

La **palabra clave declare \_ guid** indica a MIDL que emita una variable GUID en el archivo de encabezado generado.

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*variable-name* 
</dt> <dd>

Especifica un nombre de variable para el identificador en el archivo de encabezado generado.

</dd> <dt>

*guid*
</dt> <dd>

Especifica el [GUID que](/windows/win32/api/guiddef/ns-guiddef-guid) se aplicará al nombre de variable en el archivo de encabezado generado.

</dd> </dl>

## <a name="examples"></a>Ejemplos

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a>Comentarios

El `declare_guid` uso de es equivalente a usar para generar una `cpp_quote` invocación de la `EXTERN_GUID` macro.

El ejemplo anterior da como resultado la siguiente salida:

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
