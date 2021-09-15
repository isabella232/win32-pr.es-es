---
description: El modo de dirección de textura de color de borde, identificado por el miembro BORDER D3DTADDRESS del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D use un color arbitrario, conocido como color del borde, para cualquier coordenadas de textura fuera del intervalo de \_ 0,0 a 1,0, ambos incluidos.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Modo de dirección de textura de color de borde (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42b18d88f3b9305d0602e43a9528357a9397d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569953"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a>Modo de dirección de textura de color de borde (Direct3D 9)

El modo de dirección de textura de color de borde, identificado por el miembro BORDER D3DTADDRESS del tipo enumerado D3DTEXTUREADDRESS, hace que Direct3D use un color arbitrario, conocido como color del borde, para cualquier coordenadas de textura fuera del intervalo de \_ 0,0 a 1,0, ambos incluidos. [](./d3dtextureaddress.md)

En la ilustración siguiente, la aplicación especifica que la textura se aplique a la primitiva mediante un borde rojo.

![ilustración de una textura y una textura con un borde rojo](images/border.png)

Las aplicaciones establecen el color del borde mediante una [**llamada a IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate). Establezca el primer parámetro para la llamada al identificador de fase de textura deseado, el segundo parámetro en el valor de estado de la fase BORDERCOLOR de D3DSAMP y el tercer parámetro en el nuevo color de \_ borde RGBA.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modos de direccionamiento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
