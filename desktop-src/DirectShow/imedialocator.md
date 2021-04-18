---
description: La interfaz IMediaLocator proporciona métodos para validar nombres de archivo en los servicios de edición de DirectShow (DES).
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Interfaz IMediaLocator (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679026"
---
# <a name="imedialocator-interface"></a>Interfaz IMediaLocator

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IMediaLocator` interfaz proporciona métodos para validar nombres de archivo en los [servicios de edición de DirectShow](directshow-editing-services.md) (des). Utilice esta interfaz para asegurarse de que un nombre de archivo y una ruta de acceso especificados corresponden a un archivo existente. Esta interfaz también proporciona una manera de buscar el archivo en otras ubicaciones y mostrar un cuadro de diálogo **abierto** para que el usuario pueda localizar el archivo.

El localizador multimedia implementa esta interfaz. La escala de tiempo y el motor de representación también admiten la validación de nombres de archivo a través de los métodos siguientes:

-   [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md): valida y actualiza los nombres de archivo en la escala de tiempo.
-   [**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): especifica cómo valida el motor de representación los nombres de archivo en tiempo de representación.

Normalmente, una aplicación DES llamará a estos métodos en lugar de crear directamente una instancia del localizador de medios. Para obtener más información, consulte [uso del localizador de medios](using-the-media-locator.md).

## <a name="members"></a>Miembros

La interfaz **IMediaLocator** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMediaLocator** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMediaLocator** tiene estos métodos.



| Método                                                     | Descripción                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**AddFoundLocation**](imedialocator-addfoundlocation.md) | Agrega un directorio a la caché de directorio.<br/>                                |
| [**FindMediaFile**](imedialocator-findmediafile.md)       | Busca un archivo y, si lo logra, recupera la ruta de acceso al archivo.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
