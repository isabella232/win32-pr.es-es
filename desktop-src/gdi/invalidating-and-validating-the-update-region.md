---
description: Una aplicación invalida una parte de una ventana y establece la región de actualización mediante la función InvalidateRect o InvalidateRgn.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Invalidación y validación de la región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba895875f9ec1350b6eb28ccb8f1721df6999ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984950"
---
# <a name="invalidating-and-validating-the-update-region"></a>Invalidación y validación de la región de actualización

Una aplicación invalida una parte de una ventana y establece la región de actualización mediante la función [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) o [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) . Estas funciones agregan el rectángulo o región especificados (en coordenadas de cliente) a la región de actualización, combinando el rectángulo o la región con cualquier elemento que el sistema o la aplicación hayan agregado previamente a la región de actualización.

Las funciones [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) y [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) no generan mensajes de [**WM \_ Paint**](wm-paint.md) . En su lugar, el sistema acumula los cambios realizados por estas funciones y sus propios cambios mientras una ventana procesa otros mensajes en su cola de mensajes. Al acumular los cambios, una ventana procesa todos los cambios a la vez en lugar de actualizar bits y partes en un paso cada vez.

Las funciones [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) y [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) validan una parte de la ventana quitando un rectángulo o una región especificados de la región de actualización. Estas funciones se utilizan normalmente cuando la ventana ha actualizado una parte específica de la pantalla en la región de actualización antes de recibir el mensaje de [**\_ dibujo de WM**](wm-paint.md) .

 

 



