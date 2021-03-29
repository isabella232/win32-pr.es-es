---
title: uuid (atributo)
description: El atributo \ UUID \ interface designa un identificador único universal (UUID) que se asigna a la interfaz y que lo distingue de otras interfaces.
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- atributo de UUID (MIDL)
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5688bafe8343bdc1ab508a4e65984cc15c88b124
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784072"
---
# <a name="uuid-attribute"></a>uuid (atributo)

El atributo **\[ UUID \]** interface designa un identificador único universal (UUID) que se asigna a la interfaz y que lo distingue de otras interfaces.

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*cadena: UUID* 
</dt> <dd>

Especifica una cadena que consta de 8 dígitos hexadecimales seguidos de un guion y, a continuación, tres grupos de 4 dígitos hexadecimales, seguidos de un guion y 12 dígitos hexadecimales. Puede incluir la cadena UUID entre comillas, excepto cuando se usa el modificador de compilador MIDL [**/OSF**](-osf.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La biblioteca en tiempo de ejecución utiliza el UUID de la interfaz que el atributo **\[ UUID \]** designa para ayudar a establecer la comunicación entre las aplicaciones cliente y servidor. El atributo **\[ UUID \]** puede aparecer en la lista de atributos de interfaz para una interfaz RPC o una interfaz com.

En el caso de una interfaz RPC, la lista de atributos de interfaz debe incluir el atributo **\[ UUID \]** o el **\[** [](local.md) **\]** atributo local y el que elija debe aparecer exactamente una vez. Si la lista incluye el atributo **\[ UUID \]** , también puede incluir el atributo **\[** [**version**](version.md) **\]** .

En el caso de una interfaz COM (identificada por el atributo de la interfaz de **\[** [**objeto**](object.md) **\]** ), la lista de atributos de interfaz debe incluir el atributo de **\[ UUID \]** , pero no puede incluir el atributo de **\[ versión \]** . La lista de una interfaz COM puede incluir el atributo **\[ local \]** aunque el atributo **\[ UUID \]** esté presente.

Microsoft RPC es compatible con una extensión de DCE IDL que permite escribir el UUID entre comillas dobles ("" "). El formulario entrecomillado es necesario para los preprocesadores del compilador de C que interpretan los números de UUID como números de punto flotante.

Todos los valores UUID deben ser generados por el equipo para garantizar la exclusividad. Use la utilidad uuidgen para generar valores únicos de UUID.

El UUID y los números de versión de la interfaz se usan para determinar si el cliente puede enlazar con el servidor. Para que el cliente se enlace al servidor, el UUID especificado en las interfaces de cliente y de servidor debe ser el mismo.

Tenga en cuenta que una interfaz sin atributos se puede importar en un archivo IDL base. Sin embargo, la interfaz debe contener solo tipos de contenido sin procedimientos. Si hay un procedimiento incluido en la interfaz, se debe especificar un atributo local o UUID.

## <a name="examples"></a>Ejemplos

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Versión**](version.md)
</dt> </dl>

 

 




