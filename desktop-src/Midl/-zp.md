---
title: /ZP (modificador)
description: El modificador/ZP es el mismo que el de la opción/Pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /ZP-modificador MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783695"
---
# <a name="zp-switch"></a>/ZP (modificador)

El modificador **/ZP** es el mismo que el de la opción [**/Pack**](-pack.md) .

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*nivel de empaquetado \_* 
</dt> <dd>

Especifica el nivel de empaquetado de las estructuras en el sistema de destino. El valor de nivel de empaquetado se puede establecer en 1, 2, 4 u 8.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El modificador **/ZP** designa el nivel de empaquetado de las estructuras en el sistema de destino. El valor de nivel de empaquetado corresponde al valor de la opción **/ZP** usado por el compilador de C/C++ de Microsoft. Para obtener más información, vea la documentación de programación de Microsoft C/C++.

Especifique el mismo nivel de empaquetado al invocar el compilador de MIDL y el compilador de C.

El nivel de empaquetado predeterminado que se usa cuando no se especifica el modificador **/ZP** ni [**/Pack**](-pack.md) es 8 en todos los entornos de compilación.

> [!Note]  
> No use **/Zp1** o **/ZP2** en plataformas MIPS o Alpha y no use **/Zp4** o **/Zp8** en plataformas de 16 bits. En función del tipo de datos y la ubicación de memoria asignada por el compilador de C en tiempo de ejecución, esto puede dar lugar a una excepción de errores de alineación de datos en las plataformas de MIPS y Alpha. En las plataformas de MS-DOS, el compilador de C no garantizará la alineación en 4 u 8, por lo que la aplicación puede finalizar.

 

## <a name="examples"></a>Ejemplos

**MIDL/Zp4 nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> </dl>

 

 




