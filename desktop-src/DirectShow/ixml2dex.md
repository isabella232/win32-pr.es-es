---
description: La interfaz IXml2Dex guarda y carga DirectShow de proyecto de Editing Services (DES) en lenguaje de marcado extensible (XML). Esta interfaz también proporciona métodos para leer y escribir DirectShow de gráficos (.grf).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Interfaz IXml2Dex (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061058"
---
# <a name="ixml2dex-interface"></a>Interfaz IXml2Dex

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La interfaz guarda y carga DirectShow de proyecto `IXml2Dex` de [Editing Services](directshow-editing-services.md) (DES) en lenguaje de marcado extensible (XML). Esta interfaz también proporciona métodos para leer y escribir DirectShow de gráficos (.grf).

## <a name="members"></a>Members

La **interfaz IXml2Dex** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IXml2Dex** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IXml2Dex** tiene estos métodos.



| Método                                                      | Descripción                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**CopyXML**](ixml2dex-copyxml.md)                         | Sin implementar.<br/>                                                |
| [**CreateGraphFromFile**](ixml2dex-creategraphfromfile.md) | Sin implementar.<br/>                                                |
| [**Eliminar**](ixml2dex-delete.md)                           | Sin implementar.<br/>                                                |
| [**PasteXML**](ixml2dex-pastexml.md)                       | Sin implementar.<br/>                                                |
| [**PasteXMLFile**](ixml2dex-pastexmlfile.md)               | Sin implementar.<br/>                                                |
| [**Readxml**](ixml2dex-readxml.md)                         | Sin implementar.<br/>                                                |
| [**ReadXMLFile**](ixml2dex-readxmlfile.md)                 | Carga un archivo de proyecto XML.<br/>                                      |
| [**Reset**](ixml2dex-reset.md)                             | Sin implementar.<br/>                                                |
| [**WriteGrfFile**](ixml2dex-writegrffile.md)               | Escribe un gráfico de filtro en un archivo en formato .grf.<br/>                 |
| [**WriteXML**](ixml2dex-writexml.md)                       | Convierte una escala de tiempo en una cadena XML.<br/>                         |
| [**WriteXMLFile**](ixml2dex-writexmlfile.md)               | Convierte una escala de tiempo en XML y escribe los datos XML en un archivo.<br/> |
| [**WriteXMLPart**](ixml2dex-writexmlpart.md)               | Sin implementar.<br/>                                                |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Internet Explorer 4.0 o posterior<br/>                                               |
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
