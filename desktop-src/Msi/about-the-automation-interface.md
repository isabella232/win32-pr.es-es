---
description: Se debe crear inicialmente un objeto Installer para cargar la compatibilidad de automatización necesaria para acceder a los componentes del instalador a través de COM.
ms.assetid: 113ed443-a866-43d4-86bd-fc3b244f2edb
title: Acerca de la interfaz de Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655a01a4daccb805bec4a858337c1dce48f0fb82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159257"
---
# <a name="about-the-automation-interface"></a>Acerca de la interfaz de Automation

Se [**debe crear inicialmente**](installer-object.md) un objeto Installer para cargar la compatibilidad de automatización necesaria para acceder a los componentes del instalador a través de COM. Este objeto proporciona contenedores para crear los objetos de nivel superior y acceder a sus métodos. Estos contenedores simplemente proporcionan traducciones de parámetros para exponer las funciones del instalador de forma coherente con Microsoft Visual Basic sin cambiar el comportamiento de los métodos.

Siempre que sea posible, un par de métodos Get y Set de C++ se exponen a Visual Basic como una sola propiedad. En algunos casos, los métodos de C++ que toman un argumento de índice se exponen como una propiedad indizada. Muchos métodos de C++ devuelven el resultado a través de un parámetro porque el valor devuelto se usa para la devolución de errores. Sin embargo, en Visual Basic, los errores se controlan mediante un mecanismo independiente y el resultado siempre se pasa en el valor devuelto.

Para obtener información sobre el uso de la automatización y la creación del objeto Installer, vea [Using the Automation Interface](using-the-automation-interface.md).

Para obtener material de referencia para los Windows Installer, vea [Referencia de la interfaz de Automation](automation-interface-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 



