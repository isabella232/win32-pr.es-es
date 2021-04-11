---
description: Las funciones GetUpdateRect y GetUpdateRgn recuperan la región de actualización actual para la ventana.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Recuperación de la región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275978"
---
# <a name="retrieving-the-update-region"></a>Recuperación de la región de actualización

Las funciones [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) y [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) recuperan la región de actualización actual para la ventana. GetUpdateRect recupera el rectángulo más pequeño (en coordenadas lógicas) que incluye toda la región de actualización. GetUpdateRgn recupera la propia región de actualización. Estas funciones se pueden usar para calcular el tamaño actual de la región de actualización con el fin de determinar dónde realizar una operación de dibujo.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) también recupera las dimensiones del rectángulo más pequeño que rodea la región de actualización actual y copia las dimensiones en el miembro **rcPaint** de la estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) . Dado que **BeginPaint** valida la región de actualización, cualquier llamada a [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) y [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) inmediatamente después de una llamada a **BeginPaint** devuelve una región de actualización vacía.

 

 



