---
description: Define los metadatos del fabricante y del modelo para el dispositivo que se va a implementar. Este elemento solo se usa para implementaciones de dispositivos (hosts).
ms.assetid: 2ebd3092-39aa-469c-a8c9-23f373ba0e66
title: elemento thisModelMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872bcdfcf3f93bfc8fe307684c31cdebb2000b05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965228"
---
# <a name="thismodelmetadata-element"></a>elemento thisModelMetadata

Define los metadatos del fabricante y del modelo para el dispositivo que se va a implementar. Este elemento solo se usa para implementaciones de dispositivos (hosts).

## <a name="usage"></a>Uso

``` syntax
<thisModelMetadata>
  child elements
</thisModelMetadata>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                     | Descripción                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fabricante**](manufacturer.md)<br/>             | Nombre del fabricante. Al menos uno [](manufacturerls.md) de los [**fabricantesLS**](manufacturer.md) debe estar presente en los metadatos.<br/> <br/> |
| [**manufacturerLS**](manufacturerls.md)<br/>         | Versión localizada del nombre del fabricante.<br/> <br/>                                                                                                                 |
| [**manufacturerURL**](manufacturerurl.md)<br/>       | Dirección URL del fabricante.<br/> <br/>                                                                                                                                   |
| [**modelName**](modelname.md)<br/>                   | Nombre del dispositivo. Al menos uno de [**los valores modelName**](modelname.md) o [**modelNameLS**](modelnamels.md) debe estar presente en los metadatos.<br/> <br/>                   |
| [**modelNameLS**](modelnamels.md)<br/>               | Versión localizada del nombre del dispositivo.<br/> <br/>                                                                                                                       |
| [**modelNumber**](modelnumber.md)<br/>               | Número de modelo del dispositivo.<br/> <br/>                                                                                                                                 |
| [**modelURL**](modelurl.md)<br/>                     | Dirección URL del modelo de dispositivo.<br/> <br/>                                                                                                                           |
| [**PnPXDeviceCategory**](pnpxdevicecategory.md)<br/> | Categoría PnP-X a la que pertenece el dispositivo. <br/> <br/>                                                                                                                |
| [**presentationURL**](presentationurl.md)<br/>       | Dirección URL de los datos de presentación del modelo de dispositivo.<br/> <br/>                                                                                                        |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  manufacturer?, 
  manufacturerLS*, 
  manufacturerURL?, 
  modelName?, 
  modelNameLS*, 
  modelNumber, 
  modelURL?, 
  PnPXDeviceCategory?, 
  presentationURL?
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                     | Descripción                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Los metadatos del fabricante coinciden con la sección de metadatos del fabricante descrita en el perfil de dispositivo (consulte el perfil del dispositivo para obtener más información). Se debe proporcionar el nombre del fabricante o al menos una versión localizada del nombre del fabricante. Se debe proporcionar el nombre del modelo o al menos una versión localizada del nombre del modelo.

El [**elemento thisModelMetadataDefinition**](thismodelmetadatadefinition.md) se usa posteriormente para generar una constante de C que contiene esta información.

Si hay [**un elemento PnPXDeviceCategory,**](pnpxdevicecategory.md) [](hosted.md) al menos un elemento hospedado debe contener los elementos [**PnPXHardwareId**](pnpxhardwareid.md) y [**PnPXCompatibleId.**](pnpxcompatibleid.md) Del mismo modo, si los elementos **PnPXHardwareId** y  **PnPXCompatibleId** están presentes en un elemento hospedado, debe haber un elemento **PnPXDeviceCategory** dentro del **elemento thisModelMetadata.**

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




