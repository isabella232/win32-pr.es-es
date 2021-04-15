---
description: Direct3D mantiene una lista de hasta ocho texturas actuales. Combina estas texturas en todas las representaciones de primitivas. Solo las texturas creadas como punteros de interfaz de textura se pueden usar en el conjunto de texturas actuales.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Asignar las texturas actuales (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496739"
---
# <a name="assigning-the-current-textures-direct3d-9"></a>Asignar las texturas actuales (Direct3D 9)

Direct3D mantiene una lista de hasta ocho texturas actuales. Combina estas texturas en todas las representaciones de primitivas. Solo las texturas creadas como punteros de interfaz de textura se pueden usar en el conjunto de texturas actuales.

Las aplicaciones llaman al método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para asignar texturas al conjunto de texturas actuales. El primer parámetro debe ser un número en el intervalo de 0-7, ambos inclusive. Pase el puntero de la interfaz de textura como segundo parámetro.

En el ejemplo de código de C++ siguiente se muestra cómo se puede asignar una textura al conjunto de texturas actuales.


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> Los dispositivos de software no admiten la asignación de una textura a más de una fase de textura a la vez.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de texturas](texture-blending.md)
</dt> </dl>

 

 
