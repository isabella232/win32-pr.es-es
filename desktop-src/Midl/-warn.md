---
title: Modificador /warn
description: El modificador /warn especifica el nivel de advertencia del compilador MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /warn switch MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a51f57be780edeac4a91ea4f127d34d1c004ff700429f405eee4522dcb63ef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067465"
---
# <a name="warn-switch"></a>Modificador /warn

El **modificador /warn** especifica el nivel de advertencia del compilador MIDL.

``` syntax
midl /warn level
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*level* 
</dt> <dd>

Especifica el nivel de advertencia, un entero en el intervalo comprendido entre 0 y 4. No hay espacio entre el **modificador /warn** y el dígito que indica el valor de nivel de advertencia.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El nivel de advertencia indica la gravedad de la advertencia. Los niveles de advertencia oscilan entre 1 y 4, con un valor de cero significado para no mostrar información de advertencia. La advertencia de gravedad más alta es el nivel 1. En la tabla siguiente se describen las advertencias de cada nivel de advertencia.



| Nivel de advertencia | Descripción                                             | Ejemplo                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| 0             | Sin advertencias.                                            |                                                                           |
| 1             | Advertencias graves que pueden provocar errores de aplicación.      | No se ha especificado ningún identificador de enlace, punteros sin atributos, modificadores en conflicto. |
| 2             | Puede causar problemas en el entorno operativo del usuario. | La longitud del identificador supera los 31 caracteres. No se ha especificado ningún arm de unión predeterminado.  |
| 3             | Reservado.                                               |                                                                           |
| 4             | Nivel de advertencia más bajo.                                   | Construcciones C que no son ANSI.                                                    |



 

Las advertencias son diferentes de los errores. Los errores hacen que el compilador MIDL detenga el procesamiento del archivo IDL. Las advertencias hacen que el compilador de MIDL emita un mensaje informativo y continúe procesando el archivo IDL.

El nivel de advertencia establecido por el modificador **/warn** se puede usar con el modificador [**WX**](-wx.md) para hacer que el compilador MIDL detenga el procesamiento del archivo IDL.

El **modificador /warn** se comporta igual que el [**modificador /W.**](-w.md)

## <a name="examples"></a>Ejemplos

**midl /warn2 filename.idl**

**midl /warn4 bar.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




