---
description: ICE97 comprueba que dos componentes no aíslan un componente compartido en el mismo directorio.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074497"
---
# <a name="ice97"></a>ICE97

ICE97 comprueba que dos componentes no aíslan un componente compartido en el mismo directorio.

## <a name="result"></a>Resultado

ICE97 publica las advertencias siguientes.



| Advertencia de ICE97                                                                                                                                                                    | Descripción                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Este componente 1 instala el componente Compartido en el mismo directorio 2 que otro, lo que interrumpe las reglas de componente si ambos \[ \] componentes (o más) están seleccionados \[ para la \] instalación. | Dos componentes no deben aislar un componente compartido en el mismo directorio. |



 

Por ejemplo, Component1 y Component2, que comparten ComponentShared, se instalan en el mismo directorio. Ambos especifican ComponentShared como componente aislado. Debido al aislamiento, los archivos de ComponentShared se copian dos veces en la referencia de directorio \_ para Component1 y Component2. Los componentes ahora tienen un recuento de referencias en la copia de archivos. Esto infringe las reglas de componentes del instalador. Si se desinstala Component1, se quitan los archivos de componentes aislados y se rompe Component2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



