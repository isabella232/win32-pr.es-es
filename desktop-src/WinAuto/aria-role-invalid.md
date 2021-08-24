---
title: Error de rol de ARIA
description: Error de rol de ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c0fcef639a54bcd805bcb3f239e8d42cfeda8c5111d128c5f54157db75d7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134018"
---
# <a name="aria-role-error"></a>Error de rol de ARIA

## <a name="text"></a>Texto

El elemento tiene el rol DE-ARIA NO VÁLIDO.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a todos los elementos que tienen el [**atributo role.**](https://developer.mozilla.org/docs/Web/HTML/Reference) Indica que el  atributo de rol no es un valor válido del rol Iniciativa de accesibilidad web: aplicaciones de Internet enriquecidas accesibles (WAI-ARIA), tal como se define en la especificación DEIA-ARIA. Establecer un rol válido ayuda a garantizar que los lectores de pantalla y otras herramientas de tecnología de asistencia interpretan correctamente el elemento.

Para corregir este error, establezca el [**atributo de rol**](https://developer.mozilla.org/docs/Web/HTML/Reference) en un valor de rol VALID DE-ARIA. Tenga en cuenta que los roles ABSTRACT DE ARIA no son válidos.

## <a name="example"></a>Ejemplo


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Error de rol de contenedor de ARIA](aria-container-role.md)
</dt> </dl>

 

 




