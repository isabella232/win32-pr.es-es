---
description: La adquisición de imágenes de Windows (WIA) proporciona objetos de automatización para su uso en lenguajes de scripting, como el software de desarrollo de Microsoft JScript y Microsoft Visual Basic Scripting Edition (VBScript), y lenguajes de programación de alto nivel, como el sistema de desarrollo de Microsoft Visual Basic.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Modelo de scripting de WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715173"
---
# <a name="wia-scripting-model"></a>Modelo de scripting de WIA

La adquisición de imágenes de Windows (WIA) proporciona objetos de automatización para su uso en lenguajes de scripting, como el software de desarrollo de Microsoft JScript y Microsoft Visual Basic Scripting Edition (VBScript), y lenguajes de programación de alto nivel, como el sistema de desarrollo de Microsoft Visual Basic.

> [!Note]  
> Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA). Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

En la tabla siguiente se describen los objetos de scripting de WIA y cómo se usan. 

| Object                                | Descripción                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WIA**](-wia-wia.md)               | Objeto de scripting de WIA de nivel superior. Use el objeto [**WIA**](-wia-wia.md) para enumerar y conectarse a los dispositivos, así como para controlar los eventos de los dispositivos de hardware.                                        |
| [**DeviceInfo**](-wia-deviceinfo.md) | El objeto [**DeviceInfo**](-wia-deviceinfo.md) proporciona acceso a información sobre las propiedades del dispositivo.                                                                                     |
| [**Elemento**](-wia-item.md)             | Este objeto representa los elementos de dispositivo, archivo y carpeta de WIA. Un dispositivo de hardware WIA y sus imágenes o escaneado de lecho se representan como un árbol jerárquico de objetos de [**elemento**](-wia-item.md) . |



 

Tanto el objeto [**DeviceInfo**](-wia-deviceinfo.md) como el objeto [**Item**](-wia-item.md) están asociados a objetos de colección. Para obtener información sobre el uso de objetos de colección, vea usar objetos de colección de WIA.

En los siguientes temas se incluye información general sobre el uso del modelo de scripting de WIA:

-   [Convenciones de sintaxis](-wia-syntax-conventions.md)
-   [Usar objetos de colección de WIA](-wia-using-wia-collection-objects.md)
-   [Definiciones de constantes de propiedades de WIA](-wia-wia-property-constant-definitions.md)

 

 
