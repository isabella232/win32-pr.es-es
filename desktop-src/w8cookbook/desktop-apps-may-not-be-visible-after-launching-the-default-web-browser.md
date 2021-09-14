---
title: Es posible que las aplicaciones de escritorio no sean visibles después de iniciar el explorador web predeterminado o Windows store.
description: Es posible que las aplicaciones de escritorio no sean visibles después de iniciar el explorador web predeterminado o Windows store.
ms.assetid: 5D2CE14B-111D-4987-A9AA-B04AC030F9F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c80541a860bd29f207ab99eba6ab4cb629a666
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362858"
---
# <a name="desktop-apps-may-not-be-visible-after-launching-the-default-web-browser-or-windows-store-apps"></a>Es posible que las aplicaciones de escritorio no sean visibles después de iniciar el explorador web predeterminado o Windows store.

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

La experiencia de usuario de la aplicación Windows Store se centra en una sola aplicación a la vez, con multitarea, cambio de aplicación y notificaciones proporcionadas por la interfaz de usuario Windows usuario. Windows Las aplicaciones de la Tienda tienen el tamaño para rellenar el espacio disponible en la pantalla, siendo la vista más común la pantalla completa. Por lo tanto, cuando se inicia otra aplicación en el sistema, ya no puede suponer que la nueva aplicación se abrirá en una ventana de escritorio junto con la aplicación de escritorio. Esto siempre sucede con las aplicaciones Windows store y los exploradores que deciden participar en la nueva experiencia de Windows de usuario. Puede seguir consultando otras aplicaciones al mismo tiempo, por ejemplo, si está en el escritorio e inicia otra aplicación de escritorio o tiene aplicaciones en un estado ajustado.

## <a name="manifestation"></a>Manifestación

Cuando una aplicación de escritorio usa técnicas comunes de activación de aplicaciones, como el uso de shellExecute API en un archivo o protocolo, Windows inicia la aplicación asociada a ese registro, que puede ser una aplicación de Windows Store y/o el explorador web predeterminado del usuario (el explorador web predeterminado podría optar por participar en el escritorio o en la nueva interfaz de usuario de Windows). Windows Las aplicaciones de la Tienda se inician con la pantalla completa, ocultando el escritorio y la aplicación de escritorio desde la que se inició.

> [!Note]  
> En Windows 8, Internet Explorer 10 se configura como explorador predeterminado del usuario, pero el usuario puede optar por instalar y establecer otro explorador como predeterminado (sin cambios desde Windows 7). En Internet Explorer 10, cuando se abre un vínculo desde una aplicación de escritorio, Internet Explorer se abrirá en el escritorio. Pero los usuarios pueden cambiar esta configuración para que Internet Explorer se abra como una Windows Store. Se ha animado a los proveedores de exploradores a adoptar una experiencia similar de "inicio contextual". Sin embargo, los desarrolladores deben planear el hecho de que no todos los exploradores se comportarán de forma similar.

 

## <a name="mitigation"></a>Mitigación

Aunque no hay ningún cambio que los desarrolladores puedan realizar en sus aplicaciones para mitigar este comportamiento, hay cosas que el usuario final puede hacer que se comunique con ellos. Considere la posibilidad de usar la información recopilada por la API ShellExecuteEx() extendida para rellenar un cuadro de diálogo contextualmente adecuado. En ese cuadro de diálogo, indique al usuario qué aplicación se va a iniciar y si esa aplicación es una aplicación Windows Store o una aplicación de escritorio. ClSID se puede usar para distinguir las aplicaciones Windows Store de las aplicaciones de escritorio. Opciones de usuario:

-   Los usuarios que tienen un monitor de pantalla ancha pueden ajustar la aplicación Windows Store al borde de la pantalla para exponer el escritorio y, por tanto, ver tanto la aplicación de Windows Store como la aplicación de escritorio al mismo tiempo.
-   Si Internet Explorer configurado como explorador predeterminado del usuario, los usuarios pueden cambiar su comportamiento cambiando las opciones de Internet en el Panel de control. En la pestaña Programas, los usuarios pueden cambiar cómo Internet Explorer los vínculos. Otros exploradores pueden ofrecer una configuración similar.

 

 




