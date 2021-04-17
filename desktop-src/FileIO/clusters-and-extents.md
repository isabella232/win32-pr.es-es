---
description: 'Se puede hacer referencia a los clústeres desde dos perspectivas diferentes: dentro del archivo y en el volumen.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Clústeres y extensiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687658"
---
# <a name="clusters-and-extents"></a>Clústeres y extensiones

Se puede hacer referencia a los clústeres desde dos perspectivas diferentes: dentro del archivo y en el volumen. Cualquier clúster de un archivo tiene un *número de clúster virtual* (VCN), que es su desplazamiento relativo desde el principio del archivo. Por ejemplo, una búsqueda de dos veces el tamaño de un clúster, seguido de una lectura, devolverá datos que comienzan en el tercer VCN. Un *número de clúster lógico* (LCN) describe el desplazamiento de un clúster desde algún punto arbitrario dentro del volumen. LCNs solo se debe tratar como números ordinales o relativos. No hay ninguna asignación garantizada de clústeres lógicos a los sectores de la unidad de disco duro física.

Una *extensión* es una ejecución de clústeres contiguos. Por ejemplo, supongamos que un archivo que consta de 30 clústeres se registra en dos extensiones. La primera extensión puede constar de cinco clústeres contiguos, el otro de los 25 clústeres restantes.

No hay ninguna garantía de ninguna relación en el disco de cualquier extensión en cualquier otra extensión. Por ejemplo, la primera extensión puede estar en un LCN superior al de una extensión posterior.

 

 



