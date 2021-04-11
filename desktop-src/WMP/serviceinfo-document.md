---
title: Documento ServiceInfo
description: Documento ServiceInfo
ms.assetid: 48f84dd7-e458-4da2-ae2b-5949e867cd3a
keywords:
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 1 tiendas en línea, documento de ServiceInfo
- tipo 2 tiendas en línea, documento de ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539c4e1a58e5dbf88e1fc79909791a7dab767ef1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075371"
---
# <a name="serviceinfo-document"></a>Documento ServiceInfo

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Las tiendas en línea deben crear el documento ServiceInfo.xml. Este es el documento que utiliza la tienda en línea para configurar la interfaz de usuario de Windows Media Player cuando Windows Media Player 10 o posterior hospeda la tienda en línea.

Los siguientes elementos y sus atributos se admiten para las tiendas en línea de Windows Media Player.



| Elemento                                      | Descripción                                                                                                                                                                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlbumInfo](albuminfo-element.md)           | Especifica la dirección URL de la página web que Windows Media Player muestra cuando el usuario elige ver más información sobre un elemento multimedia determinado. Tipo 1: opcional<br/> Tipo 2 música: obligatorio<br/> Tipo 2 Commerce: omitido<br/>                                |
| [ButtonText](buttontext-element.md)         | Especifica la cadena de texto que Windows Media Player muestra para un botón del panel de tareas. Tipo 1: obligatorio<br/> Tipo 2 música: obligatorio<br/> Tipo 2 Commerce: obligatorio<br/>                                                                                             |
| [ButtonTip](buttontip-element.md)           | Especifica la información sobre herramientas que se muestra cuando el usuario apunta a un botón del panel de tareas. Tipo 1: opcional<br/> Tipo 2 música: opcional<br/> Tipo 2 Commerce: opcional<br/>                                                                                         |
| [BuyCD](buycd-element.md)                   | Especifica las direcciones URL de las páginas web que Windows Media Player muestra cuando el usuario decide hacer una compra. Tipo 1: obligatorio<br/> Tipo 2 música: obligatorio<br/> Tipo 2 Commerce: omitido<br/>                                                                      |
| [Color](color-element.md)                   | Especifica el color de fondo de los botones de navegación de tiendas en línea. Tipo 1: opcional<br/> Tipo 2 música: opcional<br/> Tipo 2 Commerce: opcional<br/>                                                                                                             |
| [Descripción](description-element.md)       | Especifica una descripción de la tienda en línea que se muestra durante la primera experiencia del usuario con una instalación de Windows Media Player. Requiere Windows Media Player 11. tipo 1: necesario<br/> Tipo 2 música: opcional<br/> Tipo 2 Commerce: opcional<br/> |
| [DownloadStatus](downloadstatus-element.md) | Especifica una dirección URL que el Media Player de Windows muestra como un vínculo para permitir que los usuarios vean el estado de la descarga. Tipo 1: omitido<br/> Tipo 2 música: opcional<br/> Tipo 2 Commerce: opcional<br/>                                                                         |
| [FriendlyName](friendlyname-element.md)     | Especifica la cadena de texto que Windows Media Player muestra al usuario para identificar la tienda en línea. Tipo 1: obligatorio<br/> Tipo 2 música: obligatorio<br/> Tipo 2 Commerce: obligatorio<br/>                                                                           |
| [HTMLView](htmlview-element.md)             | Especifica la dirección URL base de una página web de HTMLView. Tipo 1: opcional<br/> Tipo 2 música: opcional<br/> Tipo 2 Commerce: opcional<br/>                                                                                                                                   |
| [Imagen](image-element.md)                   | Especifica las imágenes que Windows Media Player muestra al usuario para representar la tienda en línea. Tipo 1: obligatorio<br/> Tipo 2 música: opcional<br/> Tipo 2 Commerce: opcional<br/>                                                                               |
| [InfoCenter](infocenter-element.md)         | Especifica la dirección URL de la página web que Windows Media Player muestra en la característica de la vista del centro de información de que **ahora se reproduce** cuando la tienda en línea está activa. Tipo 1: obligatorio<br/> Tipo 2 música: obligatorio<br/> Tipo 2 Commerce: omitido<br/>                           |
| [Instalación](install-element.md)               | Especifica los valores utilizados por el programa de instalación de Windows Media Player para instalar la tienda en línea predeterminada. Tipo 1: obligatorio<br/> Tipo 2 música: opcional<br/> Tipo 2 Commerce: omitido<br/>                                                                                          |
| [Navegar](navigate-element.md)             | Especifica una dirección URL base usada por las llamadas a **external. NavigateTaskPaneURL**. Tipo 1: opcional<br/> Tipo 2 música: opcional<br/> Tipo 2 Commerce: opcional<br/>                                                                                                          |
| [ServiceInfo](serviceinfo-element.md)       | Representa el elemento principal del documento ServiceInfo.xml. Tipo 1: obligatorio<br/> Tipo 2 música: obligatorio<br/> Tipo 2 Commerce: obligatorio<br/>                                                                                                                    |
| [ServiceTask1](servicetask1-element.md)     | Representa el primer panel de tareas de la tienda en línea. Tipo 1: obligatorio<br/> Tipo 2 música: obligatorio<br/> Tipo 2 Commerce: obligatorio<br/>                                                                                                                                     |
| [ServiceTask2](servicetask2-element.md)     | Representa el segundo panel de tareas de la tienda en línea. Tipo 1: omitido<br/> Tipo 2 música: opcional<br/> Tipo 2 Commerce: opcional<br/>                                                                                                                                     |
| [ServiceTask3](servicetask3-element.md)     | Representa el tercer panel de tareas de la tienda en línea. Tipo 1: omitido<br/> Tipo 2 música: opcional<br/> Tipo 2 Commerce: opcional<br/>                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





