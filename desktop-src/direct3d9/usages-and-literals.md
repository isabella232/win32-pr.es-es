---
description: El uso es similar al ámbito de un parámetro, ya que define el ámbito en el que el parámetro es válido.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Usos y literales (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8c9fa8eb30726e783ce763ec8700f715dbd5d2b85ff3bf98340cf604e8e2f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026015"
---
# <a name="usages-and-literals-direct3d-9"></a>Usos y literales (Direct3D 9)

El uso es similar al ámbito de un parámetro, ya que define el ámbito en el que el parámetro es válido.



| Value  | Descripción                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| const  | El parámetro será constante dentro del ámbito de todas las funciones. (Tenga en cuenta que estos parámetros todavía se pueden escribir en con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), porque esto se produce fuera del ámbito de todas las funciones). |
| shared | El parámetro se compartirá en el grupo de efectos.                                                                                                                                                                                                                                    |
| static | El parámetro será invisible para la aplicación, es decir, no se puede acceder a ellos desde [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).                                                                                                  |



 

Marcar un parámetro como literal indica que su valor nunca cambiará. Esto permite que el compilador de efectos realice una optimización adicional.

Solo los parámetros de nivel superior no compartidos se pueden marcar como literales. Los parámetros solo se pueden marcar como literales [**con ID3DXEffectCompiler**](id3dxeffectcompiler.md). Los valores literales no se pueden establecer [**con ID3DXEffect.**](id3dxeffect.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



