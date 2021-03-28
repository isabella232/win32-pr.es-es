---
title: Representar un efecto (Direct3D 11)
description: Se puede usar un efecto para almacenar información o para representar mediante un grupo de estado.
ms.assetid: 7af239de-812d-4295-b599-b9deb371b01b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c99aef9f83cdf286e86ca843e57315d9ab88619
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420955"
---
# <a name="rendering-an-effect-direct3d-11"></a>Representar un efecto (Direct3D 11)

Se puede usar un efecto para almacenar información o para representar mediante un grupo de estado. Cada técnica especifica un conjunto de sombreadores de vértices, sombreadores de casco, sombreadores de dominio, sombreadores de geometría, sombreadores de píxeles, sombreadores de cálculo, estado del sombreador, estado de muestra y textura, estado de vista de acceso desordenado y otro estado de canalización. Por tanto, una vez que haya organizado el estado en un efecto, puede encapsular el efecto de representación resultante de ese estado mediante la creación y representación del efecto.

Hay algunos pasos para preparar un efecto para la representación. La primera es la compilación, que comprueba el código de HLSL como el código con la sintaxis del lenguaje HLSL y las reglas del marco de efecto. Puede compilar un efecto desde la aplicación mediante llamadas API o puede compilar un efecto sin conexión mediante la utilidad del compilador [fxc.exe](/windows/desktop/direct3dtools/fxc). Una vez que el efecto se ha compilado correctamente, créelo llamando a un conjunto de API diferente (pero muy similar).

Una vez creado el efecto, hay dos pasos restantes para usarlo. En primer lugar, debe inicializar los valores de estado del efecto (los valores de las variables de efecto) mediante una serie de métodos para establecer el estado si no se inicializan en HLSL. En el caso de algunas variables, esto se puede hacer una vez cuando se crea un efecto; otros deben actualizarse cada vez que la aplicación llame al bucle de representación. Una vez establecidas las variables de efecto, se indica al tiempo de ejecución que represente el efecto aplicando una técnica. Estos temas se describen con más detalle a continuación.

Naturalmente, existen consideraciones de rendimiento para el uso de efectos. Estas consideraciones son en gran medida las mismas si no está utilizando un efecto. Cosas como minimizar la cantidad de cambios de estado y organizar las variables por frecuencia de actualización. Estas tácticas se usan para minimizar la cantidad de datos que deben enviarse desde la CPU a la GPU y, por tanto, minimizar los posibles problemas de sincronización.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                        | Descripción                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Compilar un efecto](d3d11-graphics-programming-guide-effects-compile.md)<br/>         | Una vez creado un efecto, el paso siguiente consiste en compilar el código para comprobar si hay problemas de sintaxis.<br/>                                                                                                                                                                                                          |
| [Crear un efecto](d3d11-graphics-programming-guide-effects-create.md)<br/>           | Un efecto se crea cargando el código de bytes de efecto compilado en el marco de trabajo de efectos. A diferencia de los efectos 10, el efecto debe compilarse antes de crear el efecto. Los efectos cargados en la memoria se pueden crear mediante una llamada a [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).<br/>                 |
| [Establecer estado de efecto](d3d11-graphics-programming-guide-effects-set-state.md)<br/>        | Algunas constantes Effect solo deben inicializarse. Una vez inicializado, el estado del efecto se establece en el dispositivo para todo el bucle de representación. Es necesario actualizar otras variables cada vez que se llama al bucle de representación. A continuación se muestra el código básico para establecer las variables de efecto, para cada uno de los tipos de variables.<br/> |
| [Aplicar una técnica](d3d11-graphics-programming-guide-effects-apply-technique.md)<br/> | Con las constantes, las texturas y el estado del sombreador declarado e inicializado, lo único que queda por hacer es establecer el estado del efecto en el dispositivo.<br/>                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

