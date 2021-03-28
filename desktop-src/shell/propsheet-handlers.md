---
description: Cuando un usuario hace clic con el botón secundario en un objeto de Shell, el menú contextual que se muestra normalmente incluye un elemento propiedades.
title: Controladores de hoja de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 40ccb8d1cee0fffb993aef417b979816597cf707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910769"
---
# <a name="property-sheet-handlers"></a>Controladores de hoja de propiedades

Cuando un usuario hace clic con el botón secundario en un objeto de Shell, el menú contextual que se muestra normalmente incluye un elemento **propiedades** . Al seleccionar ese elemento se inicia una hoja de propiedades que permite al usuario ver y, en algunos casos, modificar las propiedades del objeto. Puede personalizar esta hoja de propiedades implementando y registrando un *controlador* de la hoja de propiedades.

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se explican en [crear controladores de extensión de Shell](handlers.md). Este documento se centra en los aspectos de la implementación que son específicos de los controladores de hojas de propiedades.

-   [Cómo funcionan los controladores de hoja de propiedades](#how-property-sheet-handlers-work)
-   [Registro e implementación de un controlador de hoja de propiedades para una unidad montada](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [Temas relacionados](#related-topics)

## <a name="how-property-sheet-handlers-work"></a>Cómo funcionan los controladores de hoja de propiedades

En la ilustración siguiente se muestra la hoja de propiedades propiedades de un archivo de texto de Windows XP.

![hoja de propiedades](images/propsheethandler1.jpg)

En esta ilustración se muestra la hoja de propiedades de propiedades predeterminadas que se muestra para cualquier archivo. Para muchas de estas hojas de propiedades, puede Agregar una o varias páginas a la hoja de propiedades implementando y registrando un controlador de la hoja de propiedades.

Los controladores de hoja de propiedades se registran normalmente para un [tipo de archivo](fa-file-types.md). Cada controlador puede Agregar una página personalizada a la hoja de propiedades de propiedades de la clase. Normalmente, estas páginas proporcionan a los usuarios acceso a las propiedades que son específicas del tipo de archivo determinado. Un tipo de archivo que consta de documentos de texto podría, por ejemplo, mostrar una página con el título y el autor, y un resumen del documento. Se utiliza un caso especial de este tipo de controlador de la hoja de propiedades para agregar una página a la hoja de propiedades propiedades de una unidad montada.

El otro uso para los controladores de hojas de propiedades es reemplazar las páginas de las hojas de propiedades que se muestran en las aplicaciones del panel de control. Un fabricante del mouse, por ejemplo, puede usar un controlador de la hoja de propiedades para reemplazar la página **botones** de la hoja de propiedades del **mouse** del panel de control por una página personalizada para las características del mouse.

Al igual que todos los controladores de extensión de Shell, los controladores de hoja de propiedades son objetos de modelo de objetos componentes (COM) en proceso implementados como archivos dll. Deben exportar dos interfaces además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) y [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext).

El shell usa la interfaz [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) para inicializar el controlador. Cuando el shell llama a [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), pasa un objeto de datos con el nombre del objeto y el puntero a una lista de identificadores de elemento (PIDL) de la carpeta que contiene el archivo. El parámetro *hRegKey* no se utiliza con controladores de hoja de propiedades. El método **IShellExtInit:: Initialize** debe extraer el nombre de archivo del objeto de datos y almacenar el nombre y el PIDL de la carpeta para su uso posterior. Para obtener más información, vea la sección *implementación de IShellExtInit* de creación de controladores de [extensión de Shell](handlers.md).

El resto de la operación se lleva a cabo a través de la interfaz [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) del controlador. Si la hoja de propiedades está asociada a un tipo de archivo, el shell llama a [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) para permitir que el controlador agregue una página a la hoja de propiedades. Si la hoja de propiedades está asociada a una aplicación del panel de control, el shell llama a [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) para permitir que el controlador reemplace una página.

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a>Registro e implementación de un controlador de hoja de propiedades para una unidad montada

Cada unidad montada tiene una hoja de propiedades que el usuario puede mostrar. La siguiente ilustración muestra una hoja de propiedades de propiedades de una unidad de CD-ROM.

![propiedades de CD-ROM (hoja de propiedades)](images/propsheethandler2.jpg)

Hay una amplia variedad de dispositivos que se pueden montar como unidades. Dado que la hoja de propiedades predeterminada, diseñada para unidades de disco, podría no ser suficiente para algunos dispositivos, se puede implementar un controlador de hoja de propiedades para agregar una página específica del dispositivo montado. La implementación básica de este tipo de controlador de la hoja de propiedades es idéntica a la que se describe en [Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md), con dos excepciones.

-   El objeto de datos que se pasa al método [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) del controlador puede contener la ruta de acceso de la unidad en el formato [CFSTR \_ MOUNTEDVOLUME](clipboard.md) en lugar del formato [CF \_ HDROP](clipboard.md) . El \_ formato CF HDROP se usa cuando el dispositivo se monta en una letra de unidad. El \_ formato CFSTR MOUNTEDVOLUME se usa con sistemas de archivos NTFS cuando el dispositivo remoto se monta en una carpeta en lugar de en una letra de unidad.
-   El GUID del controlador se registra en la **\_ \_** \\  \\ clave **shellex** \\ **PropertySheetHandlers** de la unidad raíz HKEY.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[Cómo registrar e implementar un controlador de la hoja de propiedades para una aplicación del panel de control](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 
