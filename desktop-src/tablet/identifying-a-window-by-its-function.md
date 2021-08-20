---
description: Descripción de la identificación de una ventana por su función para tablet PC.
ms.assetid: 513e0c9d-4c9e-4e7c-8314-bd7603489e89
title: Identificar una ventana por su función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7b7255fd22b44d3aa7de8f9ef11a35db95f822d8029f0a56428b1c04f8ecf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044377"
---
# <a name="identifying-a-window-by-its-function"></a>Identificar una ventana por su función

Para identificar cada tipo de ventana, asígnele una clase de ventana única. Evite tener una sola clase de ventana que se utilice para una amplia variedad de funciones.

Las ayuda de accesibilidad deben tener esta identificación para controlar diferentes ventanas dentro de la misma aplicación. Puede haber instrucciones independientes para controlar estas ventanas, como el anuncio de áreas específicas cuando cambia el contenido.

Si no puede usar clases de ventana independientes, puede exponer las diferencias a través de Microsoft Active Accessibility o, si es necesario, mediante un mensaje de ventana privada que documente en <entity type="reg"/> <entity type="reg"/> su sitio web.

Para obtener más información sobre cómo exponer clases de ventana mediante Active Accessibility, vea la [sección Accesibilidad.](/windows/desktop/accessibility)

 

 
