---
description: Cuando un usuario hace clic con el botón derecho en un objeto shell, el menú contextual que se muestra normalmente incluye un elemento Propiedades.
title: Controladores de hoja de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 27327db4718430ba646d9566227116e304d4d5f5770d0119987b32e0cd2adce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719547"
---
# <a name="property-sheet-handlers"></a>Controladores de hoja de propiedades

Cuando un usuario hace clic con el botón derecho en un objeto shell, el menú contextual que se muestra normalmente incluye un **elemento** Propiedades. Al seleccionar ese elemento se inicia una hoja de propiedades que permite al usuario ver y, en algunos casos, modificar las propiedades del objeto. Puede personalizar esta hoja de propiedades implementando y registrando un controlador *de hoja de propiedades*.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se de abordan en [Creación de controladores de extensión de shell](handlers.md). Este documento se centra en los aspectos de implementación específicos de los controladores de hoja de propiedades.

-   [Cómo funcionan los controladores de hoja de propiedades](#how-property-sheet-handlers-work)
-   [Registrar e implementar un controlador de hoja de propiedades para una unidad montada](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [Temas relacionados](#related-topics)

## <a name="how-property-sheet-handlers-work"></a>Cómo funcionan los controladores de hoja de propiedades

En la ilustración siguiente se muestra la hoja de propiedades Propiedades de un Windows de texto XP.

![hoja de propiedades](images/propsheethandler1.jpg)

En esta ilustración se muestra la hoja de propiedades propiedades predeterminada que se muestra para cualquier archivo. Para muchas de estas hojas de propiedades, puede agregar una o varias páginas a la hoja de propiedades implementando y registrando un controlador de hoja de propiedades.

Los controladores de hoja de propiedades se registran normalmente para un [tipo de archivo](fa-file-types.md). Cada controlador puede agregar una página personalizada a la hoja de propiedades Propiedades de la clase . Estas páginas suelen proporcionar a los usuarios acceso a propiedades específicas del tipo de archivo determinado. Por ejemplo, un tipo de archivo que consta de documentos de texto podría mostrar una página que enumera el título y el autor, y un resumen del documento. Se usa un caso especial de este tipo de controlador de hoja de propiedades para agregar una página a la hoja de propiedades Propiedades de una unidad montada.

El otro uso para los controladores de hoja de propiedades es reemplazar las páginas de las hojas de propiedades mostradas por Panel de control aplicaciones. Por ejemplo, un fabricante del mouse puede usar  un controlador de hoja de  propiedades para reemplazar la página Botones de la hoja de propiedades propiedades del mouse de Panel de control por una página personalizada para las características de su mouse.

Al igual que todos los controladores de extensión de Shell, los controladores de hoja de propiedades son objetos del Modelo de objetos componentes (COM) en proceso implementados como archivos DLL. Deben exportar dos interfaces además de [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext).

Shell usa la interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) para inicializar el controlador. Cuando el shell llama a [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), pasa un objeto de datos con el nombre del objeto y el puntero a una lista de identificadores de elemento (PIDL) de la carpeta que contiene el archivo. El *parámetro hRegKey* no se usa con controladores de hoja de propiedades. El **método IShellExtInit::Initialize** debe extraer el nombre de archivo del objeto de datos y almacenar el nombre y el PIDL de la carpeta para su uso posterior. Para obtener más información, vea *la sección Implementación de IShellExtInit* de Creating Shell Extension [Handlers](handlers.md).

El resto de la operación tiene lugar a través de la [**interfaz IShellPropSheetExt del**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) controlador. Si la hoja de propiedades está asociada a un tipo de archivo, el Shell llama a [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) para permitir que el controlador agregue una página a la hoja de propiedades. Si la hoja de propiedades está asociada a una aplicación Panel de control, el Shell llama a [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) para permitir que el controlador reemplace una página.

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a>Registrar e implementar un controlador de hoja de propiedades para una unidad montada

Cada unidad montada tiene una hoja Propiedades que el usuario puede mostrar. En la ilustración siguiente se muestra una hoja de propiedades de propiedades para una unidad de CD-ROM.

![Hoja de propiedades de cd-rom](images/propsheethandler2.jpg)

Hay una amplia variedad de dispositivos que se pueden montar como unidades. Dado que la hoja de propiedades predeterminada, diseñada para unidades de disco, podría no ser suficiente para algunos dispositivos, se puede implementar un controlador de hoja de propiedades para agregar una página específica para el dispositivo montado. La implementación básica de este tipo de controlador de hoja de propiedades es idéntica [a](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)la que se describe en Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo , con dos excepciones.

-   El objeto de datos pasado al método [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del controlador puede contener la ruta de acceso de la unidad en el formato [ \_ CFSTR MOUNTEDVOLUME](clipboard.md) en lugar del formato [ \_ HDROP de CF.](clipboard.md) El formato CF \_ HDROP se usa cuando el dispositivo se monta en una letra de unidad. El formato CFSTR MOUNTEDVOLUME se usa con sistemas de archivos NTFS cuando el dispositivo remoto se monta en una carpeta en lugar de \_ en una letra de unidad.
-   El GUID del controlador se registra en la clave **HKEY \_ CLASSES \_ ROOT** \\ **Drive** \\ **shellex** \\ **PropertySheetHandlers.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[Cómo registrar e implementar un controlador de hoja de propiedades para una Panel de control aplicación](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 
