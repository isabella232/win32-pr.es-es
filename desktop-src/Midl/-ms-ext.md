---
title: modificador/ms_ext
description: A partir de la versión 3,0 de MIDL, las características habilitadas por el \_ conmutador MS ext son ahora el modo predeterminado para el compilador de MIDL.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext modificador MIDL
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077608"
---
# <a name="ms_ext-switch"></a>/MS \_ ext switch

A partir de la versión 3,0 de MIDL, las características habilitadas por el conmutador **MS \_ ext** son ahora el modo predeterminado para el compilador de MIDL.

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

El uso del modificador no generará un error del compilador, por lo que no tendrá que quitar las referencias a **/MS \_ ext** o [**/c \_ ext**](-c-ext.md) de un archivo make existente.

Las siguientes extensiones de Microsoft para OSF DCE ahora están disponibles de forma predeterminada:

-   Definiciones de interfaz para objetos OLE. Para obtener más información sobre los archivos generados para las interfaces OLE, consulte [archivos generados para una interfaz com](files-generated-for-a-com-interface.md) .
-   Un atributo de [**\[ devolución \]**](callback.md) de llamada que especifica una función de devolución de llamada estática en el cliente.
-   [**CPP \_ Quote**](cpp-quote.md)(*\_ cadena entrecomillada*) y [**\# pragma MIDL \_ echo**](pragma.md)
-   tipos de caracteres anchos, constantes y cadenas de [**WCHAR \_ t**](wchar-t.md)
-   [**inicialización de enumeración**](enum.md) (enumeradores dispersos)
-   Expresiones como especificadores de tamaño y discriminador
-   [Administrar extensiones](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [Herencia de tipos de atributos de puntero](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [Varias interfaces](/windows/desktop/Rpc/registering-interfaces)
-   Definiciones fuera del bloque de interfaz
-   Puede omitir [los atributos direccionales](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**en**](in.md), [**out**](out-idl.md)\]

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[Herencia de tipos de atributos de puntero](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**configuración de/APP \_**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 