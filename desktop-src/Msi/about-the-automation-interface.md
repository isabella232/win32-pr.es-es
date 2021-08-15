---
description: Se debe crear inicialmente un objeto Installer para cargar la compatibilidad de automatización necesaria para acceder a los componentes del instalador a través de COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Acerca de la interfaz de Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c51469240ad684d6fd32ffbc5466007e73f4e4ff7a870b6878b18f25f54d32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382072"
---
# <a name="about-the-automation-interface"></a>Acerca de la interfaz de Automation

Se [**debe crear inicialmente**](installer-object.md) un objeto Installer para cargar la compatibilidad de automatización necesaria para acceder a los componentes del instalador a través de COM. Este objeto proporciona contenedores para crear los objetos de nivel superior y acceder a sus métodos. Estos contenedores simplemente proporcionan traducciones de parámetros para exponer las funciones del instalador de forma coherente con Microsoft Visual Basic sin cambiar el comportamiento de los métodos.

Siempre que sea posible, un par de métodos Get y Set de C++ se exponen a Visual Basic como una sola propiedad. En algunos casos, los métodos de C++ que toman un argumento de índice se exponen como una propiedad indizada. Muchos métodos de C++ devuelven el resultado a través de un parámetro porque el valor devuelto se usa para la devolución de errores. Sin embargo, en Visual Basic, los errores se controlan mediante un mecanismo independiente y el resultado siempre se pasa en el valor devuelto.

Para obtener información sobre el uso de la automatización y la creación del objeto Installer, vea [Using the Automation Interface](using-the-automation-interface.md).

Para obtener material de referencia para los Windows Installer, vea [Referencia de la interfaz de Automation.](automation-interface-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



