---
description: Opciones de formato de archivo X, cargar y guardar.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073887c6cc93754ead01ce379310a9be09edc88f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696066"
---
# <a name="d3dxf"></a>D3DXF

Opciones de formato de archivo X, cargar y guardar.

## <a name="file-formats"></a>Formatos de archivo

En la tabla siguiente se especifica el tipo de datos de archivo:



| \#define el formato de archivo     | Value | Descripción                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| \_Binario de D3DXF FILEFORMAT \_     | 0     | Archivo binario de formato heredado. Consulte [referencia de archivo X (heredado)](dx9-graphics-reference-x-file.md). |
| D3DXF \_ \_ texto FILEFORMAT       | 1     | Archivo de texto.                                                                                     |
| D3DXF \_ FILEFORMAT \_ comprimido | 2     | Archivo comprimido. Con esta marca, también debe especificar el formato binario o el formato de texto.   |



 

## <a name="file-load-options"></a>Opciones de carga de archivos

En la tabla siguiente se especifican las opciones de carga de archivos con archivos. x:



| \#define                      | Value | Descripción                |
|-------------------------------|-------|----------------------------|
| D3DXF \_ FILELOAD \_ FromFile     | 0     | Cargar datos de un archivo.     |
| D3DXF \_ FILELOAD \_ FROMWFILE    | 1     | Cargar datos de un archivo.     |
| D3DXF \_ FILELOAD \_ FROMRESOURCE | 2     | Cargar datos de un recurso. |
| D3DXF \_ FILELOAD \_ FROMMEMORY   | 3     | Cargar datos de la memoria.     |



 

## <a name="file-save-options"></a>Opciones para guardar archivos

En la tabla siguiente se especifican las opciones de guardado y carga de archivos con archivos. x:



| \#define                 | Value | Descripción                    |
|--------------------------|-------|--------------------------------|
| D3DXF \_ ArchivoGuardar \_ TOFILE  | 0     | Guardar en un archivo.                |
| D3DXF \_ ArchivoGuardar \_ TOWFILE | 1     | Guardar en un archivo de caracteres anchos. |



 

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3dx9xof. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de archivo de D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[**D3DXSaveMeshToX**](d3dxsavemeshtox.md)
</dt> </dl>

 

 



