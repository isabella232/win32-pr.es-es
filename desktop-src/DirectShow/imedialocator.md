---
description: La interfaz IMediaLocator proporciona métodos para validar nombres de archivo en DirectShow Editing Services (DES).
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Interfaz IMediaLocator (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886809"
---
# <a name="imedialocator-interface"></a>IMediaLocator (interfaz)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IMediaLocator` interfaz proporciona métodos para validar nombres de archivo [en DirectShow Editing Services](directshow-editing-services.md) (DES). Use esta interfaz para asegurarse de que un nombre de archivo y una ruta de acceso determinados se correspondan con un archivo existente. Esta interfaz también proporciona una manera de buscar el archivo  en otras ubicaciones y mostrar un cuadro de diálogo Abrir para que el usuario pueda localizar el archivo.

El localizador de medios implementa esta interfaz. La escala de tiempo y el motor de representación también admiten la validación de nombres de archivo mediante los métodos siguientes:

-   [**IAMTimeline::ValidateSourceNames:**](iamtimeline-validatesourcenames.md)valida y actualiza los nombres de archivo en la escala de tiempo.
-   [**IRenderEngine::SetSourceNameValidation:**](irenderengine-setsourcenamevalidation.md)especifica cómo el motor de representación valida los nombres de archivo en el momento de la representación.

Normalmente, una aplicación DES llamará a estos métodos en lugar de crear directamente una instancia del localizador de medios. Para obtener más información, [vea Using the Media Locator](using-the-media-locator.md).

## <a name="members"></a>Members

La **interfaz IMediaLocator** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMediaLocator también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMediaLocator** tiene estos métodos.



| Método                                                     | Descripción                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**AddFoundLocation**](imedialocator-addfoundlocation.md) | Agrega un directorio a la caché de directorios.<br/>                                |
| [**FindMediaFile**](imedialocator-findmediafile.md)       | Busca un archivo y, si se realiza correctamente, recupera la ruta de acceso al archivo.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
