---
title: Objeto del editor de metadatos
description: Objeto del editor de metadatos
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows SDK de formato multimedia, objetos del editor de metadatos
- Formato de sistemas avanzados (ASF), objetos del editor de metadatos
- ASF (formato de sistemas avanzados), objetos del editor de metadatos
- objects,metadata editor objects
- objetos del editor de metadatos, acerca de
- metadata,editor objects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8e78aaf6ada96a9cefa1a9ec6f4aa5708c7382539bc3b75493734c18d600b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027453"
---
# <a name="metadata-editor-object"></a>Objeto del editor de metadatos

El objeto del editor de metadatos se usa para editar la información almacenada en la sección de encabezado de los archivos ASF. Las cosas más comunes manipuladas por este objeto son los atributos de metadatos. Además, el editor de metadatos se ocupa de [*marcadores y*](wmformat-glossary.md) comandos de script. La única vez que necesita usar el editor de metadatos es cuando desea editar el encabezado de un archivo existente sin reproducirlo.

La función [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)crea el objeto del editor de metadatos, que establece un puntero a una **interfaz IWMMetadataEditor.** Las demás interfaces del objeto del editor de metadatos se pueden obtener llamando al **método QueryInterface.**

El objeto del editor de metadatos admite las interfaces siguientes.



| Interfaz                                        | Descripción                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | Permite a las aplicaciones de [*edición examinar las propiedades drm*](wmformat-glossary.md) de un archivo ASF sin tener derechos para reproducir el contenido protegido. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | Manipula atributos, marcadores y comandos de script en el encabezado.                                                                                                                                    |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | Recupera la información del códec. Hereda todos los métodos de **IWMHeaderInfo**.                                                                                                                         |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | Proporciona compatibilidad avanzada con atributos, incluidos atributos grandes, varios idiomas y nombres de atributos duplicados. Hereda todos los métodos de **IWMHeaderInfo** **e IWMHeaderInfo2.**      |
| [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | Abre, cierra y guarda los cambios en el encabezado de un archivo ASF.                                                                                                                                         |
| [**IWMMetadataEditor2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | Abre un archivo ASF para la edición de encabezados con varias opciones de acceso y uso compartido de archivos. Hereda todos los métodos de **IWMMetadataEditor**.                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Marcadores**](markers.md)
</dt> <dt>

[**Metadatos**](metadata.md)
</dt> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Comandos de script**](script-commands.md)
</dt> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




