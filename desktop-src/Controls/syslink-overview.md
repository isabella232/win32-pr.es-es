---
title: Acerca de los controles SysLink
description: Un control SysLink es una ventana que representa texto marcado y notifica a la aplicación cuando los usuarios hacen clic en sus hipervínculos incrustados. Este control proporciona una alternativa práctica al uso del botón de vínculo de comando. Para obtener más información, vea tipos de botón.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078433"
---
# <a name="about-syslink-controls"></a>Acerca de los controles SysLink

Un control SysLink es una ventana que representa texto marcado y notifica a la aplicación cuando los usuarios hacen clic en sus hipervínculos incrustados. Este control proporciona una alternativa práctica al uso del [**botón de vínculo de comando**](button-styles.md). Para obtener más información, vea [tipos de botón](button-types-and-styles.md).

Cada control SysLink puede admitir varios hipervínculos, y puede tener acceso a cada hipervínculo a través de un índice basado en cero. El control SysLink se define en el ComCtl32.dll versión 6 y requiere un manifiesto o una directiva que especifique que se debe usar la versión 6 del archivo DLL si está disponible. Para obtener más información, vea [habilitar estilos visuales](cookbook-overview.md).

Este artículo contiene las secciones siguientes.

-   [Marcado de SysLink](#syslink-markup)
-   [Atributos de vínculo](#link-attributes)
-   [Estados de vínculo](#link-states)
-   [Limitaciones de la presentación de texto bidireccional](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a>Marcado de SysLink

El control SysLink admite la etiqueta delimitadora ( &lt; a &gt; ) junto con los atributos **href** e **ID**. Un **href** puede ser cualquier protocolo, como http, FTP y mailto. Un **identificador** es un nombre opcional, único dentro de un control SysLink, y está asociado a un vínculo individual. A los vínculos también se les asigna un índice basado en cero según su posición dentro de la cadena. Este índice se utiliza para tener acceso a un vínculo.

## <a name="link-attributes"></a>Atributos de vínculo

Los atributos de cada vínculo se pueden establecer en la etiqueta delimitadora para cada vínculo o mediante el envío del mensaje [**LM \_ SETITEM**](lm-setitem.md) . La configuración de un atributo mediante su especificación en la cadena de inicialización simplemente inicializa el valor. Puede cambiar el valor de un atributo mediante el uso posterior del mensaje **de \_ SETITEM de LM** .

## <a name="link-states"></a>Estados de vínculo

Los elementos de vínculo pueden estar en cualquiera de los tres Estados, representados por las marcas de la tabla siguiente.



| Marca de estado   | Apariencia y significado                                            |
|--------------|-------------------------------------------------------------------|
| LIS \_ centrado | El vínculo tiene el foco de teclado y al presionar entrar se activa. |
| LIS \_ habilitado | El vínculo está habilitado.                                              |
| LIS \_ visitado | El usuario ya ha visitado la dirección URL representada por el vínculo.     |



 

## <a name="limitations-on-bidirectional-text-display"></a>Limitaciones de la presentación de texto bidireccional

Algunos idiomas, como el árabe o el hebreo, se escriben de derecha a izquierda (RTL); El inglés se escribe de izquierda a derecha (LTR). La combinación de RTL con LTR se denomina texto bidireccional. No se puede producir el resultado esperado cuando se usa un control SysLink para mezclar construcciones de marcado direccionales Unicode o con Unicode de LTR y RTL en cadenas de recursos, como marcadores de flujo bidireccionales para controlar el flujo de cadenas. Por ejemplo, es posible que una oración marcada por LTR no se muestre correctamente en el contexto RTL.

> [!Note]  
> Los controles SysLink no admiten la presentación bidireccional en todos los escenarios. Use un control SysLink solo si sabe que un diseño de LTR o RTL sencillo es adecuado. En caso contrario, considere la posibilidad de usar una tecnología más avanzada, como [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).

 

 

 