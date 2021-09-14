---
title: Modificador /ms_ext
description: A partir de la versión 3.0 de MIDL, las características habilitadas por el modificador ms ext ahora son el modo predeterminado \_ para el compilador MIDL.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext switch MIDL
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159740"
---
# <a name="ms_ext-switch"></a>Modificador /ms \_ ext

A partir de la versión 3.0 de MIDL, las características habilitadas por el modificador **ms \_ ext** ahora son el modo predeterminado para el compilador MIDL.

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

El uso del modificador no generará un error del compilador, por lo que no es necesario quitar las referencias a **/ms \_ ext** o [**/c \_ ext**](-c-ext.md) de un archivo Make existente.

Las siguientes extensiones de Microsoft para OSF DCE ahora están disponibles de forma predeterminada:

-   Definiciones de interfaz para objetos OLE. Para obtener más información sobre los archivos generados para interfaces OLE, vea [Archivos generados para una interfaz COM.](files-generated-for-a-com-interface.md)
-   Atributo [**\[ de \] devolución de**](callback.md) llamada que especifica una función de devolución de llamada estática en el cliente
-   [**cpp \_ quote**](cpp-quote.md)(*quoted \_ string*) and [**\# pragma midl \_ echo**](pragma.md)
-   [**wchar \_ t**](wchar-t.md) tipos de caracteres anchos, constantes y cadenas
-   [**inicialización de enumeración**](enum.md) (enumeradores dispersos)
-   Expresiones como especificadores de tamaño y discriminador
-   [Control de extensiones](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [Herencia de tipos de atributo de puntero](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [Varias interfaces](/windows/desktop/Rpc/registering-interfaces)
-   Definiciones fuera del bloque de interfaz
-   Puede omitir atributos [direccionales](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**en**](in.md), [**out**](out-idl.md)\]

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Herencia de tipos de atributo de puntero](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**/app \_ config**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 