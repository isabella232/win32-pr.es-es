---
title: Modificador /Oi
description: Los modificadores /Oi y /Oic dirigen al compilador MIDL a usar un método de serialización totalmente interpretado. El modificador /Oicf proporciona mejoras de rendimiento adicionales.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- /Oi switch MIDL
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38b6faee202e15b7c551297678ce301cbfdcb853b48ecd15c75dda7bb281e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385289"
---
# <a name="oi-switch"></a>Modificador /Oi

Los **modificadores /Oi** y **/Oic** dirigen al compilador MIDL a usar un método de serialización totalmente interpretado. El **modificador /Oicf** proporciona mejoras de rendimiento adicionales.

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*Oi* 
</dt> <dd>

Especifica el método totalmente interpretado para serializar el código auxiliar pasado entre el cliente y el servidor.

> [!Note]  
> Este modificador está obsoleto. Se recomienda usar el **modificador /Oicf** en su lugar.

 

</dd> <dt>

*Oci* 
</dt> <dd>

Especifica el método de serialización de proxy sin código que proporciona todas las características de **/Oi** y también reduce aún más el tamaño del código auxiliar de cliente para las interfaces de objeto.

> [!Note]  
> Este modificador está obsoleto. Se recomienda usar el **modificador /Oicf** en su lugar.

 

</dd> <dt>

*Oif u Oicf* 
</dt> <dd>

Especifica el método de serialización de proxy sin código que incluye todas las características proporcionadas por **/Oi** y **/Oic,** pero usa un nuevo intérprete (cadenas de formato rápido) que proporciona un mejor rendimiento que **/Oi** o **/Oic.** Este modificador incluye mejoras recientes de RPC y se recomienda para escenarios de RPC modernos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Tenga en cuenta las restricciones relacionadas con las plataformas compatibles.

El compilador midl 3.0 proporciona dos métodos para serializar código: totalmente interpretado ( **/Oi**, **/Oic** y **/Oicf**) y modo mixto ( [**/Os**](-os.md)). A partir de la versión 6.0.359 de MIDL, el compilador de MIDL genera códigos auxiliares **/Oicf** Â [**/robust**](-robust.md) de forma predeterminada. Algunas características de lenguaje no se admiten en algunos modos. En este caso, el compilador cambia automáticamente al modo adecuado y emite una advertencia.

Si el rendimiento es un problema, el método de modo mixto ( [**/Os**](-os.md)) puede ser el mejor enfoque. En este modo, el compilador elige serializar algunos parámetros en línea en los códigos auxiliares generados. Aunque esto da como resultado un tamaño de código auxiliar mayor, ofrece un mayor rendimiento.

El método totalmente interpretado serializa los datos completamente sin conexión. Esto reduce considerablemente el tamaño del código auxiliar, pero reduce el rendimiento. Además, con el método totalmente interpretado, hay un límite de 16 parámetros para cada procedimiento. Cualquier procedimiento que contenga más de 16 parámetros se procesará automáticamente en [**modo /Os.**](-os.md) Entre los modos interpretados, **/Oicf** ofrece el mejor rendimiento y **/Oi** ofrece la mejor compatibilidad con versiones anteriores.

Es posible que quiera usar la opción **/Oif** si la aplicación usa características midl que se introdujeron con MIDL 3.0, como la serialización de conexión y los atributos de serialización \[ [**\_**](wire-marshal.md) \] \[ [**\_ de**](user-marshal.md) \] usuario. Si la aplicación usa [canalizaciones,](/windows/desktop/Rpc/pipes) debe usar la **opción /Oif;** si especifica otro modo, el compilador de MIDL cambia a **/Oif**.

Para ajustar la forma en que se serializa el código auxiliar, Rpc de Microsoft proporciona un atributo de optimización \[ [](optimize.md) \] ACF. Este atributo se usa como atributo de interfaz u atributo de operación para seleccionar el modo de serialización para interfaces individuales o para operaciones individuales.

### <a name="calling-conventions"></a>Convenciones de llamada

Los códigos auxiliares generados por el compilador MIDL en el método interpretado mediante los modificadores **/Oi**, **/Oic** o **/Oif** deben compilarse como un procedimiento stdcall o cdecl durante la compilación de C. Una convención de llamada PASCAL o Fastcall no funcionará. Además, el código auxiliar del servidor debe compilarse como stdcall.

## <a name="examples"></a>Ejemplos

**midl /Oi filename.idl**

**midl /Oic filename.idl**

**midl /Oif filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**/no \_ robust**](-no-robust.md)
</dt> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**Optimizar**](optimize.md)
</dt> <dt>

[**/no \_ format \_ opt**](-no-format-opt.md)
</dt> </dl>

 

 