---
title: Interfaces (marco de la cinta de opciones)
description: Documentación de referencia para las interfaces Windows marco de la cinta de opciones.
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c168a342b7f362d2d679d578a88011c9d14977
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466747"
---
# <a name="interfaces-ribbon-framework"></a>Interfaces (marco de la cinta de opciones)

Documentación de referencia para las interfaces Windows marco de la cinta de opciones.

### <a name="interfaces"></a>Interfaces



| Tema                                                                                  | Contenido                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | La aplicación implementa la interfaz [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) y define los métodos de punto de entrada de devolución de llamada para el marco de la cinta de opciones.<br/>                                                                                                                                                                                                              |
| [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)                         | La [**interfaz IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) se implementa mediante el marco de la cinta de opciones. La **interfaz IUICollection** define los métodos para manipular dinámicamente controles basados en colecciones, como las [distintas galerías](ribbon-controls-galleries.md) de la cinta de opciones y la barra de herramientas de acceso rápido (QAT), en tiempo de ejecución.<br/>                                              |
| [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | La aplicación implementa la interfaz [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) y define el método necesario para controlar los cambios en una colección en tiempo de ejecución.<br/>                                                                                                                                                                                |
| [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | La aplicación implementa la interfaz [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) y define los métodos para recopilar información de comandos y controlar eventos Command desde el marco de la cinta de opciones.<br/>                                                                                                                                                              |
| [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)                     | La [**interfaz IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)se implementa mediante el marco de la cinta de opciones y proporciona la funcionalidad básica para la [vista emergente de](windowsribbon-controls-contextpopup.md)contexto.<br/>                                                                                                                                                                       |
| [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                           | La [**interfaz IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) se implementa mediante el marco ribbon y define los métodos que proporcionan la funcionalidad principal para el marco.<br/>                                                                                                                                                                                                     |
| [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                   | La aplicación implementa la interfaz [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) y define el método para recuperar una imagen que se va a mostrar en la interfaz de usuario emergente de la cinta de opciones y el contexto del marco de la cinta de opciones .<br/>                                                                                                                                                                          |
| [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)               | [**IUIImageFromBitmap es**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap) una interfaz de generador implementada por el marco ribbon que define el método para crear un [**objeto IUIImage.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)<br/>                                                                                                                                                             |
| [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                                 | La [**interfaz IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) se implementa mediante el marco de cinta de opciones y proporciona la capacidad de especificar la configuración y las propiedades de una cinta de opciones. <br/>                                                                                                                                                                                                               |
| [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)           | [**IUISimplePropertySet es**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)una interfaz de solo lectura que define un método para recuperar el valor identificado por una clave de propiedad. Esta interfaz se implementa mediante el marco de cinta de opciones y también se implementa mediante la aplicación host para cada elemento en el [**objeto IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)de una galería de elementos.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Referencia del marco de opciones](windowsribbon-reference-entry.md)
</dt> </dl>

 

