---
description: La función ExcludeUpdateRgn excluye la región de actualización de la región de recorte para el contexto del dispositivo de presentación.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Exclusión de la región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580492"
---
# <a name="excluding-the-update-region"></a>Exclusión de la región de actualización

La [**función ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) excluye la región de actualización de la región de recorte para el contexto del dispositivo de visualización. Esta función es útil al dibujar en una ventana que no sea cuando se está procesando \_ un mensaje WM PAINT. Impide dibujar en las áreas que se actualizarán durante el siguiente mensaje \_ DE WM PAINT.

 

 



