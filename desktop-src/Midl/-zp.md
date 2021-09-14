---
title: Modificador /Zp
description: El modificador /Zp es el mismo que la opción /pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /Zp switch MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159697"
---
# <a name="zp-switch"></a>Modificador /Zp

El **modificador /Zp** es el mismo que la [**opción /pack.**](-pack.md)

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*nivel de \_ empaquetado* 
</dt> <dd>

Especifica el nivel de empaquetado de las estructuras en el sistema de destino. El valor de nivel de empaquetado se puede establecer en 1, 2, 4 u 8.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **modificador /Zp** designa el nivel de empaquetado de las estructuras en el sistema de destino. El valor de nivel de empaquetado corresponde al valor de la opción **/Zp** usado por el compilador de Microsoft C/C++. Para obtener más información, consulte la documentación de programación de Microsoft C/C++.

Especifique el mismo nivel de empaquetado al invocar el compilador MIDL y el compilador de C.

El nivel de empaquetado predeterminado que se usa cuando no se especifica el modificador **/Zp** ni [**/pack**](-pack.md) es 8 en todos los entornos de compilación.

> [!Note]  
> No use **/Zp1** o **/Zp2** en las plataformas MIPS o Alpha y no use **/Zp4** o **/Zp8** en plataformas de 16 bits. Según el tipo de datos y la ubicación de memoria asignada por el compilador de C en tiempo de ejecución, esto puede dar lugar a una excepción de desalineación de datos en las plataformas MIPS y Alpha. En las plataformas MS-DOS, el compilador de C no garantizará la alineación en 4 u 8, por lo que la aplicación puede finalizar.

 

## <a name="examples"></a>Ejemplos

**midl /Zp4 filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/pack**](-pack.md)
</dt> </dl>

 

 




