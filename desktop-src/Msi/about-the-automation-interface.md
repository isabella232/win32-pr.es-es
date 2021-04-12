---
description: Un objeto instalador debe crearse inicialmente para cargar la compatibilidad de automatización necesaria para obtener acceso a los componentes del instalador a través de COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Acerca de la interfaz de automatización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276538"
---
# <a name="about-the-automation-interface"></a>Acerca de la interfaz de automatización

Un [**objeto instalador**](installer-object.md) debe crearse inicialmente para cargar la compatibilidad de automatización necesaria para obtener acceso a los componentes del instalador a través de com. Este objeto proporciona contenedores para crear los objetos de nivel superior y obtener acceso a sus métodos. Estos contenedores simplemente proporcionan traducciones de parámetros para exponer las funciones del instalador de manera coherente con Microsoft Visual Basic sin cambiar el comportamiento de los métodos.

Siempre que sea posible, se expone un par de métodos de C++ GET y set a Visual Basic como una propiedad única. En algunos casos, los métodos de C++ que toman un argumento de índice se exponen como una propiedad indizada. Muchos métodos de C++ devuelven el resultado a través de un parámetro, ya que el valor devuelto se utiliza para devolver el error. Sin embargo, en Visual Basic, los errores se controlan mediante un mecanismo independiente y el resultado siempre se pasa en el valor devuelto.

Para obtener información sobre el uso de la automatización y la creación del objeto de instalador, vea [usar la interfaz de automatización](using-the-automation-interface.md).

Para obtener material de referencia sobre los objetos de Windows Installer, vea referencia de la [interfaz de automatización](automation-interface-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



