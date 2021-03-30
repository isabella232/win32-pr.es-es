---
description: La plantilla CMSPArray implementa una matriz inteligente que crecerá a petición.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002063"
---
# <a name="cmsparray"></a>CMSPArray

La plantilla CMSPArray implementa una matriz inteligente que crecerá a petición. Está diseñado para contener matrices pequeñas con tipos de datos simples. No tiene una sección crítica. Sus únicas dependencias son **realloc** y **memmove**. Se utiliza internamente para mantener listas de punteros de objeto. Es similar a la implementación de **CSimpleArray** de ATL, pero es más eficaz para las asignaciones iniciales.

Esta plantilla se define en MSPutils. h.

 

 



