---
description: Crear el archivo de recursos de idioma base
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Crear el archivo de recursos de idioma base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083264"
---
# <a name="creating-the-base-language-resource-file"></a>Crear el archivo de recursos de idioma base

Los recursos de los elementos de la interfaz de usuario se definen para el idioma básico que admite la aplicación, por ejemplo, Inglés (Estados Unidos). Un ejemplo de un archivo de recursos PE de Win32 es un archivo. rc, creado mediante el compilador RC. Para más información sobre la creación de archivos. rc, consulte [acerca de los archivos de recursos](../menurc/about-resource-files.md).

Si usa un archivo. RC para los recursos de idioma base, tiene la opción de usar un archivo de configuración de recursos para una representación XML de los datos de configuración de recursos. Para crear este archivo, consulte [preparación de un archivo de configuración de recursos](preparing-a-resource-configuration-file.md).

También puede usar un archivo PE que no sea de Win32 para definir recursos de idioma base. Por ejemplo, puede usar un archivo. XML o. txt para este fin.

> [!Note]  
> Al definir los recursos de idioma base mediante un archivo PE que no es de Win32, no puede usar el compilador RC para la definición de recursos. En su lugar, defina su propio formato de recursos y la aplicación debe proporcionar su propia funcionalidad para buscar y cargar los recursos necesarios.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Preparación de recursos](preparing-resources.md)
</dt> <dt>

[Preparación de un archivo de configuración de recursos](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
