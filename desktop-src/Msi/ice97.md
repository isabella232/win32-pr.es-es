---
description: ICE97 comprueba que dos componentes no aíslan un componente compartido en el mismo directorio.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652791"
---
# <a name="ice97"></a>ICE97

ICE97 comprueba que dos componentes no aíslan un componente compartido en el mismo directorio.

## <a name="result"></a>Resultado

ICE97 expone las siguientes advertencias.



| ADVERTENCIA de ICE97                                                                                                                                                                    | Descripción                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Este componente \[ 1 \] instala el componente compartido en el mismo directorio \[ 2 \] que otro, lo que interrumpe las reglas de componentes si se seleccionan los dos (o más) componentes para la instalación. | Dos componentes no deben aislar un componente compartido en el mismo directorio. |



 

Por ejemplo, Component1 y Component2, que comparten ComponentShared, se instalan en el mismo directorio. Ambos especifican ComponentShared como un componente aislado. Debido al aislamiento, los archivos de ComponentShared se copian dos veces en la \_ referencia de directorio para Component1 y Component2. Los componentes ahora tienen un recuento de referencias en la copia de archivos. Esto infringe las reglas del componente instalador. Si se desinstala Component1, se quitan los archivos de componentes aislados y Component2 se rompe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



