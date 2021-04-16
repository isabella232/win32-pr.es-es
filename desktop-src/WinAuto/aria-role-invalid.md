---
title: Error de rol de ARIA
description: Error de rol de ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df04ad94d68ae1e8e2e8d3352aa349834a2389fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105685802"
---
# <a name="aria-role-error"></a>Error de rol de ARIA

## <a name="text"></a>Texto

El elemento tiene un rol WAI-ARIA no válido.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a todos los elementos que tienen el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) . Indica que el atributo **role** no es un valor de rol de aplicaciones de Internet enriquecidas (WAI-ARIA) accesible para la iniciativa de accesibilidad web, tal como se define en la especificación WAI-ARIA. Establecer un rol válido ayuda a garantizar que el elemento sea interpretado correctamente por los lectores de pantalla y otras herramientas de tecnología de asistencia.

Para corregir este error, establezca el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) en un valor de rol WAI-ARIA válido. Tenga en cuenta que los roles WAI-ARIA abstractos no son válidos.

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

 

 




