---
title: Directrices de extensión de metarchivo
description: Directrices de extensión de metarchivo
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Windows Metarchivos multimedia, extensiones
- Windows Metarchivos multimedia, extensiones de nombre de archivo
- metarchivos, extensiones
- metarchivos, extensiones de nombre de archivo
- Windows Multimedia, metarchivos
- extensiones de nombre de archivo para Windows metarchivos multimedia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aaa31f1364271b1b968244494586ba5006e7c292ca2d9a207cdd1c758b5e432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836973"
---
# <a name="metafile-extension-guidelines"></a>Directrices de extensión de metarchivo

Una extensión de nombre de archivo proporciona a un proveedor de software independiente (ISV) información sobre los requisitos de representación de una aplicación que usa la extensión y permite a los autores de contenido dirigirse a tipos generales de reproductores.

Windows Las extensiones de nombre de metarchivo multimedia se usan para identificar el formato de los archivos Windows multimedia a los que hace referencia un metarchivo. Windows Metarchivos multimedia con archivos de referencia de extensiones .lot, .wvx o .asx con extensiones .wma, .wmv y .asf, respectivamente. Todos los metarchivos, independientemente de la extensión de nombre de archivo usada, tienen la etiqueta de elemento **ASX** al principio del archivo con el atributo **version** especificado.

En la tabla siguiente se muestran los tipos de archivo multimedia a los que hace referencia cada tipo de extensión de nombre de archivo de metarchivo. Las columnas muestran extensiones de nombre de archivo multimedia y las filas muestran extensiones de nombre de metarchivo. Una X de una columna indica un tipo de archivo multimedia al que se puede hacer referencia mediante una extensión de nombre de archivo de metarchivo determinada.



| Extensión | .asf | .wma | .wmv |
|-----------|------|------|------|
| .wvx      | X    | X    | X    |
| .desenlace      | X    | X    |      |
| .asx      | X    |      |      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de nombre de archivo**](file-name-extensions.md)
</dt> <dt>

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




