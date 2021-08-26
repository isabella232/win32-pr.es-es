---
description: Una aplicación invalida una parte de una ventana y establece la región de actualización mediante la función InvalidateRect o InvalidateRgn.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Invalidar y validar la región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6813d88674ef0339cfd3501b561e5a7c95fa5b41f0c7f212e625f9846f5beb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944175"
---
# <a name="invalidating-and-validating-the-update-region"></a>Invalidar y validar la región de actualización

Una aplicación invalida una parte de una ventana y establece la región de actualización mediante la función [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) [**o InvalidateRgn.**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) Estas funciones agregan el rectángulo o la región especificados (en coordenadas de cliente) a la región de actualización, combinando el rectángulo o la región con cualquier cosa que el sistema o la aplicación puedan haber agregado previamente a la región de actualización.

Las [**funciones InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) [**e InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) no generan [**mensajes WM \_ PAINT.**](wm-paint.md) En su lugar, el sistema acumula los cambios realizados por estas funciones y sus propios cambios mientras una ventana procesa otros mensajes en su cola de mensajes. Al acumular cambios, una ventana procesa todos los cambios a la vez en lugar de actualizar los bits y las piezas un paso a la vez.

Las [**funciones ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) y [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) validan una parte de la ventana quitando un rectángulo o región especificados de la región de actualización. Estas funciones se usan normalmente cuando la ventana ha actualizado una parte específica de la pantalla en la región de actualización antes de recibir el [**mensaje \_ WM PAINT.**](wm-paint.md)

 

 



