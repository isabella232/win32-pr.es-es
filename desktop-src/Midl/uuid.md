---
title: uuid (atributo)
description: El atributo de interfaz \ uuid\ designa un identificador único universal (UUID) que se asigna a la interfaz y que lo distingue de otras interfaces.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- atributo uuid MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159327"
---
# <a name="uuid-attribute"></a>uuid (atributo)

El atributo de interfaz **\[ uuid \]** designa un identificador único universal (UUID) que se asigna a la interfaz y que lo distingue de otras interfaces.

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*string-uuid* 
</dt> <dd>

Especifica una cadena formada por 8 dígitos hexadecimales seguidos de un guion, tres grupos de 4 dígitos hexadecimales cada uno seguidos de un guion y, a continuación, 12 dígitos hexadecimales. Puede incluir la cadena UUID entre comillas, excepto cuando se usa el modificador del compilador MIDL [**/osf**](-osf.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La biblioteca en tiempo de ejecución usa el UUID de interfaz que el atributo **\[ uuid \]** designa para ayudar a establecer la comunicación entre las aplicaciones cliente y servidor. El **\[ atributo \] uuid** puede aparecer en la lista de atributos de interfaz para una interfaz RPC o una interfaz COM.

Para una interfaz RPC, la lista de atributos de interfaz debe incluir el atributo **\[ \] uuid** o el atributo local, y el que elija debe **\[** [](local.md) **\]** producirse exactamente una vez. Si la lista incluye el **\[ atributo uuid, \]** también puede incluir el atributo **\[** [**de**](version.md) **\]** versión.

Para una interfaz COM (identificada por el atributo de interfaz de objeto), la lista de atributos de interfaz debe incluir el atributo **\[** [](object.md) **\]** **\[ uuid, \]** **\[ \]** pero no puede incluir el atributo de versión. La lista de una interfaz COM puede incluir el **\[ atributo \] local** aunque el atributo **\[ uuid \]** esté presente.

Microsoft RPC admite una extensión para DCE IDL que permite incluir el UUID entre comillas dobles ("" ""). El formato entre comillas es necesario para los preprocesadores del compilador de C que interpretan los números UUID como números de punto flotante.

Todos los valores UUID deben generarse en el equipo para garantizar la unidad. Use la utilidad Uuidgen para generar valores UUID únicos.

El UUID y los números de versión de la interfaz se usan para determinar si el cliente puede enlazarse al servidor. Para que el cliente se enlace al servidor, el UUID especificado en las interfaces de cliente y servidor debe ser el mismo.

Tenga en cuenta que una interfaz sin atributos se puede importar en un archivo IDL base. Sin embargo, la interfaz solo debe contener tipos de datos sin procedimientos. Si incluso hay un procedimiento contenido en la interfaz, se debe especificar un atributo uuid o local.

## <a name="examples"></a>Ejemplos

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**object**](object.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 




