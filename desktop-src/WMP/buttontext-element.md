---
title: ButtonText (Elemento)
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. | Elemento ButtonText
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Elemento ButtonText Windows Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700414"
---
# <a name="buttontext-element"></a>ButtonText (Elemento)

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El elemento **ButtonText** especifica la cadena de texto que Windows Media Player muestra para un botón del panel de tareas.

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elemento                                              |
|-----------------|------------------------------------------------------|
| Elementos primarios | **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |
| Elementos secundarios  | Ninguno                                                 |



 

## <a name="remarks"></a>Observaciones

Este elemento es necesario para cada instancia de **ServiceTask1**, **ServiceTask2** o **ServiceTask3**.

> [!Note]  
> Windows Media Player 10 tiene tres paneles de tareas en los que una tienda en línea puede mostrar sus páginas Web. La tienda en línea puede elegir usar uno, dos o los tres paneles de tareas. Windows Media Player 11 solo tiene un panel de tareas, que el usuario puede ver haciendo clic en la pestaña **tiendas en línea** . Windows Media Player 11 omite los elementos **ServiceTask2** y **ServiceTask3** .

 

Windows Media Player puede recortar el texto del botón para ajustarse al espacio disponible. El reproductor siempre usa la fuente Tahoma de 8 puntos de negrita para este texto. Hay dos líneas disponibles para mostrar el texto del botón, pero el reproductor no ajusta automáticamente el texto de la primera línea al segundo. Para especificar un salto de línea en el texto del botón, inserte la nueva secuencia de escape de línea " \\ n" en la cadena de texto.

La cadena de texto también se muestra en el menú **ir** en la interfaz de usuario de Windows Media Player.

Debe probar la tienda en línea con una variedad de opciones de visualización para asegurarse de que el texto se muestre como se espera.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





