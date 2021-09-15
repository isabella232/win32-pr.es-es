---
description: Windows Adquisición de imágenes (WIA) proporciona objetos de automatización para su uso en lenguajes de scripting, como software de desarrollo microsoft JScript y Microsoft Visual Basic Scripting Edition (VBScript), y lenguajes de programación de alto nivel, como el sistema de desarrollo de Microsoft Visual Basic.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467133"
---
# <a name="wia-scripting-model"></a>Modelo de scripting de WIA

Windows Adquisición de imágenes (WIA) proporciona objetos de automatización para su uso en lenguajes de scripting, como software de desarrollo microsoft JScript y Microsoft Visual Basic Scripting Edition (VBScript), y lenguajes de programación de alto nivel, como el sistema de desarrollo de Microsoft Visual Basic.

> [!Note]  
> Este sistema de scripting se ha reemplazado por Windows capa de automatización de adquisición de imágenes (WIA). Consulte [Windows capa de automatización de adquisición de imágenes.](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

 

En la tabla siguiente se describen los objetos de scripting de WIA y cómo se usan. 

| Object                                | Descripción                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wia**](-wia-wia.md)               | Objeto de scripting de WIA de nivel superior. Use el [**objeto Wia**](-wia-wia.md) para enumerar y conectarse a dispositivos, y para controlar eventos de dispositivos de hardware.                                        |
| [**DeviceInfo**](-wia-deviceinfo.md) | El [**objeto DeviceInfo**](-wia-deviceinfo.md) proporciona acceso a información sobre las propiedades del dispositivo.                                                                                     |
| [**Elemento**](-wia-item.md)             | Este objeto representa elementos de dispositivo, archivo y carpeta WIA. Un dispositivo de hardware WIA y sus imágenes o examen se representan como un árbol jerárquico de [**objetos Item.**](-wia-item.md) |



 

Tanto el [**objeto DeviceInfo**](-wia-deviceinfo.md) como el [**objeto Item**](-wia-item.md) están asociados a objetos de colección. Para obtener información sobre el uso de objetos de colección, consulte Uso de objetos de colección de WIA.

En los temas siguientes se trata información general sobre el uso del modelo de scripting de WIA:

-   [Convenciones de sintaxis](-wia-syntax-conventions.md)
-   [Uso de objetos de colección wia](-wia-using-wia-collection-objects.md)
-   [Definiciones de constantes de propiedad WIA](-wia-wia-property-constant-definitions.md)

 

 
