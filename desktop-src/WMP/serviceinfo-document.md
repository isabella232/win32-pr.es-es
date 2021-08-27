---
title: Documento ServiceInfo
description: Documento ServiceInfo
ms.assetid: 48f84dd7-e458-4da2-ae2b-5949e867cd3a
keywords:
- Reproductor de Windows Media en línea,documento ServiceInfo
- online stores,ServiceInfo document
- tipo 1 tiendas en línea, documento ServiceInfo
- tipo 2 tiendas en línea, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88863bb75cd0a7b85bead1c20759b77710c2db483b4d9e48ed1f53741dd0840d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995425"
---
# <a name="serviceinfo-document"></a>Documento ServiceInfo

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Las tiendas en línea deben crear ServiceInfo.xml documento. Este es el documento que usa la tienda en línea para configurar la interfaz Reproductor de Windows Media usuario cuando Reproductor de Windows Media 10 o posterior hospeda la tienda en línea.

Los siguientes elementos y sus atributos se admiten para Reproductor de Windows Media en línea.



| Elemento                                      | Descripción                                                                                                                                                                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlbumInfo](albuminfo-element.md)           | Especifica la dirección URL de la página web que Reproductor de Windows Media cuando el usuario decide ver más información sobre un elemento multimedia determinado. Tipo 1: opcional<br/> Tipo 2 Música: obligatorio<br/> Comercio de tipo 2: omitido<br/>                                |
| [ButtonText](buttontext-element.md)         | Especifica la cadena de texto que Reproductor de Windows Media para un botón del panel de tareas. Tipo 1: obligatorio<br/> Tipo 2 Música: obligatorio<br/> Tipo 2 Comercio: obligatorio<br/>                                                                                             |
| [Información sobre botones](buttontip-element.md)           | Especifica la información sobre herramientas que se muestra cuando el usuario apunta a un botón del panel de tareas. Tipo 1: opcional<br/> Tipo 2 Música: opcional<br/> Tipo 2 Comercio: opcional<br/>                                                                                         |
| [BuyCD](buycd-element.md)                   | Especifica las direcciones URL de las páginas web que Reproductor de Windows Media cuando el usuario decide realizar una compra. Tipo 1: obligatorio<br/> Tipo 2 Música: obligatorio<br/> Comercio de tipo 2: omitido<br/>                                                                      |
| [Color](color-element.md)                   | Especifica el color de fondo de los botones de navegación de los almacenes en línea. Tipo 1: opcional<br/> Tipo 2 Música: opcional<br/> Tipo 2 Comercio: opcional<br/>                                                                                                             |
| [Descripción](description-element.md)       | Especifica una descripción de la tienda en línea que se muestra durante la primera experiencia del usuario con una instalación de Reproductor de Windows Media. Requiere Reproductor de Windows Media 11.Type 1: obligatorio<br/> Tipo 2 Música: opcional<br/> Tipo 2 Comercio: opcional<br/> |
| [DownloadStatus](downloadstatus-element.md) | Especifica una dirección URL que el Reproductor de Windows Media muestra como un vínculo para permitir que los usuarios puedan ver el estado de descarga. Tipo 1: omitido<br/> Tipo 2 Música: opcional<br/> Tipo 2 Comercio: opcional<br/>                                                                         |
| [FriendlyName](friendlyname-element.md)     | Especifica la cadena de texto que Reproductor de Windows Media muestra al usuario para identificar la tienda en línea. Tipo 1: obligatorio<br/> Tipo 2 Música: obligatorio<br/> Tipo 2 Comercio: obligatorio<br/>                                                                           |
| [HTMLView](htmlview-element.md)             | Especifica la dirección URL base de una página web HTMLView. Tipo 1: opcional<br/> Tipo 2 Música: opcional<br/> Tipo 2 Comercio: opcional<br/>                                                                                                                                   |
| [Imagen](image-element.md)                   | Especifica las imágenes que se Reproductor de Windows Media al usuario para representar la tienda en línea. Tipo 1: obligatorio<br/> Tipo 2 Música: opcional<br/> Tipo 2 Comercio: opcional<br/>                                                                               |
| [Infocenter](infocenter-element.md)         | Especifica la dirección URL de la página web que Reproductor de Windows Media muestra en la característica Vista del Centro de información de **Reproducción** ahora cuando la tienda en línea está activa. Tipo 1: obligatorio<br/> Tipo 2 Música: obligatorio<br/> Comercio de tipo 2: omitido<br/>                           |
| [Instalación](install-element.md)               | Especifica los valores usados por Reproductor de Windows Media instalación para instalar el almacén en línea predeterminado. Tipo 1: obligatorio<br/> Tipo 2 Música: opcional<br/> Comercio de tipo 2: omitido<br/>                                                                                          |
| [Navegar](navigate-element.md)             | Especifica una dirección URL base que usan las llamadas a **External.NavigateTaskPaneURL.** Tipo 1: opcional<br/> Tipo 2 Música: opcional<br/> Tipo 2 Comercio: opcional<br/>                                                                                                          |
| [ServiceInfo](serviceinfo-element.md)       | Representa el elemento principal del ServiceInfo.xml documento. Tipo 1: obligatorio<br/> Tipo 2 Música: obligatorio<br/> Tipo 2 Comercio: obligatorio<br/>                                                                                                                    |
| [ServiceTask1](servicetask1-element.md)     | Representa el primer panel de tareas del almacén en línea. Tipo 1: obligatorio<br/> Tipo 2 Música: obligatorio<br/> Tipo 2 Comercio: obligatorio<br/>                                                                                                                                     |
| [ServiceTask2](servicetask2-element.md)     | Representa el segundo panel de tareas del almacén en línea. Tipo 1: omitido<br/> Tipo 2 Música: opcional<br/> Tipo 2 Comercio: opcional<br/>                                                                                                                                     |
| [ServiceTask3](servicetask3-element.md)     | Representa el tercer panel de tareas del almacén en línea. Tipo 1: omitido<br/> Tipo 2 Música: opcional<br/> Tipo 2 Comercio: opcional<br/>                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo de ejemplo para una tienda en línea de tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Información común a las tiendas en línea de tipo 1 y tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





