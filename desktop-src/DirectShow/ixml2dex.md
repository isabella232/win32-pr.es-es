---
description: La interfaz IXml2Dex guarda y carga los archivos de proyecto de servicios de edición de DirectShow (DES) en lenguaje de marcado extensible (XML). Esta interfaz también proporciona métodos para leer y escribir archivos de gráficos de DirectShow (. GRF).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Interfaz IXml2Dex (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690908"
---
# <a name="ixml2dex-interface"></a>Interfaz IXml2Dex

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IXml2Dex` interfaz guarda y carga los archivos de proyecto de [servicios de edición de DirectShow](directshow-editing-services.md) (DES) en lenguaje de marcado extensible (XML). Esta interfaz también proporciona métodos para leer y escribir archivos de gráficos de DirectShow (. GRF).

## <a name="members"></a>Miembros

La interfaz **IXml2Dex** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IXml2Dex** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IXml2Dex** tiene estos métodos.



| Método                                                      | Descripción                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**CopyXML**](ixml2dex-copyxml.md)                         | Sin implementar.<br/>                                                |
| [**CreateGraphFromFile**](ixml2dex-creategraphfromfile.md) | Sin implementar.<br/>                                                |
| [**Elimínelos**](ixml2dex-delete.md)                           | Sin implementar.<br/>                                                |
| [**PasteXML**](ixml2dex-pastexml.md)                       | Sin implementar.<br/>                                                |
| [**PasteXMLFile**](ixml2dex-pastexmlfile.md)               | Sin implementar.<br/>                                                |
| [**ReadXML**](ixml2dex-readxml.md)                         | Sin implementar.<br/>                                                |
| [**ReadXMLFile**](ixml2dex-readxmlfile.md)                 | Carga un archivo de proyecto XML.<br/>                                      |
| [**Reset**](ixml2dex-reset.md)                             | Sin implementar.<br/>                                                |
| [**WriteGrfFile**](ixml2dex-writegrffile.md)               | Escribe un gráfico de filtro en un archivo en formato. GRF.<br/>                 |
| [**WriteXML**](ixml2dex-writexml.md)                       | Convierte una escala de tiempo en una cadena XML.<br/>                         |
| [**WriteXMLFile**](ixml2dex-writexmlfile.md)               | Traduce una escala de tiempo a XML y escribe los datos XML en un archivo.<br/> |
| [**WriteXMLPart**](ixml2dex-writexmlpart.md)               | Sin implementar.<br/>                                                |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Internet Explorer 4,0 o posterior<br/>                                               |
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
