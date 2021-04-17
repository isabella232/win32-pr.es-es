---
title: Estructura RESOURCEHEADER
description: Contiene información sobre el propio encabezado de recursos y los datos específicos de este recurso.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Menús de la estructura RESOURCEHEADER y otros recursos
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714554"
---
# <a name="resourceheader-structure"></a>Estructura RESOURCEHEADER

Contiene información sobre el propio encabezado de recursos y los datos específicos de este recurso. Esta estructura no es una verdadera estructura de lenguaje C, porque contiene miembros de longitud variable. La definición de la estructura que se proporciona aquí solo es para explicación; no se encuentra en ningún archivo de encabezado estándar.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**DataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño, en bytes, de los datos que siguen al encabezado de recursos para este recurso concreto. No incluye ningún relleno de archivos entre este recurso y cualquier recurso que lo siga en el archivo de recursos.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño, en bytes, de los datos del encabezado de recursos que se indican a continuación.

</dd> <dt>

**TYPE**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

El tipo de recurso. El miembro de **tipo** puede ser un valor numérico o una cadena Unicode terminada en null que especifica el nombre del tipo. Vea la siguiente sección de comentarios para obtener una descripción de los miembros de **nombre** o de tipo **ordinal** .

Si el miembro de **tipo** es un valor numérico, puede especificar un tipo de recurso estándar o definido por el usuario. Si el miembro es una cadena, se trata de un tipo de recurso definido por el usuario. Para obtener una lista de los tipos de recursos predefinidos, consulte [tipos de recursos](/windows/desktop/menurc/resource-types).

Los valores inferiores a 256 se reservan para uso del sistema.

</dd> <dt>

**NOMBRE**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Nombre que identifica el recurso en particular. El miembro de **nombre** , al igual que el miembro de **tipo** , puede ser un valor numérico o una cadena Unicode terminada en NULL. Vea la siguiente sección de comentarios para obtener una descripción de los miembros de **nombre** o de tipo **ordinal** .

No es necesario agregar relleno para la alineación **DWORD** entre los miembros **Type** y **Name** porque contienen datos de **Word** . Sin embargo, puede que tenga que agregar una **palabra** de relleno después del miembro de **nombre** para alinear el resto del encabezado en los límites de **DWORD** .

</dd> <dt>

**DataVersion**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Una versión de datos de recursos predefinida. Esto determinará qué versión de los datos de recursos debe usar la aplicación.

</dd> <dt>

**MemoryFlags**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Un conjunto de marcas de atributo que pueden describir el estado del recurso. Modificadores de. Archivo de script RC asigne estos atributos al recurso. Los identificadores de script pueden asignar los siguientes valores de marca.

Las aplicaciones no usan ninguno de estos atributos. Los atributos se permiten en el script para la compatibilidad con versiones anteriores de los scripts existentes, pero se omiten. Los recursos se cargan cuando se carga el módulo correspondiente y se liberan cuando se descarga el módulo.

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

**Móvil** (0x0010)


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

**corregido** (~ movible)


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

**Puro** (0x0020)


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

**IMpurar** (~ puro)


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

**Carga previa** (0x0040)


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

**LOADONCALL** (~ preload)


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

**DEScartable** (0x1000)


</dt> <dd></dd> </dl> </dd> <dt>

**LanguageId**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Lenguaje del recurso o conjunto de recursos. Establezca el valor de este miembro con la instrucción de definición de recursos de [lenguaje](./language-statement.md) opcional. Los parámetros son constantes del archivo winnt. h.

Cada recurso incluye un identificador de idioma, por lo que el sistema o la aplicación pueden seleccionar un idioma adecuado para la configuración regional actual del sistema. Si hay varios recursos del mismo tipo y nombre que solo difieren en el idioma de las cadenas dentro de los recursos, deberá especificar un **iddeidioma** para cada uno.

</dd> <dt>

**Versión**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Un número de versión definido por el usuario para los datos de recursos que las herramientas pueden utilizar para leer y escribir archivos de recursos. Establezca este valor con la instrucción de definición de recursos de [versión](./version-statement.md) opcional.

</dd> <dt>

**Características**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica la información definida por el usuario sobre el recurso que las herramientas pueden utilizar para leer y escribir archivos de recursos. Establezca este valor con la instrucción de definición de recursos de [características](./characteristics-statement.md) opcionales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un miembro de tipo variable se denomina **nombre** o miembro **ordinal** , y se usa en la mayoría de los lugares del archivo de recursos donde aparece un identificador. La primera **palabra** de un miembro de **nombre** o de tipo **ordinal** indica si el miembro es un valor numérico o una cadena. Si la primera **palabra** del miembro es igual al valor 0xFFFF, que es un carácter Unicode no válido, la **palabra** siguiente es un número de tipo. De lo contrario, el miembro contiene una cadena Unicode y la primera **palabra** del miembro es el primer carácter de la cadena de nombre. Para obtener más información sobre las instrucciones de definición de recursos, vea [instrucciones de definición de recursos](./resource-definition-statements.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Vista**
</dt> <dt>

[Recursos](resources.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Instrucción CHARACTERISTICS](./characteristics-statement.md)
</dt> <dt>

[LANGUAGE (instrucción)](./language-statement.md)
</dt> <dt>

[VERSION (instrucción)](./version-statement.md)
</dt> </dl>

 

