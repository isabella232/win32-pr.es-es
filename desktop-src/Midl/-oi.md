---
title: Parámetro/OI
description: Los modificadores/OI y/OIC indican al compilador de MIDL que use un método de serialización totalmente interpretado. El modificador/Oicf proporciona mejoras de rendimiento adicionales.
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- Parámetro/OI del modificador
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1671b16640d3f3214f10138e50a2ac08b6114674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270884"
---
# <a name="oi-switch"></a>Parámetro/OI

Los modificadores **/OI** y **/OIC** indican al compilador de MIDL que use un método de serialización totalmente interpretado. El modificador **/Oicf** proporciona mejoras de rendimiento adicionales.

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*OI* 
</dt> <dd>

Especifica el método totalmente interpretado para calcular las referencias del código auxiliar que se pasa entre el cliente y el servidor.

> [!Note]  
> Este modificador está obsoleto. Se recomienda usar el modificador **/Oicf** en su lugar.

 

</dd> <dt>

*Oic* 
</dt> <dd>

Especifica el método de serialización del proxy no codificado que proporciona todas las características de **/OI** y, además, reduce aún más el tamaño del código auxiliar de cliente para las interfaces de objeto.

> [!Note]  
> Este modificador está obsoleto. Se recomienda usar el modificador **/Oicf** en su lugar.

 

</dd> <dt>

*Interfaces salientes o Oicf* 
</dt> <dd>

Especifica el método de serialización del proxy sin código que incluye todas las características proporcionadas por **/OI** y **/OIC** , pero usa un nuevo intérprete (cadenas de formato rápido) que proporciona un mejor rendimiento que **/OI** o **/OIC**. Este modificador incluye mejoras de RPC recientes y se recomienda para escenarios de RPC modernos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Tenga en cuenta las restricciones relacionadas con las plataformas de soporte técnico.

El compilador MIDL 3,0 proporciona dos métodos para calcular las referencias del código: interpretado totalmente ( **/OI**, **/OIC** y **/Oicf**) y Mixed-mode ( [**/os**](-os.md)). A partir de la versión 6.0.359 de MIDL, el compilador MIDL  [**genera código auxiliar**](-robust.md) **/Oicf de** de forma predeterminada. Algunas características del lenguaje no se admiten en algunos modos. En este caso, el compilador cambia automáticamente al modo apropiado y emite una advertencia.

Si el rendimiento es un problema, el método de modo mixto ( [**/os**](-os.md)) puede ser el mejor enfoque. En este modo, el compilador elige calcular las referencias de algunos parámetros insertados en el código auxiliar generado. Aunque esto da como resultado un mayor tamaño de código auxiliar, ofrece un mayor rendimiento.

El método totalmente interpretado calcula las referencias de los datos completamente sin conexión. Esto reduce considerablemente el tamaño del código auxiliar, pero disminuye el rendimiento. Además, con el método completamente interpretado, hay un límite de 16 parámetros para cada procedimiento. Cualquier procedimiento que contenga más de 16 parámetros se procesará automáticamente en el modo [**/os**](-os.md) . Entre los modos interpretados, **/Oicf** ofrece el mejor rendimiento y **/OI** ofrece la mejor compatibilidad con versiones anteriores.

Puede usar la opción **/OIF** si la aplicación usa las características de MIDL que se INTRODUJERON con MIDL 3,0, como los atributos de serialización de \[ [**conexión \_**](wire-marshal.md) \] y de cálculo de \[ [**\_ referencias de usuario**](user-marshal.md) \] . Si su aplicación usa [canalizaciones](/windows/desktop/Rpc/pipes) , debe usar la opción **/OIF** ; Si especifica otro modo, el compilador MIDL cambiará a **/OIF**.

Para ajustar la forma en que se calculan las referencias del código auxiliar, Microsoft RPC proporciona un atributo ACF \[ [**Optimize**](optimize.md) \] . Este atributo se utiliza como un atributo de interfaz u operación para seleccionar el modo de cálculo de referencias para interfaces individuales o para operaciones individuales.

### <a name="calling-conventions"></a>Convenciones de llamada

Los códigos auxiliares generados por el compilador MIDL en el método interpretado mediante los modificadores **/OI**, **/OIC** o **/OIF** se deben compilar como un procedimiento Stdcall o Cdecl durante la compilación de C. Una Convención de llamada de PASCAL o fastcall no funcionará. Además, el código auxiliar del servidor se debe compilar como Stdcall.

## <a name="examples"></a>Ejemplos

**nombre de archivo de MIDL/OI. idl**

**MIDL/OIC nombrearchivo. idl**

**MIDL/OIF nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/Robust**](-robust.md)
</dt> <dt>

[**/no \_ robusto**](-no-robust.md)
</dt> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**optimiz**](optimize.md)
</dt> <dt>

[**/no \_ format \_ OPC**](-no-format-opt.md)
</dt> </dl>

 

 