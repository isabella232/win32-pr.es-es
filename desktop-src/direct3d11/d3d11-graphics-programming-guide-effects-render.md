---
title: Representación de un efecto (Direct3D 11)
description: Obtenga información sobre cómo representar un efecto para Direct3D 11. Un efecto se puede usar para almacenar información o para representar mediante un grupo de estado.
ms.assetid: 7af239de-812d-4295-b599-b9deb371b01b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7def8f7bbfb9f2c7a5102eb8e02fc848155e4bde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361291"
---
# <a name="rendering-an-effect-direct3d-11"></a>Representación de un efecto (Direct3D 11)

Un efecto se puede usar para almacenar información o para representar mediante un grupo de estado. Cada técnica especifica un conjunto de sombreadores de vértices, sombreadores de casco, sombreadores de dominio, sombreadores de geometría, sombreadores de píxeles, sombreadores de cálculo, estado de sombreador, estado de muestreo y textura, estado de vista de acceso desordenado y otro estado de canalización. Por lo tanto, una vez que haya organizado el estado en un efecto, puede encapsular el efecto de representación que resulta de ese estado mediante la creación y representación del efecto.

Hay algunos pasos para preparar un efecto para la representación. La primera es la compilación, que comprueba el hlsl como código con la sintaxis del lenguaje HLSL y las reglas del marco de efectos. Puede compilar un efecto desde la aplicación mediante llamadas API o puede compilar un efecto sin conexión mediante la utilidad del compilador de [ efectofxc.exe](/windows/desktop/direct3dtools/fxc). Una vez que el efecto se haya compilado correctamente, puede crearlo mediante una llamada a un conjunto diferente (pero muy similar) de API.

Una vez creado el efecto, hay dos pasos restantes para usarlo. En primer lugar, debe inicializar los valores de estado de efecto (los valores de las variables de efecto) mediante una serie de métodos para establecer el estado si no se inicializan en HLSL. Para algunas variables, esto se puede hacer una vez cuando se crea un efecto. otros deben actualizarse cada vez que la aplicación llama al bucle de representación. Una vez establecidas las variables de efecto, se le dice al tiempo de ejecución que represente el efecto mediante la aplicación de una técnica. Estos temas se tratan con más detalle a continuación.

Naturalmente, hay consideraciones de rendimiento para usar efectos. Estas consideraciones son en gran medida las mismas si no usa ningún efecto. Aspectos como minimizar la cantidad de cambios de estado y organizar las variables por frecuencia de actualización. Estas tácticas se usan para minimizar la cantidad de datos que se deben enviar desde la CPU a la GPU y, por tanto, minimizar los posibles problemas de sincronización.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                        | Descripción                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Compilar un efecto](d3d11-graphics-programming-guide-effects-compile.md)<br/>         | Después de crear un efecto, el siguiente paso es compilar el código para comprobar si hay problemas de sintaxis.<br/>                                                                                                                                                                                                          |
| [Crear un efecto](d3d11-graphics-programming-guide-effects-create.md)<br/>           | Se crea un efecto cargando el código de bytes del efecto compilado en el marco de efectos. A diferencia de Efectos 10, el efecto debe compilarse antes de crear el efecto. Los efectos cargados en memoria se pueden crear llamando a [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).<br/>                 |
| [Establecer estado de efecto](d3d11-graphics-programming-guide-effects-set-state.md)<br/>        | Algunas constantes de efecto solo deben inicializarse. Una vez inicializado, el estado de efecto se establece en el dispositivo para todo el bucle de representación. Cada vez que se llama al bucle de representación, es necesario actualizar otras variables. A continuación se muestra el código básico para establecer variables de efecto, para cada uno de los tipos de variables.<br/> |
| [Aplicar una técnica](d3d11-graphics-programming-guide-effects-apply-technique.md)<br/> | Con las constantes, las texturas y el estado del sombreador declarados e inicializados, lo único que queda por hacer es establecer el estado de efecto en el dispositivo.<br/>                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

