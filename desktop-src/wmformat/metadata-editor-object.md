---
title: Objeto del editor de metadatos
description: Objeto del editor de metadatos
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- SDK de Windows Media Format, objetos de editor de metadatos
- Advanced Systems Format (ASF), objetos de editor de metadatos
- ASF (formato de sistemas avanzados), objetos de editor de metadatos
- objetos, objetos de editor de metadatos
- objetos de editor de metadatos, acerca de
- metadatos, objetos de editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789220"
---
# <a name="metadata-editor-object"></a>Objeto del editor de metadatos

El objeto editor de metadatos se usa para editar la información almacenada en la sección de encabezado de los archivos ASF. Los elementos más comunes manipulados por este objeto son atributos de metadatos. Además, el editor de metadatos trata los [*marcadores*](wmformat-glossary.md) y los comandos de script. La única vez que necesita usar el editor de metadatos es cuando desea editar el encabezado de un archivo existente sin reproducirlo.

La función [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)crea el objeto de editor de metadatos, que establece un puntero a una interfaz **IWMMetadataEditor** . Las demás interfaces del objeto de editor de metadatos se pueden obtener llamando al método **QueryInterface** .

El objeto del editor de metadatos admite las siguientes interfaces.



| Interfaz                                        | Descripción                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | Permite que las aplicaciones de edición examinen las propiedades [*DRM*](wmformat-glossary.md) de un archivo ASF sin tener ningún derecho para reproducir el contenido protegido. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | Manipula atributos, marcadores y comandos de script en el encabezado.                                                                                                                                    |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | Recupera información del códec. Hereda todos los métodos de **IWMHeaderInfo**.                                                                                                                         |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | Proporciona compatibilidad avanzada con atributos, incluidos atributos grandes, varios lenguajes y nombres de atributos duplicados. Hereda todos los métodos de **IWMHeaderInfo** y **IWMHeaderInfo2**.      |
| [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | Abre, cierra y guarda los cambios realizados en el encabezado de un archivo ASF.                                                                                                                                         |
| [**IWMMetadataEditor2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | Abre un archivo ASF para la edición de encabezados con varias opciones de acceso y uso compartido de archivos. Hereda todos los métodos de **IWMMetadataEditor**.                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Marcadores**](markers.md)
</dt> <dt>

[**Repositorio**](metadata.md)
</dt> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Comandos de script**](script-commands.md)
</dt> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




