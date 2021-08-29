---
description: La función ExcludeUpdateRgn excluye la región de actualización de la región de recorte para el contexto del dispositivo de visualización.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Exclusión de la región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1551990c1da985240ee606223177eb3e84118a7083c459e3991451cd313f3c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092945"
---
# <a name="excluding-the-update-region"></a>Exclusión de la región de actualización

La [**función ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) excluye la región de actualización de la región de recorte para el contexto del dispositivo de visualización. Esta función es útil al dibujar en una ventana que no sea cuando se está procesando \_ un mensaje WM PAINT. Impide dibujar en las áreas que se actualizarán durante el siguiente mensaje \_ DE WM PAINT.

 

 



