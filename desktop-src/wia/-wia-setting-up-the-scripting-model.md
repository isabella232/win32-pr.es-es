---
description: Para usar el modelo de scripting de adquisición de imágenes de Windows (WIA), debe tener el archivo Wiascr.dll instalado y registrado en el equipo.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Configurar el entorno de desarrollo del modelo de scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275453"
---
# <a name="setting-up-the-scripting-model-development-environment"></a>Configurar el entorno de desarrollo del modelo de scripting

Para usar el modelo de scripting de adquisición de imágenes de Windows (WIA), debe tener el archivo Wiascr.dll instalado y registrado en el equipo.

> [!Note]  
> Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA). Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Copie este archivo desde el SDK de WIA en el directorio *% WINDIR%*/system32 (por ejemplo, c: \\ Windows \\ system32). En la línea de comandos, vaya a este directorio y escriba **regsvr32 Wiascr.dll**.

Esto especifica la información necesaria en el registro del sistema.

Ahora está listo para usar el modelo de scripting de WIA.

 

 
