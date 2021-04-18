---
description: La interfaz IDxtJpeg establece las propiedades en la transición de borrado de SMPTE. Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición de borrado de SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interfaz IDxtJpeg (QEDIT. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679425"
---
# <a name="idxtjpeg-interface"></a>Interfaz IDxtJpeg

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IDxtJpeg` interfaz establece las propiedades en la transición de [borrado de SMPTE](smpte-wipe-transition.md) .

Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición de borrado de SMPTE. Las aplicaciones DES no necesitan usar esta interfaz. Para establecer las propiedades de una transición en DES, use la interfaz [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Miembros

La interfaz **IDxtJpeg** hereda de **IDXEffect**. **IDxtJpeg** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDxtJpeg** tiene estos métodos.



| Método                                                     | Descripción                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ApplyChanges (**](idxtjpeg-applychanges.md)              | Aplica las propiedades que han cambiado.<br/>                                      |
| [**obtener \_ BorderColor**](idxtjpeg-get-bordercolor.md)       | Recupera el color del borde alrededor de los bordes del patrón de barrido.<br/>        |
| [**obtener \_ BorderSoftness**](idxtjpeg-get-bordersoftness.md) | Recupera el ancho de la región borrosa alrededor de los bordes del patrón de barrido.<br/> |
| [**obtener \_ BorderWidth**](idxtjpeg-get-borderwidth.md)       | Recupera el ancho del borde sólido a lo largo de los bordes del patrón de barrido.<br/>   |
| [**obtener \_ MaskName**](idxtjpeg-get-maskname.md)             | Recupera el nombre de un archivo JPEG que se usará como máscara de borrado.<br/>                 |
| [**obtener \_ MaskNum**](idxtjpeg-get-masknum.md)               | Recupera el código de borrado de SMPTE de la eliminación.<br/>                                     |
| [**obtener \_ offsetX**](idxtjpeg-get-offsetx.md)               | Recupera el desplazamiento horizontal del origen de borrado.<br/>                            |
| [**obtener \_ desplazamiento**](idxtjpeg-get-offsety.md)               | Recupera el desplazamiento vertical del origen de borrado.<br/>                              |
| [**obtener \_ ReplicateX**](idxtjpeg-get-replicatex.md)         | Recupera el número de veces que el patrón de barrido se replica horizontalmente.<br/>     |
| [**obtención de \_ replicación**](idxtjpeg-get-replicatey.md)         | Recupera el número de veces que el patrón de barrido se replica verticalmente.<br/>       |
| [**obtener \_ scaleX**](idxtjpeg-get-scalex.md)                 | Recupera la cantidad por la que se ajusta horizontalmente el borrado.<br/>              |
| [**obtener \_ escalado**](idxtjpeg-get-scaley.md)                 | Recupera la cantidad por la que se ajusta verticalmente el borrado.<br/>                |
| [**LoadDefSettings**](idxtjpeg-loaddefsettings.md)        | Restaura la configuración predeterminada de la transición de borrado.<br/>                          |
| [**poner \_ BorderColor**](idxtjpeg-put-bordercolor.md)       | Especifica el color del borde alrededor de los bordes del patrón de barrido.<br/>        |
| [**Put \_ BorderSoftness**](idxtjpeg-put-bordersoftness.md) | Especifica el ancho de la región borrosa alrededor de los bordes del patrón de barrido.<br/> |
| [**poner \_ BorderWidth**](idxtjpeg-put-borderwidth.md)       | Especifica el ancho del borde sólido a lo largo de los bordes del patrón de barrido.<br/>   |
| [**Put \_ MaskName**](idxtjpeg-put-maskname.md)             | Especifica el nombre de un archivo JPEG que se va a usar como máscara de borrado.<br/>                     |
| [**Put \_ MaskNum**](idxtjpeg-put-masknum.md)               | Especifica el código de borrado de SMPTE de la eliminación.<br/>                                     |
| [**Put \_ offsetX**](idxtjpeg-put-offsetx.md)               | Especifica el desplazamiento horizontal del origen de borrado.<br/>                            |
| [**colocar \_ desplazamiento**](idxtjpeg-put-offsety.md)               | Especifica el desplazamiento vertical del origen de borrado.<br/>                              |
| [**Put \_ ReplicateX**](idxtjpeg-put-replicatex.md)         | Especifica el número de veces que el patrón de barrido se replica horizontalmente.<br/>     |
| [**poner en \_ replicación**](idxtjpeg-put-replicatey.md)         | Especifica el número de veces que el patrón de barrido se replica verticalmente.<br/>       |
| [**poner \_ scaleX**](idxtjpeg-put-scalex.md)                 | Especifica la cantidad por la que se ajusta horizontalmente el borrado.<br/>              |
| [**colocar \_ escalado**](idxtjpeg-put-scaley.md)                 | Especifica la cantidad por la que se ajusta verticalmente el borrado.<br/>                |



 

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



 

 




