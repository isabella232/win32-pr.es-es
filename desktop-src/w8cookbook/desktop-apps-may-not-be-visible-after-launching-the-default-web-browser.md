---
title: Es posible que las aplicaciones de escritorio no estén visibles después de iniciar el explorador Web predeterminado o las aplicaciones de la tienda Windows
description: Es posible que las aplicaciones de escritorio no estén visibles después de iniciar el explorador Web predeterminado o las aplicaciones de la tienda Windows
ms.assetid: 5D2CE14B-111D-4987-A9AA-B04AC030F9F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c80541a860bd29f207ab99eba6ab4cb629a666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104359456"
---
# <a name="desktop-apps-may-not-be-visible-after-launching-the-default-web-browser-or-windows-store-apps"></a>Es posible que las aplicaciones de escritorio no estén visibles después de iniciar el explorador Web predeterminado o las aplicaciones de la tienda Windows

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

La experiencia del usuario de la aplicación de la tienda Windows se centra en una sola aplicación cada vez, con multitarea, conmutación de aplicaciones y notificaciones proporcionadas por la interfaz de usuario de Windows. Las aplicaciones de la tienda Windows tienen el tamaño para rellenar el espacio disponible en pantalla, con la vista más común en pantalla completa. Por lo tanto, cuando se inicia otra aplicación en el sistema, ya no puede suponer que la nueva aplicación se abrirá en una ventana de escritorio junto con la aplicación de escritorio. Esto siempre es cierto en el caso de las aplicaciones y exploradores de la tienda Windows que optan por participar en la nueva experiencia de interfaz de usuario de Windows. Puede seguir viendo otras aplicaciones al mismo tiempo, por ejemplo, si está en el escritorio y inicia otra aplicación de escritorio o tiene aplicaciones en un estado ajustado.

## <a name="manifestation"></a>Manifestación

Cuando una aplicación de escritorio usa técnicas de activación de aplicaciones comunes, como el uso de la API de ShellExecute en un archivo o protocolo, Windows inicia la aplicación asociada a ese registro, que puede ser una aplicación de la tienda Windows o el explorador Web predeterminado del usuario (el explorador Web predeterminado puede optar por participar en el escritorio o en la nueva interfaz de usuario de Windows). Las aplicaciones de la tienda Windows se inician con la pantalla completa, ocultando el escritorio y la aplicación de escritorio desde la que se inició.

> [!Note]  
> En Windows 8, Internet Explorer 10 se configura como el explorador predeterminado del usuario, pero el usuario puede optar por instalar y establecer otro explorador como predeterminado (sin cambios en Windows 7). En Internet Explorer 10, cuando se abre un vínculo desde una aplicación de escritorio, se abre Internet Explorer en el escritorio. Pero los usuarios pueden cambiar esta configuración para que Internet Explorer se abra como una aplicación de la tienda Windows. Se recomienda a los proveedores de explorador adoptar una experiencia similar de "Inicio contextual"; sin embargo, los desarrolladores deben planear el hecho de que no todos los exploradores se comportarán de forma similar.

 

## <a name="mitigation"></a>Mitigación

Aunque no hay ningún cambio que los desarrolladores puedan hacer a sus aplicaciones para mitigar este comportamiento, hay cosas que puede hacer el usuario final que debe comunicarse. Considere la posibilidad de usar la información recopilada por la API Extended ShellExecuteEx () para rellenar un cuadro de diálogo adecuado contextualmente. En ese cuadro de diálogo, indique al usuario qué aplicación se iniciará y si se trata de una aplicación de la tienda Windows o de una aplicación de escritorio. El CLSID puede usarse para distinguir las aplicaciones de la tienda Windows de las aplicaciones de escritorio. Opciones de usuario:

-   Los usuarios que tienen un monitor de pantalla ancha pueden ajustar la aplicación de la tienda Windows al borde de la pantalla para exponer el escritorio y, por tanto, ver la aplicación de la tienda Windows y la aplicación de escritorio al mismo tiempo.
-   Si Internet Explorer está configurado como el explorador predeterminado del usuario, los usuarios pueden cambiar su comportamiento cambiando las opciones de Internet en el panel de control. En la pestaña programas, los usuarios pueden cambiar el modo en que Internet Explorer controla los vínculos. Otros exploradores pueden ofrecer una configuración similar.

 

 




