---
description: La interfaz IDxtJpeg establece las propiedades en la transición de borrado de SMPTE. Esta interfaz la usa internamente DirectShow Editing Services (DES) cuando representa la transición de borrado de SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interfaz IDxt Serialeg (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261300"
---
# <a name="idxtjpeg-interface"></a>IDxtEnceeg (interfaz)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IDxtJpeg` interfaz establece las propiedades en la transición de borrado de [SMPTE.](smpte-wipe-transition.md)

Esta interfaz la usa internamente DirectShow Editing Services (DES) cuando representa la transición de borrado de SMPTE. Las aplicaciones DES no necesitan usar esta interfaz. Para establecer las propiedades en una transición en DES, use la [**interfaz IPropertySetter.**](ipropertysetter.md)

## <a name="members"></a>Members

La **interfaz IDxtPxeg** hereda de **IDXEffect**. **IDxtXtEg también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDxtJpeg** tiene estos métodos.



| Método                                                     | Descripción                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ApplyChanges**](idxtjpeg-applychanges.md)              | Aplica las propiedades que han cambiado.<br/>                                      |
| [**get \_ BorderColor**](idxtjpeg-get-bordercolor.md)       | Recupera el color del borde alrededor de los bordes del patrón de borrado.<br/>        |
| [**get \_ BorderSoftness**](idxtjpeg-get-bordersoftness.md) | Recupera el ancho de la región desenfoque alrededor de los bordes del patrón de borrado.<br/> |
| [**get \_ BorderWidth**](idxtjpeg-get-borderwidth.md)       | Recupera el ancho del borde sólido a lo largo de los bordes del patrón de borrado.<br/>   |
| [**get \_ MaskName**](idxtjpeg-get-maskname.md)             | Recupera el nombre de un archivo JPEG que se va a usar como máscara de borrado.<br/>                 |
| [**get \_ MaskNum**](idxtjpeg-get-masknum.md)               | Recupera el código de borrado de SMPTE del borrado.<br/>                                     |
| [**get \_ OffsetX**](idxtjpeg-get-offsetx.md)               | Recupera el desplazamiento horizontal del origen del borrado.<br/>                            |
| [**get \_ OffsetY**](idxtjpeg-get-offsety.md)               | Recupera el desplazamiento vertical del origen de borrado.<br/>                              |
| [**get \_ ReplicateX**](idxtjpeg-get-replicatex.md)         | Recupera el número de veces que el patrón de borrado se replica horizontalmente.<br/>     |
| [**get \_ ReplicateY**](idxtjpeg-get-replicatey.md)         | Recupera el número de veces que el patrón de borrado se replica verticalmente.<br/>       |
| [**get \_ ScaleX**](idxtjpeg-get-scalex.md)                 | Recupera la cantidad por la que se extiende horizontalmente el borrado.<br/>              |
| [**get \_ ScaleY**](idxtjpeg-get-scaley.md)                 | Recupera la cantidad por la que se extiende verticalmente el borrado.<br/>                |
| [**LoadDefSettings**](idxtjpeg-loaddefsettings.md)        | Restaura la configuración predeterminada de la transición de borrado.<br/>                          |
| [**put \_ BorderColor**](idxtjpeg-put-bordercolor.md)       | Especifica el color del borde alrededor de los bordes del patrón de borrado.<br/>        |
| [**put \_ BorderSoftness**](idxtjpeg-put-bordersoftness.md) | Especifica el ancho de la región desenfoque alrededor de los bordes del patrón de borrado.<br/> |
| [**put \_ BorderWidth**](idxtjpeg-put-borderwidth.md)       | Especifica el ancho del borde sólido a lo largo de los bordes del patrón de borrado.<br/>   |
| [**put \_ MaskName**](idxtjpeg-put-maskname.md)             | Especifica el nombre de un archivo JPEG que se usará como máscara de borrado.<br/>                     |
| [**put \_ MaskNum**](idxtjpeg-put-masknum.md)               | Especifica el código de borrado de SMPTE del borrado.<br/>                                     |
| [**put \_ OffsetX**](idxtjpeg-put-offsetx.md)               | Especifica el desplazamiento horizontal del origen del borrado.<br/>                            |
| [**put \_ OffsetY**](idxtjpeg-put-offsety.md)               | Especifica el desplazamiento vertical del origen del borrado.<br/>                              |
| [**put \_ ReplicateX**](idxtjpeg-put-replicatex.md)         | Especifica el número de veces que el patrón de borrado se replica horizontalmente.<br/>     |
| [**put \_ ReplicateY**](idxtjpeg-put-replicatey.md)         | Especifica el número de veces que el patrón de borrado se replica verticalmente.<br/>       |
| [**put \_ ScaleX**](idxtjpeg-put-scalex.md)                 | Especifica la cantidad por la que se extiende horizontalmente el borrado.<br/>              |
| [**put \_ ScaleY**](idxtjpeg-put-scaley.md)                 | Especifica la cantidad por la que se extiende verticalmente el borrado.<br/>                |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 




