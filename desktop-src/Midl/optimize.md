---
title: atributo optimize
description: El atributo \ optimize\ ACF se usa para ajustar el nivel de gradación para serializar los datos.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- optimización del atributo MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7703a3539ff16c7f2dc78d51c62cfe05612dcb6e935bb5c5701f9a7b59a9f1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869575"
---
# <a name="optimize-attribute"></a>atributo optimize

El **\[ atributo optimize \]** ACF se usa para ajustar el nivel de gradación para serializar los datos.

> [!Note]  
> Esta palabra clave se superceed y no se debe usar. Las compilaciones MIDL actuales deben [**usar /Oicf**](-oi.md)[**/robust en su**](-robust.md) lugar.

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*optimization-options* 
</dt> <dd>

Especifica el método de serialización de datos. Use "s" para la serialización en modo mixto o "i" para la serialización interpretada.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta versión de RPC proporciona dos métodos para serializar datos: modo mixto ("s") e interpretado ("i"). Estos métodos corresponden a los modificadores de línea de comandos [**/Os**](-os.md) y [**/Oi.**](-oi.md) El método interpretado serializa los datos completamente sin conexión. Aunque esto puede reducir considerablemente el tamaño del código auxiliar, el rendimiento puede verse afectado.

Si el rendimiento es un problema, el método de modo mixto puede ser el mejor enfoque. El modo mixto permite que el compilador MIDL realice la determinación entre qué datos se serializarán en línea y cuáles se serializarán mediante una llamada a una biblioteca de vínculos dinámicos sin conexión. Si muchos procedimientos usan los mismos tipos de datos, se puede llamar repetidamente a un único procedimiento para serializar los datos. De esta manera, los datos más adecuados para la serialización insertada se procesan en línea, mientras que otros datos se pueden serializar sin conexión de forma más eficaz.

Tenga en cuenta que **\[ el atributo optimize \]** se puede usar como atributo de interfaz o como atributo de operación. Si se usa como atributo de interfaz, establece el valor predeterminado para toda la interfaz, reemplazando los modificadores de línea de comandos. Sin embargo, si se usa como atributo de operación, solo afecta a esa operación, invalidando los modificadores de línea de comandos y el valor predeterminado de la interfaz.

## <a name="examples"></a>Ejemplos

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de configuración de la aplicación (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




