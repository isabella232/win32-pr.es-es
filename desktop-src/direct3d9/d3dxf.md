---
description: Opciones de formato de archivo X, carga y guardado.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e230fc08ac4d7f8713959f2025f67262046ecea5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072804"
---
# <a name="d3dxf"></a>D3DXF

Opciones de formato de archivo X, carga y guardado.

## <a name="file-formats"></a>Formatos de archivo

En la tabla siguiente se especifica el tipo de datos de archivo:



| \#define para El formato de archivo     | Value | Descripción                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| D3DXF \_ FILEFORMAT \_ BINARY     | 0     | Archivo binario con formato heredado. Vea [X File Reference (Legacy) [Referencia de archivo X (heredado)].](dx9-graphics-reference-x-file.md) |
| TEXTO DEL FORMATO DE ARCHIVO D3DXF \_ \_       | 1     | Archivo de texto.                                                                                     |
| FORMATO DE ARCHIVO D3DXF \_ \_ COMPRIMIDO | 2     | Archivo comprimido. Con esta marca, también debe especificar el formato binario o el formato de texto.   |



 

## <a name="file-load-options"></a>Opciones de carga de archivos

En la tabla siguiente se especifican las opciones de carga de archivos con archivos .x:



| \#Definir                      | Value | Descripción                |
|-------------------------------|-------|----------------------------|
| D3DXF \_ FILELOAD \_ FromFile     | 0     | Cargar datos desde un archivo.     |
| D3DXF \_ FILELOAD \_ FROMWFILE    | 1     | Cargar datos desde un archivo.     |
| D3DXF \_ FILELOAD \_ FROMRESOURCE | 2     | Carga de datos desde un recurso. |
| D3DXF \_ FILELOAD \_ FROMMEMORY   | 3     | Cargar datos desde la memoria.     |



 

## <a name="file-save-options"></a>Opciones de guardado de archivos

En la tabla siguiente se especifican las opciones de guardado y carga de archivos con archivos .x:



| \#Definir                 | Value | Descripción                    |
|--------------------------|-------|--------------------------------|
| D3DXF \_ FILESAVE \_ TOFILE  | 0     | Guarde en un archivo.                |
| D3DXF \_ FILESAVE \_ TOWFILE | 1     | Guarde en un archivo de caracteres anchos. |



 

## <a name="constant-information"></a>Información constante



| Requisito                         | Value           |
|--------------------------|------------|
| Encabezado                   | d3dx9xof.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de archivo D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[**D3DXSaveMeshToX**](d3dxsavemeshtox.md)
</dt> </dl>

 

 



