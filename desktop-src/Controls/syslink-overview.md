---
title: Acerca de los controles SysLink
description: Un control SysLink es una ventana que representa texto marcado y notifica a la aplicación cuando los usuarios hacen clic en sus hipervínculos incrustados. Este control proporciona una alternativa práctica al uso del botón de vínculo Comando. Para obtener más información, vea Tipos de botón.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4a5d64af48fc0b48b15f22fff55e5cb563339ac8d90446981c74e07f5d4713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168565"
---
# <a name="about-syslink-controls"></a>Acerca de los controles SysLink

Un control SysLink es una ventana que representa texto marcado y notifica a la aplicación cuando los usuarios hacen clic en sus hipervínculos incrustados. Este control proporciona una alternativa cómoda al uso del botón [**de vínculo Comando**](button-styles.md). Para obtener más información, vea [Tipos de botón](button-types-and-styles.md).

Cada control SysLink puede admitir varios hipervínculos y puede acceder a cada hipervínculo a través de un índice de base cero. El control SysLink se define en la versión 6 de ComCtl32.dll y requiere un manifiesto o una directiva que especifique que se debe usar la versión 6 del archivo DLL si está disponible. Para obtener más información, vea [Habilitar estilos visuales.](cookbook-overview.md)

Este artículo contiene las secciones siguientes.

-   [Marcado syslink](#syslink-markup)
-   [Atributos de vínculo](#link-attributes)
-   [Estados de vínculo](#link-states)
-   [Limitaciones de la presentación de texto bidireccional](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a>Marcado syslink

El control SysLink admite la etiqueta delimitadora( a ) junto &lt; &gt; con los atributos **HREF** e **ID**. Un **HREF** puede ser cualquier protocolo, como http, ftp y mailto. Un **identificador** es un nombre opcional, único dentro de un control SysLink, y está asociado a un vínculo individual. Los vínculos también tienen asignado un índice de base cero según su posición dentro de la cadena. Este índice se usa para acceder a un vínculo.

## <a name="link-attributes"></a>Atributos de vínculo

Los atributos de cada vínculo se pueden establecer dentro de la etiqueta delimitadora de cada vínculo o mediante el envío [**del \_ mensaje SETITEM de LM.**](lm-setitem.md) Si se establece un atributo mediante su especificación dentro de la cadena de inicialización, simplemente se inicializa el valor. Puede cambiar el valor de un atributo mediante el uso posterior del **mensaje \_ SETITEM de LM.**

## <a name="link-states"></a>Estados de vínculo

Los elementos de vínculo pueden estar en cualquiera de los tres estados, representados por las marcas de la tabla siguiente.



| Marca de estado   | Apariencia y significado                                            |
|--------------|-------------------------------------------------------------------|
| LIS \_ CENTRADA | El vínculo tiene el foco del teclado y al presionar Entrar se activa. |
| LIS \_ HABILITADA | El vínculo está habilitado.                                              |
| LIS \_ VISITADA | El usuario ya ha visitado la dirección URL representada por el vínculo.     |



 

## <a name="limitations-on-bidirectional-text-display"></a>Limitaciones de la presentación de texto bidireccional

Algunos idiomas, como árabe o hebreo, se escriben de derecha a izquierda (RTL); El inglés se escribe de izquierda a derecha (LTR). La combinación de RTL con LTR se denomina texto bidireccional. La combinación de construcciones de marcado unicode o HTML LTR y RTL en cadenas de recursos, como marcadores de flujo bidireccionales para controlar el flujo de cadenas, puede que no produzca el resultado esperado al usar un control SysLink. Por ejemplo, es posible que una oración marcada con LTR no se muestre correctamente en el contexto RTL.

> [!Note]  
> Los controles SysLink no admiten la presentación bidireccional en todos los escenarios. Use un control SysLink solo si sabe que un diseño LTR o RTL simple es adecuado. De lo contrario, considere la posibilidad de usar una tecnología más avanzada, [como MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).

 

 

 