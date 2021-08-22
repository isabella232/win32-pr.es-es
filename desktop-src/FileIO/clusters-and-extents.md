---
description: 'Se puede hacer referencia a los clústeres desde dos perspectivas diferentes: dentro del archivo y en el volumen.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Clústeres y extensiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce987dc5c8afea842d6c92196474f88d17c36d2011995a2d760b83bfc1e5a644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533845"
---
# <a name="clusters-and-extents"></a>Clústeres y extensiones

Se puede hacer referencia a los clústeres desde dos perspectivas diferentes: dentro del archivo y en el volumen. Cualquier clúster de un archivo tiene un *número de clúster virtual* (VCN), que es su desplazamiento relativo desde el principio del archivo. Por ejemplo, si se busca el doble del tamaño de un clúster, seguido de una lectura, se devolverán datos que comienzan en la tercera VCN. Un *número de clúster lógico* (LCN) describe el desplazamiento de un clúster desde algún punto arbitrario dentro del volumen. Las LCN solo se deben tratar como números ordinales o relativos. No hay ninguna asignación garantizada de clústeres lógicos a sectores de unidades de disco duro físico.

Una *extensión* es una ejecución de clústeres contiguos. Por ejemplo, supongamos que un archivo que consta de 30 clústeres se registra en dos extensiones. La primera extensión puede constar de cinco clústeres contiguos, el otro de los 25 clústeres restantes.

No hay ninguna garantía de ninguna relación en el disco de ninguna otra extensión. Por ejemplo, la primera extensión puede estar en una LCN mayor que una extensión posterior.

 

 



