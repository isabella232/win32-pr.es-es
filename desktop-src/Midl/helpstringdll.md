---
title: atributo helpstringdll
description: El atributo \ helpstringdll\ establece el nombre del archivo DLL que se usará para realizar una búsqueda de cadenas de documento.
ms.assetid: 1b9b962c-c355-4428-b5ea-dc7fd48b50a9
keywords:
- Atributo helpstringdll MIDL
topic_type:
- apiref
api_name:
- helpstringdll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dace4fb9ddc3908ce637cd2d8521a1ab4671d620
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159562"
---
# <a name="helpstringdll-attribute"></a>atributo helpstringdll

El **\[ atributo helpstringdll \]** establece el nombre del archivo DLL que se usará para realizar una búsqueda de cadenas de documento.

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

*help-text-string* 
</dt> <dd>

Cadena de caracteres terminada en cero que especifica el nombre de archivo completo de un archivo DLL.

</dd> <dt>

*optional-attribute-list* 
</dt> <dd>

Otros atributos que se aplican a la instrucción de biblioteca en su conjunto.

</dd> <dt>

*library-name* 
</dt> <dd>

Identificador que los componentes de software usarán para denotar esta [**biblioteca.**](library.md)

</dd> <dt>

*library-definition-statements* 
</dt> <dd>

Una o varias instrucciones MIDL que definen la interfaz de la [**biblioteca**](library.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use el **\[ atributo \] helpstringdll** en una instrucción de biblioteca para especificar, como una cadena de caracteres, el nombre de archivo completo de una biblioteca de vínculos dinámicos. Esto permite a un usuario ver una descripción del archivo DLL con el visor de objetos.

Use las **funciones GetDocumentation2** en las interfaces **ITypeLib2** e **ITypeInfo2** para recuperar la cadena de ayuda.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Biblioteca**](library.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 