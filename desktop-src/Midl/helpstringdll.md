---
title: atributo helpstringdll
description: El atributo \ helpstringdll \ establece el nombre del archivo DLL que se va a usar para realizar una búsqueda de cadena de documento.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- helpstringdll (atributo) MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995154"
---
# <a name="helpstringdll-attribute"></a>atributo helpstringdll

El atributo **\[ helpstringdll \]** establece el nombre del archivo DLL que se va a usar para realizar una búsqueda de cadena de documento.

``` syntax
[
    helpstringdll(help-text-string)
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
};
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Help-Text-String* 
</dt> <dd>

Una cadena de caracteres terminada en cero que especifica el nombre de archivo completo de un archivo DLL.

</dd> <dt>

*opcional-Attribute-List* 
</dt> <dd>

Otros atributos que se aplican a la instrucción Library en conjunto.

</dd> <dt>

*nombre de biblioteca* 
</dt> <dd>

El identificador que los componentes de software usarán para denotar esta [**biblioteca**](library.md).

</dd> <dt>

*Library-Definition-instrucciones* 
</dt> <dd>

Una o más instrucciones MIDL que definen la interfaz de la [**biblioteca**](library.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Utilice el atributo **\[ helpstringdll \]** en una instrucción Library para especificar, como una cadena de caracteres, el nombre de archivo completo de una biblioteca de vínculos dinámicos. Esto permite que un usuario vea una descripción del archivo DLL con el visor de objetos.

Use las funciones **GetDocumentation2** en las interfaces **ITypeLib2** e **ITypeInfo2** para recuperar la cadena de ayuda.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**biblioteca**](library.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 